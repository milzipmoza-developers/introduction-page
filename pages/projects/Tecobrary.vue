<template>
  <div class="root" style="width: auto; height: 500vh;" v-on:scroll.native="offsetTop">
    <div class="projects-navigation">
      <div class="navigation-body">
        <div style="color: white; font-size: 30px; font-weight: bold; float: left">
          offsetTop : {{ offsetTop }}
        </div>
        <div class="navigation-btn-container">
          <div class="navigation-btn">
            <div class="btn-text" onclick="location.href = '/#Welcome'">
              Welcome
            </div>
          </div>
          <div class="navigation-btn" onclick="location.href = '/#Introduction'">
            <div class="btn-text">
              Introduction
            </div>
          </div>
          <div class="navigation-btn" onclick="location.href = '/#Projects'">
            <div class="btn-text">
              Projects
            </div>
          </div>
          <div class="navigation-btn" onclick="location.href = '/#Members'">
            <div class="btn-text">
              Members
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="projects-container default-container">
      <div class="title-container text-align-center" style="height: 100vh; width: 100vw">
        <div class="title-block">
          <h1 class="title">TECOBRARY</h1>
          <h3 class="desc" onclick="window.open('https://dgh7qtsxun9z8.cloudfront.net/')">서비스 구경하기</h3>
        </div>
      </div>
    </div>
    <div id="first-content" class="content-container default-container" style="height: 100vh; width: auto; float: top">
      <img id="tecobrary-1" class="tecobrary-service-img" src="../../static/phone_fm_main.png"
           width="300vw" :style="tecobrary01Style"/>
      <img id="tecobrary-2" class="tecobrary-service-img" src="../../static/tecobrary/01_tecobrary_home.png"
           width="300vw" :style="tecobrary02Style"/>
      <div class="tecobrary-1-story-1 content-story-right" :style="tecobrary01Story01Style">
        <h1 class="title">김덕수(러너덕)과 박우빈(닉)님이 열어주신 대개발시대</h1>
        <h3 class="desc" onclick="window.open('https://www.youtube.com/watch?v=NfJjaGjVceo&t=4s')">발표영상 보러가기</h3>
      </div>
      <div class="content-story-right" :style="tecobrary01Story02Style">
        <h1 class="title">테코브러리의 시작</h1>
        <h3 class="desc">우아한테크코스의 도서 관리 시스템</h3>
      </div>
    </div>
  </div>
</template>

<script>

  const ANIM = {
    FIRST_IMAGE: {
      START_FADE_IN: 80,
      END_FADE_IN: 758,
      START_FADE_OUT: 1106,
      END_FADE_OUT: 1550,
    },
    STORY: {
      FIRST: {
        TOP: 566,
        MID: 706,
        BOT: 936
      },
      SECOND: {
        TOP: 966,
        MID: 1106,
        BOT: 1336
      },
    }
  }

  export default {
    name: "Tecobrary.vue",
    data: () => ({
      offsetTop: 0,
      ticking: false,
      tecobrary01Style: {
        opacity: 0,
        position: 'relative',
        left: '0vw'
      },
      tecobrary01Story01Style: {
        opacity: 0,
      },
      tecobrary01Story02Style: {
        opacity: 0
      },
      tecobrary02Style: {
        opacity: 1,
        position: 'fixed',
        left: '10vw',
        visibility: 'hidden',
        top: '20vh'
      }
    }),

    methods: {
      scrollListener(scroll_pos) {
        this.offsetTop = scroll_pos
      },
      _vue_opacityBasedOffset(start, end) {
        let value = (this.offsetTop - start) / (end - start)
        if (value < 0) return 0
        if (value > 1) return 1
        return value.toFixed(1)
      },

      _vue_isOffsetInRange(start, end) {
        return this.offsetTop >= start && this.offsetTop <= end
      },

      _vue_position_handling(props, position, left) {
        props.position = position
        props.left = left
      },

      _vue_story_duration(scroll, duration) {
        return scroll + duration
      },

      // 스토리 페이드 인 아웃
      _vue_story_fade_in_and_out(storyProps, start, mid, end) {
        // 스토리 페이드 인
        if (this._vue_isOffsetInRange(start, mid)) {
          storyProps.opacity = this._vue_opacityBasedOffset(start, mid)
        }
        // 텍스트 페이드 아웃
        if (this._vue_isOffsetInRange(mid + 30, end)) {
          storyProps.opacity = 1 - this._vue_opacityBasedOffset(mid + 30, end)
        }
      }
    },

    watch: {
      offsetTop: function () {
        // first-content
        if (this._vue_isOffsetInRange(0, 2000)) {
          // 첫번째 이미지 페이드 인
          if (this._vue_isOffsetInRange(ANIM.FIRST_IMAGE.START_FADE_IN, ANIM.FIRST_IMAGE.END_FADE_IN)) {
            this.tecobrary01Style.opacity = this._vue_opacityBasedOffset(ANIM.FIRST_IMAGE.START_FADE_IN, ANIM.FIRST_IMAGE.END_FADE_IN)
          }
          // 첫번째 이미지 위치 고정
          // TODO: Logic 수정
          if (this.offsetTop >= ANIM.FIRST_IMAGE.END_FADE_IN) {
            this.tecobrary01Style.top = '20vh'
            this._vue_position_handling(this.tecobrary01Style, 'fixed', '10vw')
          } else {
            this._vue_position_handling(this.tecobrary01Style, 'relative', '0vw')
            delete this.tecobrary01Style['top']
          }
          this._vue_story_fade_in_and_out(this.tecobrary01Story01Style, ANIM.STORY.FIRST.TOP, ANIM.STORY.FIRST.MID, ANIM.STORY.FIRST.BOT)
          this._vue_story_fade_in_and_out(this.tecobrary01Story02Style, ANIM.STORY.SECOND.TOP, ANIM.STORY.SECOND.MID, ANIM.STORY.SECOND.BOT)

          if (this.offsetTop > ANIM.FIRST_IMAGE.START_FADE_OUT) {
            this.tecobrary01Style.visibility = 'hidden'
            this.tecobrary02Style.visibility = 'visible'
          } else {
            this.tecobrary02Style.visibility = 'hidden'
            this.tecobrary01Style.visibility = 'visible'
          }
        }
      }
    },

    created() {
      if (process.client) {
        const self = this
        window.addEventListener('scroll', function (e) {
          const last_known_scroll_position = window.scrollY;

          if (!self.ticking) {
            window.requestAnimationFrame(function () {
              self.scrollListener(last_known_scroll_position);
              self.ticking = false;
            });

            self.ticking = true;
          }
        });
      }
    },


  }
</script>

<style scoped>
  div {
    font-family: 'Source Sans Pro', sans-serif;
  }

  .default-container {
    margin-right: 10vw;
    margin-left: 10vw;
  }

  .root {
    background-color: black;
  }

  .text-align-center {
    text-align: center;
  }

  .projects-navigation {
    background-color: black;
    width: 100vw;
    height: 50px;
    position: fixed;
  }

  .projects-navigation > .navigation-body {
    margin-right: 3vw;
    margin-left: 3vw;
    height: 50px;
    border-bottom: 1px gray solid;
  }

  .projects-navigation > .navigation-body > .navigation-btn-container {
    float: right;
  }

  .navigation-btn-container > .navigation-btn {
    color: gray;
    font-size: 16px;
    text-align: center;
    line-height: inherit;
    height: 50px;
    width: 10vw;
    float: left;
    display: table;
    cursor: pointer;
    transition: color 0.1s 0.15s;
  }

  .navigation-btn-container > .navigation-btn:hover {
    color: white;
  }

  .navigation-btn > .btn-text {
    text-align: center;
    display: table-cell;
    vertical-align: middle;
  }

  .projects-container {
    background-color: #999999;
    opacity: 1;
    display: table;
  }

  .title-container {
    background-color: #000000;
    transition: opacity 1s 1s;
    display: table-cell;
    vertical-align: middle;
    opacity: 1;
  }

  .title-container > .title-block {
    padding-top: 200px;
    padding-bottom: 200px;
    opacity: 1;
    pointer-events: all;
  }

  .title-container > .title-block > .title {
    font-size: 120px;
    letter-spacing: 0rem;
    color: white;
  }

  .title-container > .title-block > .desc {
    padding-top: 4vh;
    letter-spacing: 0rem;
    color: white;
  }

  .title-container > .title-block > .desc:hover {
    text-decoration: underline;
    cursor: pointer;
  }

  /* content-container */
  .content-container {
    background-color: black;
    /*background-color: gray;*/
  }

  .content-story-right {
    width: 55vw;
    position: fixed;
    top: 40%;
    right: 10vw;
  }

  .title {
    letter-spacing: 0rem;
    text-align: center;
    color: white;
  }

  .desc {
    margin-top: 4vh;
    letter-spacing: 0rem;
    text-align: center;
    color: white;
  }

  .tecobrary-1-story-1 > .desc:hover {
    text-decoration: underline;
    cursor: pointer;
  }

  .tecobrary-service-img {
    transition: visibility 0s, opacity 2s linear;
  }


  @media ( max-width: 2560px ) {
    /* 글씨 크기 조절 */
  }


  @media ( max-width: 1023px ) {
    /* 글씨 크기 조절 */
  }

  @media ( max-width: 734px ) {
    /* 모바일 */

  }

</style>

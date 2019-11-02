<template>
  <div class="section">
    <div class="project-container">
      <div class="project-title">
        Projects
      </div>
      <div class="project-content">
        <project-card
          v-for="(project, i) in projects" :key="i"
          :title=project.title
          :logo-src=project.logoSrc
          :logo-out-line=project.logoOutLine
          :content-lines=project.contentLines
          :github-href=project.githubHref
          :use-img-btn=project.useImgBtn
          :img-btn-href=project.imgBtnHref
          :desc-page=project.descPage
        >
        </project-card>
        <div class="project-footer">대개발시대의 많은 프로젝트들이 추가될 예정입니다.</div>
      </div>
    </div>
  </div>
</template>

<script>
  import ProjectCard from "../components/ProjectCard"

  export default {
    name: 'Production',
    components: {
      ProjectCard
    },
    data: () => ({
      projects: [
        {
          title: '테코브러리 (TECOBRARY)',
          logoSrc: '../_nuxt/static/tecobrary_logo.png',
          logoOutLine: false,
          contentLines: [
            '우아한 형제들이 주관하는 교육, 우아한테크코스 내부의 작은 도서관을 관리하기 위한 프로그램입니다.',
            '비치 중인 장서 검색, QR 코드 기반 대여, 반납, 희망도서 신청 등의 기능이 있습니다.'
          ],
          githubHref: 'https://github.com/milzipmoza-developers/tecobrary-wiki/wiki',
          useImgBtn: true,
          imgBtnHref: 'https://dgh7qtsxun9z8.cloudfront.net/',
          descPage: ''
        },
        {
          title: '테코비스 (TECORVIS)',
          logoSrc: '../_nuxt/static/tecorvis_logo.png',
          logoOutLine: true,
          contentLines:[
            '테코브러리의 희망도서 알림, 신착도서 알림을 위한 인간지능 슬랙 봇 입니다.',
            '\"주인님, 희망도서가 새로 도착하였습니다.\"'
          ],
          githubHref: 'https://github.com/milzipmoza-developers/tecobrary-noti-slackbot',
          useImgBtn: false,
          imgBtnHref: '',
          descPage: ''
        },
      ]
    })
  }
</script>

<style>
  div {
    font-family: 'Noto Sans KR', sans-serif;
  }

  .project-container {
    margin-top: 40px;
    background-color: black;
    height: 100%;
    width: auto;
    padding: 36px;
    padding-right: 20vw !important;
    padding-left: 20vw !important;
  }

  .project-title {
    margin-bottom: 24px;
    font-size: 70px;
    color: white;
    font-family: 'Do Hyeon', sans-serif !important;
  }

  .project-footer {
    color: white;
    margin-top: 48px;
    margin-bottom: 48px;
    line-height: 100px;
    text-align: center;
  }

  @media ( max-width: 1023px ) {

  }

  @media ( max-width: 767px ) {

  }
</style>


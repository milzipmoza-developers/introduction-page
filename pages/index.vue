<template>
  <full-page :options="options" ref="fullpage">
    <welcome-section/>
    <introduction-section/>
    <project-section/>
    <contributor-section/>
  </full-page>
</template>

<script>
import WelcomeSection from "./WelcomeSection";
import IntroductionSection from "./IntroductionSection";
import ProjectSection from "./ProjectSection";
import ContributorSection from "./ContributorSection"

export default {
  components: {
    WelcomeSection,
    IntroductionSection,
    ProjectSection,
    ContributorSection,
  },

  data: () => ({
    options: {
      licenseKey: 'OPEN-SOURCE-GPLV3-LICENSE',
      controlArrows: true,
      menu: "#menu",
      anchors: ["Welcome", "Introduction", "Product", "Contributor"],
      sectionsColor: ["#000000", "#000000", "#000000", "#000000"],
      lockAnchors: true,
      scrollBar: false,
      fitToSection: true,
      navigation: true,
      navigationPosition: 'right',
      navigationTooltips: ["Welcome", "Introduction", "Product", "Contributor"],
    },
  }),

  beforeCreate() {
    console.log('나는 개발왕이 될 루피다.')
    console.log('내 동료가 돼라 !')
    console.log('Welcome to Milzipmoza Developers')
    console.log(`
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@&&&@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@@,.(((((((((((((.,@@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@ ((((((((((((((((((((( @@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@ (( (((((((((((((((((((((( @@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@&(((/(.(/(((((((((((((((((( ((%@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@%((((((((((((((((((((((((((((.((#@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,&@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@ ********************************* @@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@***********************************@@@@@@@@@@@@@@@@
@@@@@ (((((((((((((((((((((((((((((((((((((((((((((((((((((((((((.@@@
@@@@@@@@@@@@@@@@@@%@@                             @@#@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@%@@                             @@#@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@%@@                             @@#@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@%@@                             @@#@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@%@@                             @@#@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@%@@        @@/,     ,*@@        @@#@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@%@@        *@   , ,  .@/        @@#@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@%@@            .% %,            @@#@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@%@@                             @@#@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@%@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@#@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@/////// ///////////////// ///////@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@/@@@@@@@@@@@@@@@@@@@,@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@#@@@@@@@@@@@@@@@@@@@@@/@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@&&&&&&&&&&&&&&&&&&&&&&&@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
    `)
  }
}
</script>

<style>

.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>


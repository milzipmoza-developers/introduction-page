<template>
  <client-only>
    <full-page :options="options" ref="fullpage">
      <welcome-section/>
      <introduction-section/>
      <project-section/>
      <contributor-section/>
      <footer-section/>
    </full-page>
  </client-only>
</template>

<script>
  import WelcomeSection from "../components/sections/WelcomeSection";
  import IntroductionSection from "../components/sections/IntroductionSection";
  import ProjectSection from "../components/sections/ProjectSection";
  import ContributorSection from "../components/sections/ContributorSection"
  import FooterSection from "../components/sections/FooterSection"

  export default {
    components: {
      WelcomeSection,
      IntroductionSection,
      ProjectSection,
      ContributorSection,
      FooterSection
    },

    data: () => ({
      options: {
        licenseKey: 'OPEN-SOURCE-GPLV3-LICENSE',
        controlArrows: true,
        menu: "#menu",
        anchors: ["Welcome", "Introduction", "Projects", "Members", "Footer"],
        sectionsColor: ["#000000", "#000000", "#000000", "#000000", "#FFFFFF"],
        lockAnchors: false,
        scrollBar: false,
        fitToSection: true,
        navigation: true,
        navigationPosition: 'right',
        navigationTooltips: ["Welcome", "Introduction", "Projects", "Members", ""],
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
</style>


<template>
  <div class="home">
    <app-home-intro :slides="slides"></app-home-intro>
    <app-home-services></app-home-services>
    <app-home-numbers></app-home-numbers>
    <app-home-why :partners="partners"></app-home-why>
    <app-home-consult></app-home-consult>
    <app-home-activities :activities="activities" />
    <app-home-steps :steps="steps" />
    <app-home-team :teams="teams"></app-home-team>
    <app-home-contact></app-home-contact>
  </div>
</template>

<script>
import AppHomeConsult from "../components/home/AppHomeConsult.vue";
import AppHomeContact from "../components/home/AppHomeContact.vue";
import AppHomeIntro from "../components/home/AppHomeIntro.vue";
import AppHomeNumbers from "../components/home/AppHomeNumbers.vue";
import AppHomeServices from "../components/home/AppHomeServices.vue";
import AppHomeTeam from "../components/home/AppHomeTeam.vue";
import AppHomeWhy from "../components/home/AppHomeWhy.vue";
import AppHomeActivities from "../components/home/AppHomeActivities.vue";
import AppHomeSteps from "../components/home/AppHomeSteps.vue";

export default {
  name: "Home",
  components: {
    AppHomeIntro,
    AppHomeServices,
    AppHomeNumbers,
    AppHomeWhy,
    AppHomeConsult,
    AppHomeTeam,
    AppHomeContact,
    AppHomeActivities,
    AppHomeSteps,
  },
  async asyncData({ $axios, app }) {
    const slides = await $axios.get("/sliders", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const teams = await $axios.get("/teams");

    const partners = await $axios.get("/partners");

    const activities = await $axios.get("/sections/activities", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    const steps = await $axios.get("/sections/steps", {
      headers: {
        "Accept-Language": app.i18n.locale,
      },
    });

    return {
      slides: slides.data.data.sliders,
      teams: teams.data.data.teams,
      partners: partners.data.data.partners,
      activities: activities.data.data,
      steps: steps.data.data,
    };
  },
};
</script>

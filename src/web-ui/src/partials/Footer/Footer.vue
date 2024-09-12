<template>
  <footer>
    <div class="justify-content-center d-flex align-items-center">
      <div class="rds">Retail Demo Store</div>
      <div class="separator mx-2" aria-hidden></div>
      <!-- <PoweredByAWS class="img"></PoweredByAWS> -->
      <span class="d-flex justify-content-center align-items-center">
        <p class="powered-by-text">powered by</p>
        <img src="/aaic.png" class="powered-by-img" />
      </span>
    </div>

    <TermsAndConditions></TermsAndConditions>
  </footer>
</template>

<script>
import PoweredByAWS from "@/components/PoweredByAWS/PoweredByAWS.vue";
import TermsAndConditions from "@/partials/TermsAndConditions/TermsAndConditions.vue";

export default {
  name: "Footer",
  components: { PoweredByAWS, TermsAndConditions },
};
</script>

<style scoped>
.rds {
  font-weight: bold;
}

.separator {
  height: 30px;
  width: 2px;
  background: var(--grey-600);
}

.img {
  /* fine-tuning to match other copy in footer */
  margin-top: 10px;
  height: 30px;
}

.powered-by-img {
  height: 48px;
  margin-left: -10px;
}

.powered-by-text {
  margin: 0;
  font-size: 1.2rem;
  font-weight: 500;
}

@media (min-width: 576px) {
  .rds {
    font-size: 1.2rem;
  }

  .separator {
    height: 40px;
  }

  .img {
    margin-top: 14px;
    height: 40px;
  }
}
</style>

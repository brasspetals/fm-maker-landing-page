<script>
  import PlanCard from '../PlanCard.svelte'
  import { pricingPlans }  from '../../../scripts/pricingPlans'
</script>

<section class="pricing">
  <div class="heading">
    <h2>Our pricing plans</h2>
    <p>We only make money when our creators make money. Our plans are always affordable, and it’s completely free to get started.</p>
  </div>
  <div class="plans">
    {#each pricingPlans as plan}
      <PlanCard plan={plan}/>
    {/each}
  </div>
</section>

<style>
  .pricing {
    display: grid;
    justify-items: center;
    text-align: center;
    padding: 72px 24px;
    gap: 56px;
  }

  h2 {
    font-size: 24px;
    margin-bottom: 26px;
  }

  p {
    max-width: 40ch;
  }

  .plans {
    display: grid;
    gap: 64px;
    text-align: left;
  }

  @media screen and (min-width: 700px) {
    .pricing {
      padding: 85px 24px;
      gap: 55px;
    }

    p {
      max-width: 60ch;
    }

    .plans {
      gap: 66px;
    }
  }
</style>
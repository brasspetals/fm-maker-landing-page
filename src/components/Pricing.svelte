<script>
  import PlanCard from './PlanCard.svelte'
  import { pricingPlans }  from '../../scripts/pricingPlans'
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

  .heading {
    max-width: 40ch;
  }

  h2 {
    font-size: 24px;
    margin-bottom: 27px;
  }

  .plans {
    display: grid;
    gap: 67px;
    text-align: left;
  }
</style>
<script>
  import PlanCard from '../PlanCard.svelte'
  import { pricingPlans }  from '../../../scripts/pricingPlans'
  import IntersectionObserver from 'svelte-intersection-observer'

  let element
  let intersecting
</script>

<IntersectionObserver {element} once bind:intersecting threshold={0.2}>
  <section class="pricing">
    <div class="heading {intersecting ? 'intersecting' : 'hidden'}" bind:this={element}>
      <h2>Our pricing plans</h2>
      <p>We only make money when our creators make money. Our plans are always affordable, and it’s completely free to get started.</p>
    </div>
    <div class="plans">
      {#each pricingPlans as plan}
        <PlanCard plan={plan}/>
      {/each}
    </div>
  </section>
</IntersectionObserver>

<style>
  .pricing {
    display: grid;
    justify-items: center;
    text-align: center;
    padding: 4.5rem 1.5rem;
    gap: 3.5rem;
  }

  h2 {
    margin-bottom: 1.625rem;
  }

  p {
    max-width: 40ch;
  }

  .plans {
    display: grid;
    gap: 4rem;
    text-align: left;
  }

  @media screen and (min-width: 700px) {
    .pricing {
      padding: 5.3125rem 1.5rem;
      gap: 3.4375rem;
    }

    p {
      max-width: 60ch;
    }

    .plans {
      gap: 4.125rem;
    }
  }

  @media screen and (min-width: 1200px) {
    .pricing {
      padding: 6.28125rem 0 6.375rem;
      gap: 6.5625rem;
    }

    h2 {
      margin-bottom: 1.5rem;
    }

    .plans {
      grid-auto-flow: column;
      gap: 1.875rem;
      align-items: center;
    }
  }
</style>
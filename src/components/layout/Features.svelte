<script>
  import Feature from '../FeatureCard.svelte'
  import { features }  from '../../../scripts/features'
</script>

<section class="features">
  <h2 class="sr-only">Benefits of joining</h2>
  <div class="feature-container">
    {#each features as feature}
      <Feature feature={feature}/>
    {/each}
  </div>
</section>

<style>
  .features {
    text-align: center;
    padding: 4.5rem 1.5rem;
  }

  .feature-container {
    display: grid;
    justify-items: center;
    gap: 3.5rem;
  }

  @media screen and (min-width: 700px) {
    .features {
      text-align: left;
      padding: 3.5rem 1.5rem;
    }

    .feature-container {
      justify-items: left;
      max-width: 35.875rem;
      margin: 0 auto;
      gap: 2.46875rem;
    }

    :global(.feature-container > :nth-child(odd)) {
      margin-left: 3.625rem;
    }
  }

  @media screen and (min-width: 1200px) {
    .features {
      padding: 5.90625rem 0 6.28125rem;
    }

    .feature-container {
      max-width: 69.375rem;
      grid-auto-flow: column;
      align-items: start;
      gap: 1.875rem;
    }

    :global(.feature-container > :nth-child(odd)) {
      margin-left: unset;
    }

    :global(.feature-container > :nth-child(even)) {
      margin-top: 3rem;
    }
  }
</style>
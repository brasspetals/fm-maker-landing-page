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
    padding: 72px 24px;
  }

  .feature-container {
    display: grid;
    justify-items: center;
    gap: 56px;
  }
</style>
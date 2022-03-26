<script>
  import Feature from './FeatureCard.svelte'
</script>

<div class="features">
  <Feature src="/images/illustration-passions.svg" heading="Indulge your passions" description="Your passions shouldn't be just for the weekend. Earn a living doing what you love." passions=true/> 
  <Feature src="/images/illustration-financial-freedom.svg" heading="Gain financial freedom" description="Start making money work for you. There’s nothing quite like earning while you sleep."/> 
  <Feature src="/images/illustration-lifestyle.svg" heading="Choose your lifestyle" description="Own your daily schedule. Fancy a lie-in? Go for it! Take charge of your week."/> 
  <Feature src="/images/illustration-work-anywhere.svg" heading="Work from anywhere" description="Selling online means not being pinned down. Want to work AND travel? Go for it!"/> 
</div>

<style>
  .features {
    display: grid;
    justify-items: center;
    text-align: center;
    padding: 72px 24px;
    gap: 56px;
  }
</style>
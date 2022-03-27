<script>
  import ListItem from './ListItem.svelte'
</script>

<section class="pricing">
  <div class="heading">
    <h2>Our pricing plans</h2>
    <p>We only make money when our creators make money. Our plans are always affordable, and it’s completely free to get started.</p>
  </div>
  <div class="plans">
    <div class="plan odd">
      <div class="plan-heading">
        <h3>Dip your toe</h3>
        <p>Just getting started? No problem at all! Our free plan will take you a long way.</p>
      </div>
      <div class="plan-cost">
        <h4>Free</h4>
      </div>
      <ul class="plan-features">
        <ListItem liText="Unlimited products" odd=true/>
        <ListItem liText="Basic analytics" odd=true/>
        <ListItem liText="Limited marketplace exposure" odd=true/>
        <ListItem liText="10% fee per transaction" odd=true/>
      </ul>
    </div>
    <div class="plan even">
      <div class="plan-heading">
        <h3>Dive right in</h3>
        <p>Ready for the big time? Our paid plan will help you take your business to the next level.</p>
      </div>
      <div class="plan-cost">
        <h4>$25.00</h4>
        <p>/ month</p>
      </div>
      <ul class="plan-features">
        <ListItem liText="Custom domain"/>
        <ListItem liText="Advanced analytics and reports"/>
        <ListItem liText="High marketplace visibility"/>
        <ListItem liText="5% fee per transaction"/>
      </ul>
    </div>
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

  .plan {
    border-radius: 8px;
    max-width: 445px;
    position: relative;
  }

  .odd {
    background-color: var(--color-blue);
    color: var(--color-white);
    margin-top: 24px;
    padding: 46px 30px 30px;
  }

  .odd::before {
    content: url('/images/icon-free.svg');
    position: absolute;
    left: 30px;
    top: -24px;
  }

  .even {
    background-color: var(--color-cyan);
    color: var(--color-bg);
    padding: 60px 30px 30px;
  }

  .even::before {
    content: url('/images/icon-paid.svg');
    position: absolute;
    left: 37px;
    top: -33px;
  }

  .even h3, .even h4 {
    color: var(--color-bg);
  }

  .plan-heading {
    margin-bottom: 26px;
  }

  h3 {
    font-size: 18px;
    line-height: 1.3889;
    margin-bottom: 20px;
  }

  .plan-heading p {
    opacity: 0.6;
  }

  .plan-cost {
    display: grid;
    grid-auto-flow: column;
    align-items: center;
    justify-content: start;
    gap: 9px;
    font-size: 40px;
  }

  ul {
    display: grid;
    margin-top: 19px;
    gap: 12px;
  }
</style>
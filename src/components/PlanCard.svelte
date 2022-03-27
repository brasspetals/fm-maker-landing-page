<script>
  import ListItem from './ListItem.svelte'
  export let plan
</script>

  <div class="plan {plan.color}">
    <div class="plan-heading">
      <h3>{plan.header}</h3>
      <p>{plan.description}</p>
    </div>
    <div class="plan-cost">
      <h4>{plan.cost}</h4>
      <p>{plan.frequency}</p>
    </div>
    <ul class="plan-features">
      {#each plan.lis as li}
        <ListItem text={li} blue={plan.blue}/>
      {/each}
    </ul>
  </div>

<style>
  .plan {
    border-radius: 8px;
    max-width: 445px;
    position: relative;
  }

  .blue {
    background-color: var(--color-blue);
    color: var(--color-white);
    margin-top: 24px;
    padding: 46px 30px 30px;
  }

  .blue::before {
    content: url('/images/icon-free.svg');
    position: absolute;
    left: 30px;
    top: -24px;
  }

  .cyan {
    background-color: var(--color-cyan);
    color: var(--color-bg);
    padding: 60px 30px 30px;
  }

  .cyan::before {
    content: url('/images/icon-paid.svg');
    position: absolute;
    left: 37px;
    top: -33px;
  }

  .cyan h3, .cyan h4 {
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
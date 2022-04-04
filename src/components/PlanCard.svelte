<script>
  import ListItem from './ListItem.svelte'
  import IntersectionObserver from 'svelte-intersection-observer'

  let element
  let intersecting
  export let plan
</script>

<IntersectionObserver {element} once bind:intersecting threshold={0.1}>
  <div class="plan {plan.color} {intersecting ? 'intersecting' : 'hidden'}" bind:this={element}>
    <div class="plan-heading">
      <h3>{plan.header}</h3>
      <p>{plan.description}</p>
    </div>
    <div class="plan-cost">
      <p class="cost">{plan.cost}</p>
      <p>{plan.frequency}</p>
    </div>
    <ul class="plan-features">
      {#each plan.lis as li}
        <ListItem text={li} blue={plan.blue}/>
      {/each}
    </ul>
  </div>
</IntersectionObserver>

<style>
  .plan {
    border-radius: .5rem;
    max-width: 27.8125rem;
    position: relative;
  }

  .blue {
    background-color: var(--color-blue);
    color: var(--color-white);
    margin-top: 1.5rem;
    padding: 3rem 1.875rem 2rem;
  }

  .blue::before {
    content: url('/images/icon-free.svg');
    position: absolute;
    left: 1.875rem;
    top: -1.4325rem;
  }

  .cyan {
    background-color: var(--color-cyan);
    color: var(--color-bg);
    padding: 3.75rem 1.875rem 2.125rem;
  }

  .cyan::before {
    content: url('/images/icon-paid.svg');
    position: absolute;
    left: 2.3125rem;
    top: -2.0625rem;
  }

  .cyan h3 {
    color: var(--color-bg);
  }

  .plan-heading {
    margin-bottom: 1.3125rem;
  }

  h3 {
    font-size: 1.125rem;
    line-height: 1.3889;
    margin-bottom: 1.25rem;
  }

  .plan-heading p {
    opacity: 0.6;
  }

  .plan-cost {
    display: grid;
    grid-auto-flow: column;
    align-items: center;
    justify-content: start;
    gap: .5625rem;
    
  }

  .cost {
    font-size: 2.5rem;
    font-weight: 800;
  }

  ul {
    display: grid;
    margin-top: .75rem;
    gap: .75rem;
  }

  @media screen and (min-width: 700px) {
    .plan-heading {
      margin-bottom: 1.125rem;
    }

    .blue {
      padding: 3rem 2.375rem;
    }

    .blue::before {
      left: 2.375rem;
    }

    .cyan {
      padding: 3.75rem 2.375rem;
    }
  }

  @media screen and (min-width: 1200px) {
    .blue {
      margin-top: 0;
    }
  }
</style>
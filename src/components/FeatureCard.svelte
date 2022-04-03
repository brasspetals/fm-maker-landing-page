<script>
  export let feature
</script>

<div class="feature">
  <div class="feature-img">
    <img src="{feature.src}" alt="" class:passions={feature.passions}>
  </div>
  <div class="feature-text">
    <h3>{feature.heading}</h3>
    <p>{feature.description} </p>
  </div>
</div>

<style>
  .feature {
    display: grid;
    justify-items: center;
    gap: 2rem;
  }

  .feature-img {
    background-color: var(--color-blue);
    height: 7.75rem;
    width: 7.5rem;
    border-radius: 2.8125rem;
    display: grid;
    align-items: center;
    justify-content: center;
    justify-items: center;
  }

  .feature-img img {
    width: 75%;
  }

  .passions {
    transform: translateX(0.25rem);
  }

  h3 {
    font-size: 1.125rem;
    line-height: 1.366;
    margin-bottom: 0.6875rem;
  }

  p {
    max-width: 38ch;
  }

  @media screen and (min-width: 700px) {
    .feature {
      grid-auto-flow: column;
      gap: 3.4375rem;
      align-items: center;
    }

    p {
      max-width: 36.5ch;
    }
  }

  @media screen and (min-width: 1200px) {
    .feature {
      grid-auto-flow: row;
      gap: 3rem;
      justify-items: left;
    }

    .feature-img {
      height: 10.25rem;
      width: 10rem;
    }

    .feature-img img {
      width: 100%;
    }

    h3 {
      margin-bottom: 1.5rem;
    }

    p {
      max-width: 27ch;
    }
  }
</style>
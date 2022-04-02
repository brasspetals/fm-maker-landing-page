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
    gap: 32px;
  }

  .feature-img {
    background-color: var(--color-blue);
    height: 124px;
    width: 120px;
    border-radius: 45px;
    display: grid;
    align-items: center;
    justify-content: center;
    justify-items: center;
  }

  .feature-img img {
    width: 75%;
  }

  .passions {
    transform: translateX(4px);
  }

  h3 {
    font-size: 18px;
    line-height: 1.366;
    margin-bottom: 11px;
  }

  p {
    max-width: 38ch;
  }

  @media screen and (min-width: 700px) {
    .feature {
      grid-auto-flow: column;
      gap: 55px;
      align-items: center;
    }

    p {
      max-width: 36.5ch;
    }
  }
</style>
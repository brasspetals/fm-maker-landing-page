<script>

</script>

<header>
  <div class="logo">
    <a href="/"><img src="/images/logo.svg" alt="Maker - Home"></a>
  </div>
  <div class="hero">
    <h1>Get paid for the work you <span>love</span> to do.</h1>
    <p>The 9-5 grind is so last century. We believe in living life on your own terms. Whether you’re looking to escape the rat race or set up a side hustle, we’ve got you covered.</p>
  </div>
</header>

<style>
  header {
    display: grid;
    justify-items: center;
    position: relative;
    padding: 40px 0 146px;
  }

  .hero {
    background-image: url('/images/illustration-hero-mobile.png');
    background-position-y: 60px;
    background-position-x: center;
    background-repeat: no-repeat;
    background-size: 410px 233px;
    padding: 342px 24px 0;
    text-align: center;
    overflow: hidden;
    display: grid;
    justify-items: center;
    gap: 24px;
  }

  h1 {
    font-size: 32px;
    line-height: 1.25;
    padding: 0 38px;
    max-width: 20ch;
  }

  span {
    color: var(--color-cyan);
  }

  p {
    max-width: 42ch;
  }

  header::after {
    content: url('/images/icon-scroll.svg');
    position: absolute;
    bottom: 67px;
    left: 50%;
    transform: translateX(-50%);
  }
</style>
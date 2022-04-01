<script>

</script>

<header>
  <div class="logo">
    <a href="/"><img src="/images/logo.svg" alt="Maker - Home"></a>
  </div>
  <div class="hero">
    <div class="hero-img-1">
      <img src="/images/illustration-hero-mobile.png" alt="">
    </div>
    <div class="hero-text">
      <h1>Get paid for the work you <span>love</span> to do.</h1>
      <p>The 9-5 grind is so last century. We believe in living life on your own terms. Whether you’re looking to escape the rat race or set up a side hustle, we’ve got you covered.</p>
    </div>
    <div class="hero-img-2"></div>
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
    padding-top: 60px;
    text-align: center;
    overflow: hidden;
    display: grid;
    justify-items: center;
    gap: 48px;
  }

  .hero img {
    display: block;
    width: 109%;
    max-width: 650px;
  }

  .hero-text {
    padding: 0 24px;
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

  .hero-img-2 {
    display: none;
  }

  header::after {
    content: url('/images/icon-scroll.svg');
    position: absolute;
    bottom: 67px;
    left: 50%;
    transform: translateX(-50%);
  }
</style>
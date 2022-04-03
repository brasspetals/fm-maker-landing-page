<script>

</script>

<header>
  <div class="logo">
    <a href="/"><img src="/images/logo.svg" alt="Maker - Home"></a>
  </div>
  <div class="hero">
    <img class="hero-image-mobile" src="/images/illustration-hero-mobile.png" alt="">
    <div class="hero-text">
      <h1>Get paid for the work you <span>love</span> to do.</h1>
      <p>The 9-5 grind is so last century. We believe in living life on your own terms. Whether you’re looking to escape the rat race or set up a side hustle, we’ve got you covered.</p>
      <img class="scroll" src="/images/icon-scroll.svg" alt="">
    </div>
  </div>
</header>

<style>
  header {
    display: grid;
    justify-items: center;
    position: relative;
    padding: 2.5rem 0 4.5rem;
    overflow-x: hidden;
  }

  .hero {
    padding-top: 3.75rem;
    text-align: center;
    display: grid;
    justify-items: center;
    gap: 3rem;
  }

  .hero-image-mobile {
    display: block;
    width: 109%;
    max-width: 37.5rem;
    transform: translateX(1.0625rem);
  }

  .hero-text {
    padding: 0 1.5rem;
    display: grid;
    justify-items: center;
    gap: 1.5rem;
  }

  h1 {
    font-size: 2rem;
    line-height: 1.25;
    padding: 0 2.375rem;
    max-width: 20ch;
  }

  span {
    color: var(--color-cyan);
  }

  p {
    max-width: 48ch;
  }

  .scroll {
    margin-top: 8px;
  }

  @media screen and (min-width: 700px) {
    header {
      padding: 3rem 0 52px;
    }

    .logo {
      margin-left: 39px;
      justify-self: left;
    }

    .hero {
      padding-top: 4.5rem;
      align-items: start;
      position: relative;
      width: 100%;
    }

    .hero-image-mobile {
      display: none;
    }

    .hero-text::before {
      content: '';
      background-image: url('/images/illustration-hero-left.svg');
      background-size: 314px auto;
      background-repeat: no-repeat;
      height: 357px;
      width: 314px;
      position: absolute;
      left: 50%;
      transform: translateX(-176%);
      top: 75px;
    }

    .hero-text {
      padding: 52px 0;
      background-image: url('/images/bg-hero-squiggle.svg');
      background-size: 86%;
      background-repeat: no-repeat;
      background-position-x: center;
      background-position-y: 33px;
    }

    .hero-text::after {
      content: '';
      background-image: url('/images/illustration-hero-right.svg');
      background-size: 317px auto;
      background-repeat: no-repeat;
      height: 357px;
      width: 317px;
      position: absolute;
      left: 50%;
      transform: translateX(75%);
      top: 73px;
    }
  }

  @media screen and (min-width: 1200px) {
    header {
      padding: 81px 0 94.5px;
      margin: 0 auto;
      max-width: 1554px;
    }

    .logo {
      width: 100%;
      max-width: 1110px;
      margin: 0 auto;
    }

    .hero {
      padding-top: 97px;
      width: 100%;
      overflow: hidden;
    }

    .hero-text::before {
      background-size: 408px auto;
      height: 459px;
      width: 408px;
      transform: translateX(-189.5%);
      top: 108px;
    }

    .hero-text {
      padding: 83px 0;
      background-size: contain;
      background-position-y: top;
      max-width: 544px;
    }

    h1 {
      font-size: 3rem;
      line-height: 1.1667;
      padding: 0;
      max-width: 18ch;
    }

    p {
      max-width: 58ch;
    }

    .scroll {
      margin-top: 41px;
    }

    .hero-text::after {
      background-size: 396px auto;
      height: 444px;
      width: 396px;
      transform: translateX(97%);
      top: 117px;
    }
  }
</style>
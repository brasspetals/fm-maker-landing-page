<script>
  import Mouse from '../Mouse.svelte'

  const mediaQuery = window.matchMedia('(prefers-reduced-motion: reduce)')
  const reducedMotion = mediaQuery.matches
 
  let userAgentString = navigator.userAgent;
  let chromeAgent = userAgentString.indexOf("Chrome") > -1;
  let safariAgent = userAgentString.indexOf("Safari") > -1;
  if ((chromeAgent) && (safariAgent)) safariAgent = false;
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
    <div class="scroll">
      {#if reducedMotion || safariAgent}
        <img src="/images/icon-scroll.svg" alt="">
      {:else}
        <Mouse/>
      {/if}
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

  .logo {
    animation: fadeUp 1s ease backwards;
  }

  .hero {
    padding-top: 3.75rem;
    text-align: center;
    display: grid;
    justify-items: center;
    gap: 3rem;
    animation: fadeUp 1s ease backwards;
    animation-delay: .3s;
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
    animation: fadeUpTxt 1s ease backwards;
    animation-delay: .3s;
  }

  span {
    color: var(--color-cyan);
  }

  p {
    max-width: 48ch;
    animation: fadeUpTxt 1s ease backwards;
    animation-delay: .5s;
  }

  .scroll {
    margin-top: 0.5rem;
    animation: fadeUpTxt 1s ease backwards;
    animation-delay: .8s;
  }

  @media screen and (min-width: 700px) {
    header {
      padding: 3rem 0 3.25rem;
    }

    .logo {
      margin-left: 2.4375rem;
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
      background-size: 19.625rem auto;
      background-repeat: no-repeat;
      height: 22.3125rem;
      width: 19.625rem;
      position: absolute;
      left: 50%;
      transform: translateX(-176%);
      top: 4.6875rem;
    }

    .hero-text {
      padding: 3.25rem 0;
      background-image: url('/images/bg-hero-squiggle.svg');
      background-size: 86%;
      background-repeat: no-repeat;
      background-position-x: center;
      background-position-y: 2.0625rem;
    }

    .hero-text::after {
      content: '';
      background-image: url('/images/illustration-hero-right.svg');
      background-size: 19.8125rem auto;
      background-repeat: no-repeat;
      height: 22.3125rem;
      width: 19.8125rem;
      position: absolute;
      left: 50%;
      transform: translateX(75%);
      top: 4.5625rem;
    }
  }

  @media screen and (min-width: 1200px) {
    header {
      padding: 5.0625rem 0 5.9063rem;
      margin: 0 auto;
      max-width: 97.125rem;
    }

    .logo {
      width: 100%;
      max-width: 69.375rem;
      margin: 0 auto;
    }

    .hero {
      padding-top: 6.0625rem;
      width: 100%;
      overflow: hidden;
    }

    .hero-text::before {
      background-size: 25.5rem auto;
      height: 28.6875rem;
      width: 25.5rem;
      transform: translateX(-189.5%);
      top: 6.75rem;
    }

    .hero-text {
      padding: 5.1875rem 0;
      background-size: contain;
      background-position-y: top;
      max-width: 34rem;
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
      margin-top: 2.5625rem;
    }

    .hero-text::after {
      background-size: 24.75rem auto;
      height: 27.75rem;
      width: 24.75rem;
      transform: translateX(97%);
      top: 7.3125rem;
    }
  }
</style>
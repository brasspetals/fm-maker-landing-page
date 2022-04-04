<script></script>

<div class="mouse"></div>

<style>
  .mouse {
    background: var(--color-cyan-fade)
    linear-gradient(
      transparent 0%,
      transparent 50%,
      var(--color-cyan) 50%,
      var(--color-cyan) 100%
    );
    position: relative;
    width: 1.625rem;
    height: 2.625rem;
    border-radius: 6.25rem;
    background-size: 100% 200%;
    animation: colorSlide 2.5s linear infinite backwards, nudgeMouse 2.5s ease-out infinite backwards;
    animation-delay: 1.9s;
  }

  .mouse::before,
  .mouse::after {
    content: "";
    position: absolute;
    top: 0; right: 0; bottom: 0; left: 0;
    margin: auto;
  }

  .mouse::before {
    width: 1.375rem;
    height: 2.375rem;
    background-color: var(--color-bg);
    border-radius: 6.25rem;
  }

  .mouse::after {
    background-color: var(--color-cyan);
    width: 0.25rem;
    height: 0.25rem;
    border-radius: 100%;
    top: 0.8125rem;
    animation: trackBallSlide 2.5s linear infinite backwards;
    animation-delay: 1.9s;
  }

  @keyframes colorSlide { 
    0% { 
      background-color: var(--color-cyan-fade);
      background-position: 0% 100%;
    }
    70% { background-position: 0% 0%; }
    81% { background-color: var(--color-cyan-fade); }
    90%, 100% { background-color: var(--color-cyan); }
  }

  @keyframes trackBallSlide {
    0% {
      opacity: 1;
      transform: scale(1) translateY(-0.8125rem);
    }
    46% { 
      opacity: 1;
      transform: scale(0.9) translateY(0.8125rem/4);
    }
    70% {
      opacity: 0;
      transform: scale(.5) translateY(0.8125rem*2);
    }
    71% {
      opacity: 0;
      transform: scale(.5) translateY(-0.8125rem);
    }
    90%, 100% {
      opacity: 1;
      transform: scale(1) translateY(-0.8125rem);
    }
  }

  @keyframes nudgeMouse {
    0% { transform: translateY(0); }
    70% { transform: translateY(0.3125rem); }
    100% { transform: translateY(0); }
  }
</style>
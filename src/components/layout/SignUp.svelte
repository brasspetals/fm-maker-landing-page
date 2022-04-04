<script>
  import EmailForm from '../EmailForm.svelte'
  import IntersectionObserver from 'svelte-intersection-observer'

  let element
  let intersecting
</script>

<IntersectionObserver {element} once bind:intersecting threshold={0.3}>
  <section class="signup {intersecting ? 'fade' : 'hidden'}" bind:this={element}>
    <h2 class="{intersecting ? 'intersecting' : 'hidden'}">Get notified when we launch</h2>
    <EmailForm/>
  </section>
</IntersectionObserver>

<style>
  .signup {
    background-image: url('/images/bg-footer-squiggle.svg');
    background-size: 156%;
    background-position-x: -6.5625rem;
    background-position-y: 4.5rem;
    background-repeat: no-repeat;
    display: grid;
    justify-items: center;
    text-align: center;
    padding: 4.5rem 1.5rem 9rem;
  }

  h2 {
    padding: 0 2.5rem;
    margin-bottom: 1.9375rem;
  }

  @media screen and (min-width: 700px) {
    .signup {
      padding: 3.25rem 1.5rem 9rem;
      background-size: 133%;
      background-position-x: -14.9375rem;
      background-position-y: 2.3125rem;
    }
    
    h2 {
      margin-bottom: 1.75rem;
    }
  }

  @media screen and (min-width: 1200px) {
    .signup {
      max-width: 97.125rem;
      margin: 0 auto;
      padding: 6.375rem 0 10rem;
      background-size: 115.5%;
      background-position-x: right;
      background-position-y: 3.125rem;
    }
    
    h2 {
      margin-bottom: 2.625rem;
    }
  }
</style>
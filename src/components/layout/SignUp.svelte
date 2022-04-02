<script>
  import EmailForm from '../EmailForm.svelte'
</script>

<section class="signup">
    <h2>Get notified when we launch</h2>
    <EmailForm/>
</section>

<style>
  .signup {
    background-image: url('/images/bg-footer-squiggle.svg');
    background-size: 156%;
    background-position-x: 50%;
    background-position-y: 72px;
    background-repeat: no-repeat;
    display: grid;
    justify-items: center;
    text-align: center;
    padding: 72px 24px;
  }

  h2 {
    padding: 0 40px;
    margin-bottom: 31px;
  }

  @media screen and (min-width: 700px) {
    .signup {
      padding: 52px 24px;
      background-size: 1022px;
      background-position-x: 94%;
      background-position-y: 35px;
    }
    
    h2 {
      margin-bottom: 28px;
    }

  }
</style>
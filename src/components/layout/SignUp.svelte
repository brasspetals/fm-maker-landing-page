<script>
  import EmailForm from '../EmailForm.svelte'
</script>

<section class="signup">
  <div class="contianer">
    <h2>Get notified when we launch</h2>
    <EmailForm/>
  </div>
</section>

<style>
  .signup {
    background-image: url('/images/bg-footer-squiggle.svg');
    background-size: 156%;
    background-position-x: 50%;
    background-position-y: 74px;
    background-repeat: no-repeat;
    display: grid;
    justify-items: center;
    text-align: center;
    padding: 75px 24px;
  }

  h2 {
    padding: 0 40px;
    margin-bottom: 31px;
  }
</style>
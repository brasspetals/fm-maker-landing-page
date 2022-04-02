<script>
  import { fade, fly } from 'svelte/transition';
  import Button from './Button.svelte'
  
  let value;
  let error = '';
  let invalid = false;
  const emailRegex = /^[a-zA-Z][a-zA-Z0-9\-\_\.]+@[a-zA-Z0-9]{2,}\.[a-zA-Z0-9]{2,}$/;

  const validate = () => {
    invalid = true
    
    if (value == "" || value == undefined) {
      error = "Oops! Please add your email"
    } else if (!value.match(emailRegex)) {
      error = "Oops! That doesn’t look like an email address"
    } else {
      error = ""
      value = ""
      invalid = false
      form.reset()
    }
  }
</script>

<form novalidate id="form" on:submit|preventDefault={validate}>
  <input type="email" name="email" class:invalid={invalid} id="email" placeholder="Email address" aria-label="Email address" aria-invalid={invalid} aria-describedby="error" bind:value={value}>
  {#if invalid}
    <p id="error" aria-live="polite" transition:fade="{{ duration: 300 }}">{error}</p>
  {/if}
  <Button type="submit" text="Get notified"/>
</form>

<style>
  form {
    position: relative;
    width: 100%;
    max-width: 400px;
    display: grid;
    gap: 24px;
  }

  input {
    background-color: var(--color-blue);
    color: var(--color-white);
    font-size: 15px;
    line-height: 1.667;
    font-weight: 800;
    border: 2px solid var(--color-blue);
    border-radius: 24px;
    height: 48px;
    padding: 0 16px;
    transition: all .4s ease;
  }

  input:focus-visible {
    border: 2px solid var(--color-cyan);
  }

  .invalid, .invalid:focus-visible {
    border: 2px solid var(--color-red);
  }

  #error {
    font-size: 12px;
    color: var(--color-red);
    position: absolute;
    top: -22px;
    left: 16px;
  }

  @media screen and (min-width: 550px) {
    form {
      grid-auto-flow: column;
      grid-template-columns: 1fr auto;
      gap: 18px;
      max-width: 476px;
    }
  }
</style>
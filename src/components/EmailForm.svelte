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
    max-width: 25rem;
    display: grid;
    gap: 1.5rem;
  }

  input {
    background-color: var(--color-blue);
    color: var(--color-white);
    font-size: .9375rem;
    line-height: 1.667;
    font-weight: 800;
    border: .125rem solid var(--color-blue);
    border-radius: 1.5rem;
    height: 3rem;
    padding: 0 1rem;
    transition: all .4s ease;
  }

  input:focus-visible {
    border: .125rem solid var(--color-cyan);
  }

  .invalid, .invalid:focus-visible {
    border: .125rem solid var(--color-red);
  }

  #error {
    font-size: 0.75rem;
    color: var(--color-red);
    position: absolute;
    top: -1.375rem;
    left: 1.125rem;
  }

  @media screen and (min-width: 550px) {
    form {
      grid-auto-flow: column;
      grid-template-columns: 1fr auto;
      gap: 1rem;
      max-width: 29.75rem;
    }

    #error {
      top: unset;
      bottom: -1.625rem;
    }
  }
</style>
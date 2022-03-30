<script>
  export let type="email"
  export let placeholder="Email address"
  export let name="email"
  export let id="email"
  export let ariaLabel="email address"
  export let ariaDescribedBy="error success"
</script>

<input type="{type}" placeholder="{placeholder}" aria-label="{ariaLabel}" aria-describedby="{ariaDescribedBy}" id="{id}" name="{name}" required>

<style>
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
</style>
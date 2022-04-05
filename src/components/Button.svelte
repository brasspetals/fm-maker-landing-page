<script>
  export let type
  export let text
</script>

<button type="{type}">{text}</button>

<style>
  button {
    background-color: var(--color-cyan);
    color: var(--color-blue);
    font-weight: 800;
    font-size: .9375rem;
    line-height: 1.667;
    cursor: pointer;
    border: .125rem solid var(--color-cyan);
    border-radius: 1.5rem;
    height: 3rem;
    padding: 0 1.5rem;
    transition-property: color, border, background-color;
    transition-duration: .4s;
    transition-timing-function: ease;
  }

  button:focus-visible {
    outline: 0.125rem dashed var(--color-cyan);
    outline-offset: 0.3125rem;
  }

  button:hover {
    background-color: var(--color-bg);
    color: var(--color-white);
  }
</style>
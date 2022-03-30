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
    font-size: 15px;
    line-height: 1.667;
    cursor: pointer;
    border: 2px solid var(--color-cyan);
    border-radius: 24px;
    height: 48px;
    padding: 0 24px;
    transition: all .4s ease;
  }

  button:hover {
    background-color: var(--color-bg);
    color: var(--color-white);
  }
</style>
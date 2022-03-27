<script>
  export let liText
  export let odd = false
</script>

<li>
  <svg xmlns="http://www.w3.org/2000/svg" width="12" height="9"><path class={odd && 'blue'} fill="#093F68" d="M10.319.768l1.363 1.464-7.128 6.634L.319 4.924 1.682 3.46l2.871 2.674z"/></svg> {liText}
</li>

<style>
  
  li svg {
    margin-right: 11px;
  }

  .blue {
    fill: var(--color-cyan);
  }

</style>
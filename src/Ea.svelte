<script lang="ts">
  import FaExternalLinkAlt from "svelte-icons/fa/FaExternalLinkAlt.svelte";
  export let text: string;
  export let href: string;
</script>

<a {href} target="_blank">
  {#if text}
    {text} 
  {/if}
  <div class="icon"><FaExternalLinkAlt /></div>
</a>

<style>
  a {
      text-decoration-color: none;
      text-decoration-line: none;
      text-decoration-style: none;
      border-bottom-style: solid;
      border-bottom-width: 1px;
      border-bottom-color: lightgray;
  }

  a:hover {
      cursor: pointer;
      border-bottom-width: 2px;
  }

  .icon {
      display: inline-block;
      color: darkgrey;
      width: 1rem;
      height: 1rem;
      transform: translateY(0.05em);
  }
</style>

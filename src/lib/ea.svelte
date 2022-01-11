<script lang="ts">
  import Icon from "@iconify/svelte";
  export let text: string = null;
  export let url: string = null;
  export let alt: string = null;
  export let iconOnly: boolean = false;

  const iconName = "fa-solid:external-link-square-alt";
</script>

{#if iconOnly}
  <a href={url} target="_blank" alt={alt || text || ""}>
    <Icon width="1rem" height="1rem" icon={iconName} />
  </a>
{:else}
  <a href={url} target="_blank" alt={alt || text || ""}>
    <div>
      <span>{text || url}</span>
      <Icon width="1rem" height="1rem" icon={iconName} />
    </div>
  </a>
{/if}

<style>
  div {
    display: inline-flex;
    flex-direction: row;
    align-items: center;
  }

  span {
    padding-right: 0.125rem;
  }

  a {
    text-decoration-style: solid;
    text-decoration-line: underline;
  }
</style>

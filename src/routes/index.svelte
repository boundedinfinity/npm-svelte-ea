<script lang="ts">
  import "../app.css";
  import Ea from "$lib/ea.svelte";
</script>

<table>
  <tr>
    <td class="key">URL only:</td>
    <td><Ea url="http://www.github.com" /></td>
  </tr>
  <tr>
    <td class="key">URL with text:</td>
    <td><Ea url="http://www.github.com" text="Github" /></td>
  </tr>
  <tr>
    <td class="key">Icon only:</td>
    <td><Ea url="http://www.github.com" text="Github" iconOnly={true} /></td>
  </tr>
</table>

<style>
  table {
    margin-left: 1rem;
    margin-top: 1rem;
  }
  td {
    border-style: solid;
    border-color: black;
    border-width: 1px;
    border-radius: 0.5rem;
    margin-top: 1rem;
    margin-bottom: 1rem;
    margin-left: 1rem;
    margin-right: 1rem;
    padding-top: 1rem;
    padding-bottom: 1rem;
    padding-left: 1rem;
    padding-right: 1rem;
  }

  .key {
    text-align: end;
  }
</style>

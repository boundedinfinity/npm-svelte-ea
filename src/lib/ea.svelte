<script lang="ts">
	import Icon from '@iconify/svelte';
	export let text: string = null;
	export let url: string = null;
    export let alt: string = null;

	let realText = text || url || 'UNKNOWN';
    let realAlt = alt || realText
</script>

<a href={url} target="_blank" alt={realAlt} class="text-slate-600 hover:text-slate-800">
    <div class="inline-flex flex-row align items-center">
        <span class="pr-0.5">{realText}</span>
        <Icon width="1rem" height="1rem" icon="fa-solid:external-link-square-alt" />
    </div>
</a>

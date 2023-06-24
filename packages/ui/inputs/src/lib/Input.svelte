<script lang="ts">
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();

    export let value = '';
    export let placeholder = '';
    export let type = '';
    export let id = '';
    export let name = '';

    function handleInput(event: Event) {
        const target = event.target as HTMLInputElement;
        dispatch('input', target.value);
    }

    function typeAction(node) {
		node.type = type;
	}


</script>

<input name={name} id={id} use:typeAction placeholder={placeholder} bind:value={value} on:input={e => handleInput(e)} />

<style>
    input {
        border: 1px solid #ccc;
        border-radius: 4px;
        padding: 0.5rem;
        font-size: 1rem;
        width: 100%;
        font-family: "Inter", sans-serif;
    }
</style>


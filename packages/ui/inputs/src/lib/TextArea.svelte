<script>
    export let id = "";
    export let name = "";
    export let cols = "";
    export let rows = "";


    function colsAction(node) {
		node.cols = parseInt(cols);
	}

    function rowsAction(node) {
		node.rows = parseInt(rows);
	}
</script>

<textarea name={name} id={id} use:colsAction use:rowsAction rows={rows}></textarea>

<style>
    textarea {
        border: 1px solid #ccc;
        border-radius: 4px;
        padding: 0.5rem;
        font-size: 1rem;
        width: 100%;
        font-family: "Inter", sans-serif;
    }
</style>
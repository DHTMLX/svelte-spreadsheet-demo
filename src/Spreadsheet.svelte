<script>
    import { onMount, onDestroy } from "svelte";
    import { Spreadsheet } from "@dhx/trial-spreadsheet";
    import "@dhx/trial-spreadsheet/codebase/spreadsheet.min.css"
    
    export let data;

    let container;
    let spreadsheet;
    
    onMount(() => {
        spreadsheet = new Spreadsheet(container, {});
        spreadsheet.parse(data);
    });

    onDestroy(() => {
        spreadsheet.destructor();
    });
</script>

<div bind:this={container} class="widget"></div>

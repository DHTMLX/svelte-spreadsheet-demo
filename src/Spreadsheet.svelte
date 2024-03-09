<script>
    import { onMount } from "svelte";
    
    import { Spreadsheet } from "@dhx/trial-spreadsheet";
    import "@dhx/trial-spreadsheet/codebase/spreadsheet.min.css"
    
    export let data;

    let spreadsheet;
    let container;
    onMount(() => {
        spreadsheet = new Spreadsheet(container, {});
        spreadsheet.events.on("ActionName", () => {})
    });

    $: spreadsheet?.parse(data);
</script>

<div bind:this={container} style="width: 100%; height: 100%;"></div>


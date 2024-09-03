<script>
    import Spreadsheet from "./Spreadsheet.svelte";
    import { getData } from "./data.js";

    const data = getData();
</script>

<Spreadsheet data={data} />

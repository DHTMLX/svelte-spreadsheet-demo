<script>
  import Spreadsheet from "./Spreadsheet.svelte";
  import { getData } from "./data.js";
</script>

<Spreadsheet data={getData()} />

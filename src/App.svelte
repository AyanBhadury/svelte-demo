<script>
  import FusionCharts from "fusioncharts";
  import Charts from "fusioncharts/fusioncharts.charts";
  import FusionTheme from "fusioncharts/themes/fusioncharts.theme.fusion";
  import SvelteFC, { fcRoot } from "svelte-fusioncharts";

  // Always set FusionCharts as the first parameter
  fcRoot(FusionCharts, Charts, FusionTheme);

  const dataSource = {
    chart: {
      caption: "Countries With Most Oil Reserves [2017-18]",
      subCaption: "In MMbbl = One Million barrels",
      xAxisName: "Country",
      yAxisName: "Reserves (MMbbl)",
      numberSuffix: "K",
      theme: "fusion",
    },
    data: [
      { label: "Venezuela", value: "290" },
      { label: "Saudi", value: "260" },
      { label: "Canada", value: "180" },
      { label: "Iran", value: "140" },
      { label: "Russia", value: "115" },
      { label: "UAE", value: "100" },
      { label: "US", value: "30" },
      { label: "China", value: "30" },
    ],
  };

  const chartConfigs = {
    type: "column2d",
    width: 600,
    height: 400,
    dataFormat: "json",
    dataSource: dataSource,
  };
</script>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<!--<script>
	export let name;
</script>-->

<main>
  <!-- <h1>Hello {name}!</h1> -->
  <h1>Svelte APP</h1>
</main>
<SvelteFC {...chartConfigs} />

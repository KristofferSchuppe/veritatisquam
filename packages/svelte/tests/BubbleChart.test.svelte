<script lang="ts">
  import { BubbleChart } from "../types";
  import type { BubbleChart as BC } from "@carbon/charts";
  import { bubbleDoubleLinearData as data, bubbleDoubleLinearOptions } from "@carbon/charts/demo/data";

  let chart: BC = null;
  let ref = null;

  const options = bubbleDoubleLinearOptions as any;
</script>

<BubbleChart
	bind:chart
	bind:ref
	on:load={e => {
		console.log(e.detail);
	}}
	on:update={e => {
		console.log(e.detail);
	}}
	on:destroy={e => {
		console.log(e.detail);
	}}
	{data}
	{options} />

<svelte:component
	this={BubbleChart}
	on:load={e => {
		console.log(e.detail);
	}}
	on:update={e => {
		console.log(e.detail);
	}}
	on:destroy={e => {
		console.log(e.detail);
	}}
	{data}
	{options} />

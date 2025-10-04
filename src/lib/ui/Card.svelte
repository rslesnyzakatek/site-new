<script lang="ts">
	export let clazzCard = '';
</script>

<div class={`rounded-lg border bg-card text-card-foreground shadow-sm ${clazzCard}`}>
	<slot />
</div>

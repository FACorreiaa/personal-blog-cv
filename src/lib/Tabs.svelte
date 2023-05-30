<script lang="ts">
	export let tabs: TabType[];

	type TabType = {
		name: string;
		url: string;
		isActive: boolean;
	};

	function handleClick(event) {
		event.preventDefault();
		const targetTab = event.target.dataset.tab;
		// Handle tab click event here, e.g., update active tab state
		console.log('Clicked tab:', targetTab);
	}
</script>

<div class="tabs">
	{#each tabs as tab}
		<a
			href={tab.url}
			class="tab tab-bordered {tab.isActive ? 'tab-active' : ''}"
			on:click={handleClick}
			data-tab={tab.name}
		>
			{tab.name}
		</a>
	{/each}
</div>

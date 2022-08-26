<script>
	import Header from '$lib/Header.svelte'
</script>

<div id="saleson">
	<Header />
	<slot />
</div>

<style>
:global(button[id="loadingActive"]),
:global(button[data-target="#findSupplierModal"]),
:global(button[data-target="#buyNowModal"]),
:global(button[data-target="#manufactureSearchModal"]),
:global(button[data-target="#itemDetailsModal"]),
:global(button[data-target="#orderProgressInfoModal"]),
:global(button[data-target="#userDetailsModal"]),
:global(button[data-target="#accountCodeModal"]),
:global(button[data-target="#requestsModal"]),
:global(button[data-target="#consigneeInfoModal"]),
:global(button[data-target="#enterOrderInfoModal"]) {
	animation-duration: 2.5s;
  animation-name: BoxShadow;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}

@keyframes BoxShadow {
	0% { 
		box-shadow: none;
	}
	100% { 
		box-shadow: 1px 1px 12px 3px #A6C8FF;
	}
}
</style>
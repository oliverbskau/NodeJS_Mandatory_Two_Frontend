<script>
	import Navigation from "./components/Navigation/Navigation.svelte";
	import CategoryNavigation from "./components/CategoryNavigation/CategoryNavigation.svelte";
	import CategoryMenu from "./components/CategoryNavigation/categoryMenu.svelte";
	import {toasts, ToastContainer, FlatToast } from "svelte-toasts";
</script>

<main>

	<Navigation/>
	<CategoryMenu/>
	<CategoryNavigation/>
	

	<ToastContainer placement="bottom-right" let:data>
		<FlatToast {data} />
	</ToastContainer>

</main>

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
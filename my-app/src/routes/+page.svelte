<script>
	import banner from '$lib/images/tofi-banner.jpg';
	import Content from './Content.svelte';
</script>



<section>
	<img src={banner} class="banner-img" alt="Banner" />
	
</section>

<Content/>


<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}
	.banner-img{
		width:100vw;
	}



	
</style>

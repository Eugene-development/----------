<script>
	export let content;
</script>

<div class="bg-white">
	<div class="max-w-2xl mx-auto px-4 py-12 sm:px-6 sm:py-20 lg:max-w-7xl lg:px-8">
		<!-- Details section -->
		<section aria-labelledby="details-heading">
			<div class="flex flex-col items-center text-center">
				<h2
					id="details-heading"
					class="text-4xl font-extrabold tracking-tight text-gray-900 sm:text-5xl"
				>
					{content.title}
				</h2>
				<p class="mt-3 max-w-3xl text-lg text-gray-600">{content.description}</p>
			</div>

			<div class="mt-8 grid grid-cols-1 gap-y-12 lg:grid-cols-2 lg:gap-x-16">
				<div>
					<div class="w-full aspect-w-3 aspect-h-2 rounded-lg overflow-hidden">
						<img
							src={content.img_1}
							alt={content.alt_1}
							class="w-full h-96 object-center object-cover"
						/>
					</div>
					{#each content.benefits_1 as { value }}
						<p class="mt-6 text-base text-gray-500">{@html value}</p>
					{/each}
				</div>
				<div>
					<div class="w-full aspect-w-3 aspect-h-2 rounded-lg overflow-hidden">
						<img
							src={content.img_2}
							alt={content.alt_2}
							class="w-full h-96 object-center object-cover"
						/>
					</div>
					{#each content.benefits_2 as { value }}
						<p class="mt-6 text-base text-gray-500">{@html value}</p>
					{/each}
				</div>
			</div>
		</section>
	</div>
</div>

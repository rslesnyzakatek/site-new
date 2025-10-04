<script lang="ts">
	import { Bed, Utensils, Activity, Home, TreePine, Accessibility } from '@lucide/svelte';

	const facilities = [
		{
			icon: Bed,
			title: '36 komfortowych pokoi',
			description:
				'Eleganckie, nowo urządzone pokoje 2 i 3-osobowe w trzech skrzydłach budynku. Dodatkowe miejsca noclegowe dla odwiedzających rodzin.',
			image: 'images/room-interior.webp'
		},
		{
			icon: Utensils,
			title: 'Własna kuchnia',
			description:
				'Pyszne, świeże i zdrowe posiłki przygotowywane codziennie na miejscu. Przestronna, jasna stołówka z widokiem na zieleń.',
			image: 'images/dining-room.webp'
		},
		{
			icon: TreePine,
			title: 'Bliskość natury',
			description:
				'Ośrodek otoczony jeziorami i lasami. Idealne miejsce na spacery, jazdę na rowerze i aktywne spędzanie czasu na świeżym powietrzu.',
			image: 'images/park-area.webp'
		}
	];

	const amenities = [
		{
			icon: Activity,
			title: 'Rehabilitacja',
			description: 'Profesjonalna fizjoterapia i terapia zajęciowo-aktywizacyjna'
		},
		{
			icon: Home,
			title: 'Pokój dzienny',
			description: 'Przestrzenne pomieszczenia wspólne do spotkań i integracji'
		},
		{
			icon: Accessibility,
			title: 'Bez barier',
			description: 'Parterowy budynek w pełni dostosowany do osób niepełnosprawnych'
		}
	];
</script>

<section id="facilities" class="scroll-m-8 bg-background py-20">
	<div class="container mx-auto px-4">
		<div class="mx-auto mb-16 max-w-3xl text-center">
			<h2 class="mb-6 text-4xl font-bold text-primary md:text-5xl">Udogodnienia i wyposażenie</h2>
			<p class="text-lg text-muted-foreground">
				Nowoczesny ośrodek wyposażony we wszystko, co potrzebne do komfortowego i aktywnego życia
				seniorów.
			</p>
		</div>

		<div class="mb-16 grid gap-8 md:grid-cols-3">
			{#each facilities as { icon: Icon, title, description, image }}
				<div
					class="group relative overflow-hidden rounded-xl shadow-lg transition-all duration-300 hover:shadow-2xl"
				>
					<div class="aspect-[4/3] overflow-hidden">
						<img
							src={image}
							alt={title}
							class="h-full w-full object-cover transition-transform duration-500 group-hover:scale-110"
						/>
					</div>
					<div
						class="absolute inset-0 bg-gradient-to-t from-primary/95 via-primary/70 to-transparent"
					></div>
					<div class="absolute right-0 bottom-0 left-0 p-6 text-primary-foreground">
						<Icon class="mb-3 h-8 w-8 text-accent" />
						<h3 class="mb-2 text-2xl font-bold">{title}</h3>
						<p class="text-sm leading-relaxed text-primary-foreground/90">
							{description}
						</p>
					</div>
				</div>
			{/each}
		</div>

		<div class="mx-auto grid max-w-4xl gap-6 md:grid-cols-3">
			{#each amenities as { icon: Icon, title, description }}
				<div
					class="rounded-lg bg-secondary/50 p-6 text-center transition-colors hover:bg-secondary"
				>
					<div
						class="mb-4 inline-flex h-16 w-16 items-center justify-center rounded-full bg-primary/10"
					>
						<Icon class="h-8 w-8 text-primary" />
					</div>
					<h4 class="mb-2 text-lg font-semibold text-foreground">
						{title}
					</h4>
					<p class="text-sm text-muted-foreground">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

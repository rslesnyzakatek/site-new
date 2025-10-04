<script lang="ts">
	import Card from '$lib/ui/Card.svelte';
	import { Shield, Heart, Users, Award } from '@lucide/svelte';

	const features = [
		{
			icon: Shield,
			title: 'Legalność i bezpieczeństwo',
			description:
				'Zarejestrowany i w pełni legalny ośrodek opieki nad seniorem. Posiadamy wszelkie wymagane pozwolenia i certyfikaty.'
		},
		{
			icon: Heart,
			title: 'Profesjonalna opieka',
			description:
				'Całodobowa opieka pielęgniarska i rehabilitacja zapewniana przez wykwalifikowany, doświadczony personel medyczny.'
		},
		{
			icon: Users,
			title: 'Kulturalna kadra',
			description:
				'Nasz zespół to wykwalifikowani opiekunowie, którzy tworzą przyjazną, rodzinną atmosferę i traktują każdego rezydenta z szacunkiem.'
		},
		{
			icon: Award,
			title: 'Najwyższe standardy',
			description:
				'Nowo wybudowany w 2025 roku obiekt spełniający najwyższe standardy komfortu i bezpieczeństwa dla osób starszych.'
		}
	];
</script>

<section
	id="about"
	class="scroll-m-8 bg-gradient-to-b from-warm-green-subtle to-warm-green-soft py-20"
>
	<div class="container mx-auto px-4">
		<div class="mx-auto mb-16 max-w-3xl text-center">
			<h2 class="mb-6 text-4xl font-bold text-primary md:text-5xl">
				Opieka na najwyższym poziomie
			</h2>
			<p class="text-lg text-balance text-muted-foreground">
				Rezydencja Seniora Leśny Zakątek to nowo wybudowany ośrodek opieki nad osobami starszymi,
				który łączy profesjonalizm z domową atmosferą blisko jezior i lasów.
			</p>
		</div>

		<div class="mx-auto grid max-w-6xl gap-6 md:grid-cols-2 lg:gap-8">
			{#each features as { icon: Icon, title, description }}
				<Card
					clazzCard="p-8 hover:shadow-xl transition-all duration-300 hover:-translate-y-1 bg-card border-border"
				>
					<div class="flex items-start gap-4">
						<div class="rounded-lg bg-primary/10 p-3">
							<Icon class="h-6 w-6 text-primary" />
						</div>
						<div>
							<h3 class="mb-3 text-xl font-semibold text-card-foreground">
								{title}
							</h3>
							<p class="leading-relaxed text-muted-foreground">
								{description}
							</p>
						</div>
					</div>
				</Card>
			{/each}
		</div>
	</div>
</section>

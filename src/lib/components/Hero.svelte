<script>
	import Button from '$lib/ui/Button.svelte';
	import { Phone, Mail } from '@lucide/svelte';
</script>

<section
	class="relative mt-24 flex min-h-screen items-center overflow-hidden bg-background lg:mt-0"
>
	<div class="max-w-8xl container mx-auto px-4">
		<div class="grid items-center gap-8 lg:grid-cols-2 lg:gap-12">
			<div class="order-2 lg:order-1">
				<div class="relative overflow-hidden rounded-2xl shadow-2xl">
					<img
						src="/images/hero-image.webp"
						alt="Rezydencja Seniora Leśny Zakątek"
						class="h-[500px] w-full object-cover lg:h-[600px]"
					/>
					<div class="absolute inset-0 bg-gradient-to-tr from-primary/30 to-transparent"></div>
				</div>
			</div>

			<div class="animate-fade-in order-1 space-y-8 lg:order-2">
				<h1
					class="text-4xl leading-tight font-bold text-balance text-primary md:text-6xl lg:text-7xl"
				>
					Rezydencja Seniora
					<br />
					<span class="text-accent">Leśny Zakątek</span>
				</h1>

				<p class="max-w-xl text-lg text-balance text-muted-foreground md:text-xl">
					Nowoczesny dom opieki w otoczeniu jezior i lasów. Profesjonalna opieka, komfort i
					serdeczna atmosfera dla Twoich bliskich.
				</p>

				<div class="flex flex-col gap-4 pt-4 sm:flex-row">
					<Button size="lg" clazz="text-lg px-8 py-6 hover:scale-105 transition-transform">
						<Phone class="mr-2 h-5 w-5" />
						Zadzwoń do nas
					</Button>
					<Button
						size="lg"
						variant="outline"
						clazz="text-lg px-8 py-6 hover:scale-105 transition-transform"
					>
						<Mail class="mr-2 h-5 w-5" />
						Napisz do nas
					</Button>
				</div>

				<div class="flex flex-wrap gap-6 pt-4 text-sm">
					<div class="flex items-center gap-2">
						<div class="h-2 w-2 rounded-full bg-accent"></div>
						<span class="text-foreground">Zarejestrowany ośrodek</span>
					</div>
					<div class="flex items-center gap-2">
						<div class="h-2 w-2 rounded-full bg-accent"></div>
						<span class="text-foreground">Nowo wybudowany w 2025</span>
					</div>
					<div class="flex items-center gap-2">
						<div class="h-2 w-2 rounded-full bg-accent"></div>
						<span class="text-foreground">36 komfortowych pokoi</span>
					</div>
				</div>
			</div>
		</div>
	</div>

	<div class="absolute bottom-8 left-1/2 -translate-x-1/2 transform">
		<div class="animate-bounce">
			<div
				class="flex h-10 w-6 items-start justify-center rounded-full border-2 border-primary/30 p-2"
			>
				<div class="h-3 w-1 rounded-full bg-primary/30"></div>
			</div>
		</div>
	</div>
</section>

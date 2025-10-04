<script lang="ts">
	import Button from '$lib/ui/Button.svelte';
	import Card from '$lib/ui/Card.svelte';
	import { MapPin, Phone, Mail, Clock } from '@lucide/svelte';

	const contactInfo = [
		{
			icon: Phone,
			title: 'Telefon',
			details: ['Zadzwoń do nas', 'Codziennie 8:00 - 20:00'],
			action: 'tel:+48123456789'
		},
		{
			icon: Mail,
			title: 'Email',
			details: ['kontakt@lesnyzakatek.pl', 'Odpowiadamy w 24h'],
			action: 'mailto:kontakt@lesnyzakatek.pl'
		},
		{
			icon: MapPin,
			title: 'Adres',
			details: ['Nowogard', 'województwo zachodniopomorskie'],
			action: '#location'
		},
		{
			icon: Clock,
			title: 'Odwiedziny',
			details: ['Codziennie', 'Umów się na wizytę'],
			action: 'tel:+48123456789'
		}
	];
</script>

<section id="contact" class="scroll-m-8 bg-background py-20">
	<div class="container mx-auto px-4">
		<div class="mx-auto mb-16 max-w-3xl text-center">
			<h2 class="mb-6 text-4xl font-bold text-primary md:text-5xl">Skontaktuj się z nami</h2>
			<p class="text-lg text-muted-foreground">
				Chętnie odpowiemy na wszystkie pytania i umówimy na wizytę w naszym ośrodku.
			</p>
		</div>

		<div class="mx-auto mb-12 grid max-w-6xl gap-6 sm:grid-cols-2 lg:grid-cols-4">
			{#each contactInfo as { icon: Icon, title, details } (title)}
				<Card
					clazzCard="bg-card p-6 text-center transition-all duration-300 hover:-translate-y-1 hover:shadow-lg"
				>
					<div
						class="mb-4 inline-flex h-16 w-16 items-center justify-center rounded-full bg-primary/10"
					>
						<Icon class="h-8 w-8 text-primary" />
					</div>
					<h3 class="mb-2 text-lg font-semibold text-card-foreground">
						{title}
					</h3>
					{#each details as detail, idx}
						<p
							class={`text-sm ${
								idx === 0 ? 'font-medium text-foreground' : 'text-muted-foreground'
							}`}
						>
							{detail}
						</p>
					{/each}
				</Card>
			{/each}
		</div>

		<div class="mx-auto max-w-2xl text-center">
			<Card
				clazzCard="border-primary/20 bg-gradient-to-br from-warm-green-subtle to-warm-green-soft p-8"
			>
				<h3 class="mb-4 text-2xl font-bold text-primary">Umów się na wizytę</h3>
				<p class="mb-6 text-muted-foreground">
					Zapraszamy do osobistego odwiedzenia naszego ośrodka. Pokaże Wam wszystkie pomieszczenia i
					odpowiemy na Wasze pytania.
				</p>
				<div class="flex flex-col justify-center gap-4 sm:flex-row">
					<Button size="lg" clazz="px-8 text-lg">
						<Phone class="mr-2 h-5 w-5" />
						Zadzwoń teraz
					</Button>
					<Button size="lg" variant="outline" clazz="px-8 text-lg">
						<Mail class="mr-2 h-5 w-5" />
						Wyślij wiadomość
					</Button>
				</div>
			</Card>
		</div>
	</div>
</section>

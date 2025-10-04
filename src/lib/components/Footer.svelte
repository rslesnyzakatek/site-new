<script>
	import { Heart } from '@lucide/svelte';
</script>

<footer class="bg-primary py-12 text-primary-foreground">
	<div class="container mx-auto px-4">
		<div class="mb-8 grid gap-8 md:grid-cols-3">
			<div>
				<h3 class="mb-4 text-2xl font-bold">Leśny Zakątek</h3>
				<p class="leading-relaxed text-primary-foreground/80">
					Rezydencja Seniora w sercu przyrody. Profesjonalna opieka i ciepła atmosfera dla Twoich
					bliskich.
				</p>
			</div>

			<div>
				<h4 class="mb-4 text-lg font-semibold">Kontakt</h4>
				<div class="space-y-2 text-primary-foreground/80">
					<p>Nowogard</p>
					<p>woj. zachodniopomorskie</p>
					<p>Tel: +48 123 456 789</p>
					<p>Email: kontakt@lesnyzakatek.pl</p>
				</div>
			</div>

			<div>
				<h4 class="mb-4 text-lg font-semibold">Godziny</h4>
				<div class="space-y-2 text-primary-foreground/80">
					<p>Biuro: 8:00 - 20:00</p>
					<p>Odwiedziny: Codziennie</p>
					<p class="pt-2">Opieka całodobowa</p>
				</div>
			</div>
		</div>

		<div class="border-t border-primary-foreground/20 pt-8 text-center">
			<div
				class="flex flex-col items-center justify-center gap-2 text-primary-foreground/70 md:flex-row"
			>
				<p>© 2025 Rezydencja Seniora Leśny Zakątek.</p>
				<p class="text-sm font-light">
					Stworzone z <Heart class="inline h-4 w-4 fill-accent text-accent" /> dla seniorów.
				</p>
			</div>
		</div>
	</div>
</footer>

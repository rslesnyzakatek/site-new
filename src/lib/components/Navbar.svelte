<script>
	import Button from '$lib/ui/Button.svelte';
	import { MenuIcon } from '@lucide/svelte';

	import { fly } from 'svelte/transition';

	let navbarVisible = false;

	const toggleMenu = () => {
		navbarVisible = !navbarVisible;
	};

	const navLinks = [
		{ label: 'O nas', href: '/#about' },
		{ label: 'Udogodnienia', href: '/#facilities' },
		{ label: 'Lokalizacja', href: '/#location' },
		{ label: 'Galeria', href: '/gallery' }
	];

	let scrolling = false;

	const scrollToContact = () => {
		const contactSection = document.getElementById('contact');
		if (contactSection) {
			contactSection.scrollIntoView({ behavior: 'smooth' });
		}
	};

	$: {
		try {
			window.onscroll = () => {
				if (window.scrollY > 20) {
					scrolling = true;
				} else {
					scrolling = false;
				}
			};
		} catch (e) {}
	}
</script>

<nav
	class="fixed top-0 right-0 left-0 z-50 bg-card transition-all duration-300 md:bg-transparent"
	class:scroll={scrolling}
	class:unscroll={!scrolling}
>
	<div class="max-w-8xl container mx-auto px-4">
		<div class="flex h-20 items-center justify-between">
			<div class="text-2xl font-bold text-primary">
				<a href="/">Leśny Zakątek</a>
			</div>
			<button on:click={toggleMenu} aria-label="Otwórz menu" class="md:hidden">
				<MenuIcon class="h-6 w-6 cursor-pointer text-primary md:hidden" />
			</button>
			<ul class="hidden items-center space-x-8 md:flex">
				{#each navLinks as { label, href }}
					<li class="text-foreground transition-colors duration-200 hover:text-primary">
						<a {href}>{label}</a>
					</li>
				{/each}
				<Button clazz="ml-4" size="lg" on:click={scrollToContact}>Kontakt</Button>
			</ul>
		</div>
	</div>
	{#if navbarVisible}
		<div
			class="absolute right-0 left-0 z-50 mx-4 mt-4 flex flex-col space-y-2 rounded-xl bg-card p-4 text-left text-xl md:hidden"
			in:fly={{ y: -100, duration: 300 }}
			out:fly={{ y: -100, duration: 300 }}
		>
			<ul class="flex flex-col space-y-4">
				{#each navLinks as { label, href }}
					<li
						class="block rounded-lg px-4 py-3 text-foreground transition-colors hover:bg-secondary"
					>
						<a {href}>{label}</a>
					</li>
				{/each}

				<div class="px-4 pt-2">
					<Button clazz="w-full" size="lg" on:click={scrollToContact}>Kontakt</Button>
				</div>
			</ul>
		</div>
	{/if}
</nav>

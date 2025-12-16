<script lang="ts">
	import Header from "$lib/components/Header.svelte";
	import { ArrowUpRight, ArrowRight, BookOpen } from 'lucide-svelte';

	const collections = [
		{ id: '01', name: 'THE GREAT GATSBY', category: 'Classic Novels' },
		{ id: '02', name: 'PRIDE AND PREJUDICE', category: 'Classic Novels' },
		{ id: '03', name: 'ALICE\'S ADVENTURES IN WONDERLAND', category: 'Fantasy' },
		{ id: '04', name: 'THE HOUND OF THE BASKERVILLES', category: 'Mystery' },
		{ id: '05', name: 'PETER AND WENDY', category: 'Adventure' },
		{ id: '06', name: 'THE WONDERFUL WIZARD OF OZ', category: 'Fantasy' },
		{ id: '07', name: 'TWENTY THOUSAND LEAGUES UNDER THE SEA', category: 'Adventure' },
		{ id: '08', name: 'THE PICTURE OF DORIAN GRAY', category: 'Classic Novels' },
		{ id: '09', name: 'ODYSSEY', category: 'Adventure' },
		{ id: '10', name: 'ADVENTURES OF HUCKLEBERRY FINN', category: 'Classic Novels' },
		{ id: '11', name: 'GULLIVER\'S TRAVELS', category: 'Classic Novels' },
		{ id: '12', name: 'CINDERELLA', category: 'Fairy Tales' },
		{ id: '13', name: 'LITTLE RED RIDING HOOD', category: 'Fairy Tales' },
		{ id: '14', name: 'SNOW WHITE', category: 'Fairy Tales' },
		{ id: '15', name: 'RAPUNZEL', category: 'Fairy Tales' },
		{ id: '16', name: 'HANSEL AND GRETEL', category: 'Fairy Tales' }
	];

	const features = [
		{ 
			title: 'COMPLETE TEXT', 
			description: 'Every poster contains the entire book text from beginning to end, maintaining full readability.',
			icon: BookOpen
		},
		{ 
			title: 'ARTISTIC TYPOGRAPHY', 
			description: 'Text is precisely wrapped around iconic imagery, creating a dual-purpose art piece.',
			icon: BookOpen
		},
		{ 
			title: 'HANDCRAFTED DESIGN', 
			description: 'Each piece requires meticulous typography and layout design to maintain both art and literature.',
			icon: BookOpen
		}
	];
</script>

<div class="min-h-screen bg-[#F4F4F2] text-[#1A1A1A] font-sans selection:bg-primary-600 selection:text-white overflow-x-hidden">
	<Header />

	<main>
		<!-- Hero Section -->
		<section class="pt-12 md:pt-20 pb-10 px-4 md:px-8">
			<div class="flex flex-col md:flex-row justify-between items-start mb-12 md:mb-24 relative">
				<div class="max-w-[200px] text-[10px] leading-relaxed uppercase tracking-wide font-medium mt-2">
					<p>Transform classic literature into stunning wall art. Complete book texts wrapped in intricate typography around iconic imagery.</p>
				</div>
				<h1 class="text-[14vw] md:text-[9rem] lg:text-[11rem] leading-[0.8] font-thin tracking-tighter text-right mt-8 md:mt-0 uppercase">
					Classic <br />
					Literature
				</h1>
			</div>

			<!-- Hero Images -->
			<div class="grid grid-cols-5 gap-2 md:gap-4 mb-8 h-[30vh] md:h-[50vh]">
				<div class="overflow-hidden h-full">
					<img src="/generated/image-close-up-of-hands-holding-an-open-classi-1765848473169-1.webp" alt="Reading classic literature" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="/generated/image-stack-of-vintage-classic-literature-book-1765848475380-2.webp" alt="Vintage books" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="/generated/image-person-reading-a-book-in-cozy-home-setti-1765848477643-3.webp" alt="Reading at home" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="/generated/image-typography-art-poster-detail-showing-leg-1765848479940-4.webp" alt="Typography detail" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
				<div class="overflow-hidden h-full">
					<img src="/generated/image-literary-art-poster-on-living-room-wall--1765848470511-0.webp" alt="Literary art on wall" class="w-full h-full object-cover hover:scale-110 transition-transform duration-1000" />
				</div>
			</div>

			<div class="flex flex-col md:flex-row justify-between items-start">
				<span class="text-[10px] uppercase tracking-wide font-medium mt-4 hidden md:block">Scroll</span>
				<h1 class="text-[14vw] md:text-[9rem] lg:text-[11rem] leading-[0.8] font-thin tracking-tighter text-right w-full uppercase">
					Meets <br />
					Wall Art
				</h1>
			</div>
		</section>

		<!-- Collection Section -->
		<section class="py-20 md:py-32" id="collection">
			<div class="flex justify-center mb-16 md:mb-24">
				<span class="text-[10px] font-bold uppercase tracking-widest">Literary Collection</span>
			</div>

			<div class="border-t border-gray-300">
				{#each collections as item}
					<div class="group border-b border-gray-300 py-6 md:py-10 px-4 md:px-8 flex items-center justify-between hover:bg-white transition-colors cursor-pointer">
						<span class="text-[10px] font-medium text-gray-500 w-8 md:w-12">/{item.id}</span>
						<h2 class="text-2xl md:text-5xl lg:text-6xl font-thin tracking-tight group-hover:italic transition-all duration-300 uppercase flex-1 text-center">{item.name}</h2>
						<div class="flex items-center gap-1 text-[10px] font-medium uppercase opacity-0 group-hover:opacity-100 transition-opacity translate-x-[-10px] group-hover:translate-x-0 duration-300 w-24 justify-end">
							<span class="text-primary-600">SOLD OUT</span>
						</div>
					</div>
				{/each}
			</div>

			<div class="text-center mt-12 px-4">
				<p class="text-[10px] uppercase tracking-wide font-medium text-gray-500 mb-4">All prints currently sold out • $44.00 each</p>
				<a href="#waitlist" class="inline-flex items-center gap-1 text-[10px] font-medium uppercase hover:opacity-60 transition-opacity">
					<ArrowUpRight size={10} />
					Join Waitlist for Restock
				</a>
			</div>
		</section>

		<!-- Process Section -->
		<section class="py-20 px-4 md:px-8 bg-[#F4F4F2]" id="process">
			<div class="flex flex-col md:flex-row justify-between items-start mb-16 md:mb-24">
				<h2 class="text-4xl md:text-6xl font-light tracking-tight mb-8 md:mb-0 uppercase">The Craft</h2>
				<div class="max-w-xs text-[10px] leading-relaxed uppercase tracking-wide font-medium text-right md:text-left">
					<p>Each NovelPoster is a meticulous work of art, requiring precise typography and layout design to transform complete literary texts into visual masterpieces.</p>
				</div>
			</div>

			<div class="grid grid-cols-1 md:grid-cols-3 gap-8 md:gap-12 mb-16">
				{#each features as feature}
					<div class="group">
						<div class="aspect-square overflow-hidden mb-6 bg-white border border-gray-200 flex items-center justify-center">
							<div class="w-16 h-16 text-primary-600">
								<svelte:component this={feature.icon} size={64} strokeWidth={1} />
							</div>
						</div>
						<h3 class="text-xs font-bold uppercase tracking-wide mb-3">{feature.title}</h3>
						<p class="text-[10px] text-gray-600 leading-relaxed uppercase tracking-wide">{feature.description}</p>
					</div>
				{/each}
			</div>

			<!-- Process Images -->
			<div class="grid grid-cols-1 md:grid-cols-2 gap-4">
				<div class="aspect-[4/3] overflow-hidden bg-gray-200">
					<img src="/generated/image-extreme-close-up-of-printed-typography-s-1765848484322-6.webp" alt="Typography detail" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
				</div>
				<div class="aspect-[4/3] overflow-hidden bg-gray-200">
					<img src="/generated/image-designer-working-on-typography-layout-on-1765848488684-8.webp" alt="Design process" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
				</div>
			</div>
		</section>

		<!-- Gallery Section -->
		<section class="py-20 px-4 md:px-8" id="gallery">
			<div class="flex flex-col lg:flex-row mb-16 gap-12 lg:gap-24">
				<div class="flex-1">
					<h2 class="text-4xl md:text-6xl font-light tracking-tight uppercase">NovelPoster Gallery</h2>
				</div>
				<div class="flex-1">
					<h2 class="text-3xl md:text-5xl font-light tracking-tight mb-8 text-left uppercase leading-tight">Where literature<br/>becomes art</h2>
					<div class="grid grid-cols-1 md:grid-cols-2 gap-8 text-[10px] leading-relaxed uppercase tracking-wide font-medium">
						<p>NovelPoster transforms beloved classics into stunning wall art. Each piece contains the complete text of the book, meticulously wrapped around iconic imagery that captures the essence of the story.</p>
						<p>Created by artist Rhys Logan, these literary art prints appeal to book lovers seeking meaningful decor. The intricate typography craft makes each poster both a visual masterpiece and a fully readable text—a true fusion of art and literature.</p>
					</div>
					<a href="#about" class="inline-flex items-center gap-1 text-[10px] font-medium uppercase mt-8 hover:opacity-60 transition-opacity">
						<ArrowUpRight size={10} />
						About the Artist
					</a>
				</div>
			</div>

			<div class="flex flex-col md:flex-row gap-4 h-[50vh] md:h-[70vh]">
				<div class="w-full md:w-[60%] h-full bg-gray-200 overflow-hidden">
					<img src="/generated/image-minimalist-home-office-with-literary-pos-1765848482145-5.webp" alt="Literary poster in home office" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
				</div>
				<div class="w-full md:w-[40%] h-full flex flex-col gap-4">
					<div class="flex-1 bg-gray-200 overflow-hidden">
						<img src="/generated/image-cozy-reading-nook-with-armchair-bookshel-1765848486448-7.webp" alt="Reading nook with art" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
					</div>
					<div class="flex-1 flex gap-4">
						<div class="flex-1 bg-gray-200 overflow-hidden">
							<img src="/generated/image-typography-art-poster-detail-showing-leg-1765848479940-4.webp" alt="Typography detail" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
						</div>
						<div class="flex-1 bg-gray-200 overflow-hidden">
							<img src="/generated/image-close-up-of-hands-holding-an-open-classi-1765848473169-1.webp" alt="Reading classic book" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
						</div>
					</div>
				</div>
			</div>
		</section>

		<!-- CTA Section -->
		<section class="py-32 px-4 md:px-8 bg-primary-600 text-white text-center" id="waitlist">
			<span class="text-[10px] font-medium uppercase tracking-widest mb-6 block opacity-80">Currently Sold Out</span>
			<h2 class="text-4xl md:text-6xl lg:text-8xl font-thin tracking-tight mb-12 uppercase">
				Join the <br />
				Waitlist
			</h2>
			<p class="text-sm uppercase tracking-wide mb-12 max-w-md mx-auto opacity-90">
				Be the first to know when our literary art prints are back in stock. All 16 titles available at $44.00 each.
			</p>
			<a href="#contact" class="inline-block bg-[#1A1A1A] text-white px-10 py-4 rounded-full text-[10px] font-bold uppercase tracking-widest hover:bg-white hover:text-primary-600 transition-colors">
				Notify Me
			</a>
		</section>

		<!-- Bottom Gallery -->
		<div class="grid grid-cols-2 md:grid-cols-5 h-[60vh]">
			<div class="overflow-hidden">
				<img src="/generated/image-gallery-wall-with-multiple-framed-litera-1765848490913-9.webp" alt="Gallery wall" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden">
				<img src="/generated/image-cozy-reading-nook-with-armchair-bookshel-1765848486448-7.webp" alt="Reading nook" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden">
				<img src="/generated/image-stack-of-vintage-classic-literature-book-1765848475380-2.webp" alt="Classic books" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden">
				<img src="/generated/image-minimalist-home-office-with-literary-pos-1765848482145-5.webp" alt="Home office" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
			<div class="overflow-hidden hidden md:block">
				<img src="/generated/image-literary-art-poster-on-living-room-wall--1765848470511-0.webp" alt="Literary art poster" class="w-full h-full object-cover hover:scale-105 transition-transform duration-700" />
			</div>
		</div>

		<!-- Footer Marquee -->
		<div class="overflow-hidden py-6 border-b border-gray-200">
			<div class="whitespace-nowrap animate-marquee flex">
				<span class="text-4xl md:text-6xl lg:text-8xl font-thin tracking-tight mx-4 uppercase">Classic Literature Meets Wall Art — Classic Literature Meets Wall Art — Classic Literature Meets Wall Art — </span>
				<span class="text-4xl md:text-6xl lg:text-8xl font-thin tracking-tight mx-4 uppercase">Classic Literature Meets Wall Art — Classic Literature Meets Wall Art — Classic Literature Meets Wall Art — </span>
			</div>
		</div>
	</main>

	<footer class="px-4 md:px-8 py-12 text-[10px] font-medium uppercase tracking-wide">
		<div class="flex flex-col md:flex-row justify-between items-start md:items-end gap-12 md:gap-8">
			<div class="flex flex-col gap-3">
				<a href="#collection" class="hover:opacity-60">Collection</a>
				<a href="#process" class="hover:opacity-60">Process</a>
				<a href="#gallery" class="hover:opacity-60">Gallery</a>
				<a href="#about" class="hover:opacity-60">About</a>
				<a href="#waitlist" class="hover:opacity-60">Waitlist</a>
			</div>

			<div class="text-left md:text-center">
				<p class="text-lg md:text-2xl font-normal tracking-tight mb-6">HELLO@NOVELPOSTER.COM</p>
				<p class="text-[10px] tracking-widest text-gray-500">ALL DESIGNS © RHYS LOGAN</p>
			</div>

			<div class="flex flex-col gap-3 text-left md:text-right">
				<a href="#privacy" class="hover:opacity-60">Privacy Policy</a>
				<a href="#terms" class="hover:opacity-60">Terms & Conditions</a>
				<a href="#press" class="hover:opacity-60">Press</a>
			</div>
		</div>

		<div class="flex flex-col md:flex-row justify-between items-center mt-20 pt-8 border-t border-gray-200 text-[10px] text-gray-400 gap-4">
			<p>©NOVELPOSTER. ALL RIGHTS RESERVED</p>
			<div class="flex items-center gap-2">
				<div class="w-5 h-5 text-primary-600">
					<svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
						<path
							fill-rule="evenodd"
							clip-rule="evenodd"
							d="M11.6277 5.74767C10.7109 6.38712 9.22456 6.38712 8.3078 5.74767C7.39104 5.10821 7.39104 4.07144 8.3078 3.43199C9.22456 2.79253 10.7109 2.79253 11.6277 3.43199C12.5445 4.07144 12.5445 5.10821 11.6277 5.74767ZM12.3486 9.68436C13.4488 10.4517 15.2324 10.4517 16.3325 9.68436C17.4326 8.91698 17.4326 7.67288 16.3325 6.90553C15.2324 6.13818 13.4488 6.13818 12.3486 6.90553C11.2485 7.67288 11.2485 8.91698 12.3486 9.68436ZM4.73651 16.6314C5.46993 17.143 6.65903 17.143 7.39246 16.6314C8.12584 16.1198 8.12584 15.2904 7.39246 14.7788C6.65903 14.2672 5.46993 14.2672 4.73651 14.7788C4.0031 15.2904 4.0031 16.1198 4.73651 16.6314ZM11.6277 13.1579C10.7109 13.7973 9.22456 13.7973 8.3078 13.1579C7.39104 12.5184 7.39104 11.4816 8.3078 10.8421C9.22456 10.2027 10.7109 10.2027 11.6277 10.8421C12.5445 11.4816 12.5445 12.5184 11.6277 13.1579ZM2.41254 12.6947C2.9626 13.0784 3.85443 13.0784 4.40449 12.6947C4.95455 12.311 4.95455 11.689 4.40449 11.3053C3.85443 10.9216 2.9626 10.9216 2.41254 11.3053C1.86248 11.689 1.86249 12.311 2.41254 12.6947ZM4.73651 9.22117C5.46992 9.73275 6.65902 9.73275 7.39246 9.22117C8.12584 8.7096 8.12584 7.88018 7.39246 7.36863C6.65902 6.85706 5.46992 6.85706 4.73651 7.36863C4.0031 7.88018 4.0031 8.7096 4.73651 9.22117ZM11.6277 20.568C10.7109 21.2075 9.22456 21.2075 8.3078 20.568C7.39104 19.9286 7.39104 18.8918 8.3078 18.2523C9.22456 17.6129 10.7109 17.6129 11.6277 18.2523C12.5445 18.8918 12.5445 19.9286 11.6277 20.568ZM17.191 13.3894C18.2911 14.1568 20.0748 14.1568 21.1749 13.3894C22.275 12.6221 22.275 11.3779 21.1749 10.6106C20.0748 9.84324 18.2911 9.84324 17.191 10.6106C16.0909 11.3779 16.0909 12.6221 17.191 13.3894ZM16.3325 17.0945C15.2324 17.8618 13.4488 17.8618 12.3486 17.0945C11.2485 16.3271 11.2485 15.083 12.3486 14.3156C13.4488 13.5483 15.2324 13.5483 16.3325 14.3156C17.4326 15.083 17.4326 16.3271 16.3325 17.0945Z"
							fill="currentColor"
						/>
					</svg>
				</div>
				<span class="text-black text-lg font-bold tracking-tight">NOVELPOSTER</span>
			</div>
			<p>LITERARY ART FOR BOOK LOVERS</p>
		</div>
	</footer>
</div>

<style>
	@keyframes marquee {
		0% { transform: translateX(0); }
		100% { transform: translateX(-50%); }
	}
	.animate-marquee {
		animation: marquee 30s linear infinite;
	}
</style>


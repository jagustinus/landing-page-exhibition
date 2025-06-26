<script>
	import { Button } from '$lib/components/ui/button/index';
	import { Badge } from '$lib/components/ui/badge/index';
	import { BrainCircuit } from 'lucide-svelte';
	import { LetterText } from 'lucide-svelte';
	import { ScanFace } from 'lucide-svelte';

	const listApplications = [
		{
			title: 'MBTI Test Informatika',
			description: 'Tes kepribadian MBTI untuk menentukan jurusan Informatika',
			href: 'https://ukdc-kbu-mbti-1.joelmedia.my.id/',
			icon: BrainCircuit
		},
		{
			title: 'MBTI Test Pekerjaan',
			description: 'Tes kepribadian MBTI untuk menentukan minat pekerjaan',
			href: 'https://ukdc-kbu-mbti-2.joelmedia.my.id/',
			icon: BrainCircuit
		},
		{
			title: 'Generator Teks Hoax',
			description: 'Aplikasi untuk menghasilkan teks berita hoax dengan bahasa Indonesia',
			href: 'https://generate-hoaks-gpt2-c4htvdjh7fdspjr8pewrkt.streamlit.app/',
			icon: LetterText
		},
		{
			title: 'Deteksi Kesimetrisan pada Wajah',
			description:
				'Aplikasi untuk mendeteksi kesimetrisan pada wajah menggunakan OpenCV dan Algoritma Viola Jones',
			href: 'https://ukdc-kbu-face-analyzer.joelmedia.my.id/',
			icon: ScanFace
		}
	];
</script>

<section
	id="applications"
	class="container mx-auto flex flex-col items-center justify-center space-y-4 py-16 md:py-24"
>
	<div class="mx-auto text-center">
		<h1 class="text-xl font-semibold tracking-tight sm:text-6xl lg:text-4xl">Showcase Aplikasi</h1>
		<p
			class="text-muted-foreground mx-auto mt-4 max-w-[18rem] text-center text-sm leading-5 md:max-w-2xl md:text-lg md:leading-8"
		>
			Temukan berbagai aplikasi keren hasil karya kami. Showcase ini menampilkan ide-ide inovatif
			dan penggunaan teknologi terkini.
		</p>
	</div>
	<div class="mx-auto grid justify-center gap-4 px-12 py-8 sm:grid-cols-2 md:max-w-5xl md:py-16">
		{#each listApplications as app}
			<a href={app.href} class="no-underline" target="_blank">
				<div
					class="bg-background relative overflow-hidden rounded-lg border p-2 transition-all duration-300 ease-in-out hover:border-red-400 hover:shadow-sm"
				>
					<div class="flex h-[180px] flex-col gap-4 rounded-md p-6">
						<svelte:component this={app.icon} class="h-8 w-8 text-red-500" />
						<div class="space-y-2">
							<h3 class="font-medium">{app.title}</h3>
							<p class="text-muted-foreground text-sm">
								{app.description}
							</p>
						</div>
					</div>
				</div>
			</a>
		{/each}
	</div>
</section>

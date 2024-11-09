<script lang="ts">
	import { Tabs } from 'bits-ui';

	// tabler.io/icons
	const links = [
		{
			icon: `<svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-github"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M9 19c-4.3 1.4 -4.3 -2.5 -6 -3m12 5v-3.5c0 -1 .1 -1.4 -.5 -2c2.8 -.3 5.5 -1.4 5.5 -6a4.6 4.6 0 0 0 -1.3 -3.2a4.2 4.2 0 0 0 -.1 -3.2s-1.1 -.3 -3.5 1.3a12.3 12.3 0 0 0 -6.2 0c-2.4 -1.6 -3.5 -1.3 -3.5 -1.3a4.2 4.2 0 0 0 -.1 3.2a4.6 4.6 0 0 0 -1.3 3.2c0 4.6 2.7 5.7 5.5 6c-.6 .6 -.6 1.2 -.5 2v3.5" /></svg>`,
			href: 'https://github.com/vishnukumarkvs'
		},
		{
			icon: `<svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-linkedin"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M8 11v5" /><path d="M8 8v.01" /><path d="M12 16v-5" /><path d="M16 16v-3a2 2 0 1 0 -4 0" /><path d="M3 7a4 4 0 0 1 4 -4h10a4 4 0 0 1 4 4v10a4 4 0 0 1 -4 4h-10a4 4 0 0 1 -4 -4z" /></svg>`,
			href: 'https://www.linkedin.com/in/vishnu-kvs/'
		},
		{
			icon: `<svg  xmlns="http://www.w3.org/2000/svg"  width="24"  height="24"  viewBox="0 0 24 24"  fill="none"  stroke="currentColor"  stroke-width="2"  stroke-linecap="round"  stroke-linejoin="round"  class="icon icon-tabler icons-tabler-outline icon-tabler-brand-medium"><path stroke="none" d="M0 0h24v24H0z" fill="none"/><path d="M4 4m0 2a2 2 0 0 1 2 -2h12a2 2 0 0 1 2 2v12a2 2 0 0 1 -2 2h-12a2 2 0 0 1 -2 -2z" /><path d="M8 9h1l3 3l3 -3h1" /><path d="M8 15l2 0" /><path d="M14 15l2 0" /><path d="M9 9l0 6" /><path d="M15 9l0 6" /></svg>`,
			href: 'https://medium.com/@kvs-vishnu23'
		}
	];
</script>

<div class="mx-10 p-4">
	<Tabs.Root class="flex w-full flex-col" value="about">
		<Tabs.List class="text-md flex space-x-10 rounded-md p-5 font-semibold">
			<Tabs.Trigger
				value="about"
				class="rounded-md p-1 px-2 data-[state=active]:bg-black data-[state=active]:text-white"
			>
				About
			</Tabs.Trigger>
			<Tabs.Trigger
				value="work"
				class="rounded-md p-1 px-2 data-[state=active]:bg-black data-[state=active]:text-white"
			>
				Work
			</Tabs.Trigger>
			<Tabs.Trigger
				value="hobbies"
				class="rounded-md p-1 px-2 data-[state=active]:bg-black data-[state=active]:text-white"
			>
				Hobbies
			</Tabs.Trigger>
			<Tabs.Trigger
				value="articles"
				class="rounded-md p-1 px-2 data-[state=active]:bg-black data-[state=active]:text-white"
			>
				Articles
			</Tabs.Trigger>
		</Tabs.List>
		<Tabs.Content value="about" class="my-5 p-5">
			<div class="grid grid-cols-2">
				<div>
					<p class="text-7xl font-bold">Hi, I am Vishnu...</p>
					<p class="py-4 pt-8 text-2xl font-semibold" style="font-family: 'Comic Neue'">
						I am a Software Engineer with expertise in Cloud, SRE and Full Stack Dev.
					</p>
					<p class="py-4 text-lg leading-loose" style="font-family: 'Comic Neue', font-weight: 600">
						I'm striving to become a polyglot, passionate about working with various technologies.
						I'm a Go and Kubernetes enthusiast who enjoys full-stack development for fun and
						documents my knowledge on Medium.
					</p>
					<div class="my-4">
						<p class="py-2 text-xl">Here are my socials</p>
						<div class="flex">
							{#each links as link}
								{@render iconLink(link.icon, link.href)}
							{/each}
						</div>
					</div>
					<div class="mt-10">
						{#each Array(7) as _, i}
							<p class="text-xl">XXXXXXXXXXXXXXXXXXX</p>
						{/each}
					</div>
				</div>
				<div></div>
			</div>
		</Tabs.Content>
		<Tabs.Content value="work" class="my-5 p-5">
			<div class="grid grid-cols-2">
				<div class="flex flex-col space-y-8">
					<p class="p-2 text-xl leading-loose" style="font-family: 'Noto Sans'">
						I’m a <span class="text-xl font-bold text-sky-500">Software Engineer II at F5</span>,
						where I balance between Site Reliability Engineering (SRE) and Development. I work with
						Kubernetes and AWS Cloud, using tools like Helm, Argo, and the LMA stack (Prometheus,
						Cortex, Loki, and Elasticsearch). I have built detailed Grafana dashboards as well with
						Grafonnet to give insights at a glance.
					</p>

					<p class="p-2 text-xl leading-loose" style="font-family: 'Noto Sans'">
						I also have a lot of experience with Infrastructure as Code from my previous org,
						primarily with Terraform and AWS CDK. I also work with Go, I’ve created a range of
						custom CLI tools that help make our workflows easier and more efficient.
					</p>

					<p class="p-2 text-xl leading-loose" style="font-family: 'Noto Sans'">
						In my free time, I enjoy building full-stack projects. I use Svelte for front-end work
						and either Go or Node.js for the backend. I’ve created a few websites, including
						{@render Link("https://candletower.com","candletower.com")} and {@render Link("https://www.producthunt.com/products/quickrefer","quickrefer.in")}
					</p>

					<p class="p-2 text-xl leading-loose" style="font-family: 'Noto Sans'">
						I am a part of {@render Link("https://phinite.ai","Phinite.Ai")}, an AI-driven platform that enhances call center
						operations. There, I led the DevOps pipeline, using some of the latest technologies to
						help improve customer interactions and drive operational efficiency.
					</p>
				</div>
				<div></div>
			</div>
		</Tabs.Content>
		<Tabs.Content value="hobbies" class="my-5 p-5">
			<div class="grid grid-cols-2">
				<div class="flex flex-col space-y-8">
					<p class="p-2 text-xl leading-loose" style="font-family: 'Noto Sans'">
						In my free time, you’ll often find me with a book in hand. I’m a huge fan of novels like
						Norwegian Wood and Before the Coffee Gets Cold. When I’m not reading, I enjoy a good
						game of chess, or really any game that freshens my mind.
					</p>
					<p class="p-2 text-xl leading-loose" style="font-family: 'Noto Sans'">
						I also enjoy building things, whether it’s a side project or experimenting with new
						tech. Writing about my experiences and what I’ve learned on Medium is something I really
						enjoy. It’s a way for me to document and share my journey in tech.
					</p>
					<p class="p-2 text-xl leading-loose" style="font-family: 'Noto Sans'">
						I play badminton from time to time to stay active, but I also like to relax with a good
						movie or anime. One Piece is my all time favourite. I also enjoy the wild humor of Rick
						and Morty. Whether it's a Netflix series or a great anime, I'm always up for something
						new.
					</p>
				</div>
				<div></div>
			</div>
		</Tabs.Content>
	</Tabs.Root>
</div>

{#snippet iconLink(iconsvg, href)}
	<a {href} target="_blank" rel="noopener noreferer">
		<div class="">
			{@html iconsvg.replace('width="24"', 'width="40"').replace('height="24"', 'height="40"')}
		</div>
	</a>
{/snippet}

{#snippet Link(href, text)}
	<a {href} class="text-sky-600" target="_blank" rel="noopener noreferer">{text}</a>
{/snippet}

<style>
@import url('https://fonts.googleapis.com/css2?family=Comic+Neue:ital,wght@0,300;0,400;0,700;1,300;1,400;1,700&family=Gaegu&family=Noto+Sans:ital,wght@0,100..900;1,100..900&family=Roboto+Slab:wght@100..900&display=swap');
</style>

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
					<p class="py-4 text-xl">
						I am a Software Engineer with expertise in Cloud, SRE and Full Stack Dev.
					</p>
					<p class="py-4 text-lg">
						I'm striving to become a polyglot, passionate about working with various technologies.
						I'm a Go and Kubernetes enthusiast who enjoys full-stack development for fun and
						documents my knowledge on Medium.
					</p>
					<div class="my-4">
						<p class="font-md py-2 text-xl">Here are my socials</p>
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
		<Tabs.Content value="work">
			<p>Thjustify-endis is about my work</p>
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

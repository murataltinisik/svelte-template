<script>
	import '../app.css'
	import { page } from '$app/stores'
  	import Fa from 'svelte-fa';
	import { faSearch } from '@fortawesome/free-solid-svg-icons'
  	import Title from './Title.svelte';

	// 
	let isOpenMenu = false;

	// VARIABLES
	const activeLink = "md:bg-transparent md:text-red-500 dark:text-white md:dark:text-red-500";
</script>

<!-- NAVBAR -->
<nav class="bg-white border-gray-200 dark:bg-gray-900">
	<div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
		<a href="/" class="flex items-center">
			<h1 class="self-center text-2xl font-semibold whitespace-nowrap dark:text-white">
				<Title />
			</h1>
		</a>

		<button
			data-collapse-toggle="navbar-default"
			type="button"
			class="inline-flex items-center p-2 ml-3 text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
			aria-controls="navbar-default"
			aria-expanded="false"
		>
			<span class="sr-only">Open main menu</span>
			<svg
				class="w-6 h-6"
				aria-hidden="true"
				fill="currentColor"
				viewBox="0 0 20 20"
				xmlns="http://www.w3.org/2000/svg"
			>
				<path
					fill-rule="evenodd"
					d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
					clip-rule="evenodd"
				></path>
			</svg>
		</button>

		<div class="hidden w-full md:block md:w-auto" id="navbar-default">
			<ul class="font-medium flex flex-col p-4 md:p-0 mt-4 border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-8 md:mt-0 md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700">
				<li>
					<a
						href="/"
						class={`${$page.url.pathname === "/" && activeLink} block py-2 pl-3 pr-4 rounded md:p-0`}
					>
						Home
					</a>
				</li>
				<li>
					<a
						href="/news"
						class={`${$page.url.pathname.indexOf('news') === 1 && activeLink} block py-2 pl-3 pr-4 rounded md:p-0`}
					>
						News
					</a>
				</li>
				<li>
					<a
						href="/about"
						class={`${$page.url.pathname.indexOf('about') === 1 && activeLink} block py-2 pl-3 pr-4 rounded md:p-0`}
					>
						About
					</a>
				</li>
			</ul>
		</div>

		<div class="flex items-center relative">
			<a href="/news">
				<Fa icon={faSearch}/>
			</a>

			<a href="/auth/signin">
				<button type="button" class="text-gray-900 bg-white border border-gray-300 focus:outline-none hover:bg-gray-100 focus:ring-4 focus:ring-gray-200 font-medium rounded-lg text-sm px-5 mx-3 py-2.5 dark:bg-gray-800 dark:text-white dark:border-gray-600 dark:hover:bg-gray-700 dark:hover:border-gray-600 dark:focus:ring-gray-700">
					Sign In
				</button>
			</a>
			
			<a href="/auth/signup">
				<button type="button" class="text-white bg-gray-800 hover:bg-gray-900 focus:outline-none focus:ring-4 focus:ring-gray-300 font-medium rounded-lg text-sm px-5 py-2.5 dark:bg-gray-800 dark:hover:bg-gray-700 dark:focus:ring-gray-700 dark:border-gray-700">
					Sign Up
				</button>
			</a>

			<button on:click={() => isOpenMenu = !isOpenMenu} data-dropdown-toggle="dropdown" class="ml-3 text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-4 py-2.5 text-center inline-flex items-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800" type="button">Unknown Unknown <svg class="w-4 h-4 ml-2" aria-hidden="true" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg></button>
			<!-- Dropdown menu -->
			<div class={`${isOpenMenu ? "":'hidden'} absolute top-16 right-0 z-10 bg-white divide-y divide-gray-100 rounded-lg shadow w-44 dark:bg-gray-700`}>
				<ul class="py-2 text-sm text-gray-700 dark:text-gray-200">
					<li>
						<a href="/profile" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">Profile</a>
					</li>
					<li>
						<a href="/" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">Sign out</a>
					</li>
				</ul>
			</div>
		</div>
	</div>
</nav>
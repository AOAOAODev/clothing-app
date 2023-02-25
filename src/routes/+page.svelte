<script>
    import { Card, Button, Rating, Badge } from "flowbite-svelte";
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte'
    import { DarkMode } from 'flowbite-svelte';
    import "@fortawesome/fontawesome-free/css/all.min.css";
    import "@fortawesome/fontawesome-free/js/all.min.js";
    let btnClass = 'text-gray-500 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700 rounded-lg text-xl p-2';
    import { Drawer, CloseButton, Sidebar, SidebarBrand, SidebarCta, SidebarDropdownItem, SidebarDropdownWrapper, SidebarGroup, SidebarItem, SidebarWrapper } from 'flowbite-svelte';
    import { sineIn } from 'svelte/easing';
    let hidden2 = true;
    let spanClass = 'flex-1 ml-3 whitespace-nowrap';
    let transitionParams = {
    x: -320,
    duration: 200,
    easing: sineIn
  };
</script>
<Navbar let:hidden let:toggle>
    <DarkMode {btnClass} />
    <NavBrand href="/">
      <img
        src="/img/applelogo.png"
        class="mr-3 h-6 sm:h-9"
        alt="Flowbite Logo"
      />
      <span class="self-center whitespace-nowrap text-xl font-semibold dark:text-white">
        HDCheap
      </span>
    </NavBrand>
    <div class="flex md:order-2">
        <Button on:click={() => (hidden2 = false)}>Get Started</Button>
        <NavHamburger on:click={toggle} />
      </div>      
    <NavUl {hidden} class="order-1">
      <NavLi href="/" active={true}>Home</NavLi>
      <NavLi href="/about">About</NavLi>
      <NavLi href="/services">Services</NavLi>
      <NavLi href="/pricing">Pricing</NavLi>
      <NavLi href="/contact">Contact</NavLi>
    </NavUl>
</Navbar>

<section class="bg-white dark:bg-gray-900">
    <div class="grid max-w-screen-xl px-4 py-8 mx-auto lg:gap-8 xl:gap-0 lg:py-16 lg:grid-cols-12">
        <div class="mr-auto place-self-center lg:col-span-7">
            <h1 class="max-w-2xl mb-4 text-4xl font-extrabold tracking-tight leading-none md:text-5xl xl:text-6xl dark:text-white">The Future Site To Buy Electronics HD</h1>
            <p class="max-w-2xl mb-6 font-light text-gray-500 lg:mb-8 md:text-lg lg:text-xl dark:text-gray-400">From checkout to global sales tax compliance, companies around the world use HDCHEAP to simplify their purchases.</p>
            <a href="#" class="inline-flex items-center justify-center px-5 py-3 mr-3 text-base font-medium text-center text-white rounded-lg bg-primary-700 hover:bg-primary-800 focus:ring-4 focus:ring-primary-300 dark:focus:ring-primary-900">
                Get started
                <svg class="w-5 h-5 ml-2 -mr-1" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10.293 3.293a1 1 0 011.414 0l6 6a1 1 0 010 1.414l-6 6a1 1 0 01-1.414-1.414L14.586 11H3a1 1 0 110-2h11.586l-4.293-4.293a1 1 0 010-1.414z" clip-rule="evenodd"></path></svg>
            </a>
            <a href="#" class="inline-flex items-center justify-center px-5 py-3 text-base font-medium text-center text-gray-900 border border-gray-300 rounded-lg hover:bg-gray-100 focus:ring-4 focus:ring-gray-100 dark:text-white dark:border-gray-700 dark:hover:bg-gray-700 dark:focus:ring-gray-800">
                Connect With Us!
            </a> 
        </div>
        <div class="hidden lg:mt-0 lg:col-span-5 lg:flex animate-pulse">
            <img src="/img/appleproducts.png"alt="mockup">
        </div>                
    </div>
</section>
  <Drawer transitionType="fly" {transitionParams} bind:hidden={hidden2} id='sidebar2'>
  <div class='flex items-center'>
    <h5 id="drawer-navigation-label-3" class="text-base font-semibold text-gray-500 uppercase dark:text-gray-400">Menu</h5>
    <CloseButton on:click={() => (hidden2 = true)} class='mb-4 dark:text-white'/>
  </div>
    <Sidebar>
      <SidebarWrapper divClass='overflow-y-auto py-4 px-3 rounded dark:bg-gray-800'>
        <SidebarGroup>
          <SidebarItem label="Dashboard">
            <svelte:fragment slot="icon">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6"><path stroke-linecap="round" stroke-linejoin="round" d="M10.5 6a7.5 7.5 0 107.5 7.5h-7.5V6z" /><path stroke-linecap="round" stroke-linejoin="round" d="M13.5 10.5H21A7.5 7.5 0 0013.5 3v7.5z" /></svg>
            </svelte:fragment>
          </SidebarItem>
          <SidebarDropdownWrapper label="E-commerce">
            <svelte:fragment slot="icon">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6"><path stroke-linecap="round" stroke-linejoin="round" d="M2.25 3h1.386c.51 0 .955.343 1.087.835l.383 1.437M7.5 14.25a3 3 0 00-3 3h15.75m-12.75-3h11.218c1.121-2.3 2.1-4.684 2.924-7.138a60.114 60.114 0 00-16.536-1.84M7.5 14.25L5.106 5.272M6 20.25a.75.75 0 11-1.5 0 .75.75 0 011.5 0zm12.75 0a.75.75 0 11-1.5 0 .75.75 0 011.5 0z" /></svg>
            </svelte:fragment>
            <SidebarDropdownItem label="Products" />
            <SidebarDropdownItem label="Billing" />
            <SidebarDropdownItem label="Invoice" />
          </SidebarDropdownWrapper>
          <SidebarItem label="Kanban" {spanClass}>
            <svelte:fragment slot="icon">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6"><path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6A2.25 2.25 0 016 3.75h2.25A2.25 2.25 0 0110.5 6v2.25a2.25 2.25 0 01-2.25 2.25H6a2.25 2.25 0 01-2.25-2.25V6zM3.75 15.75A2.25 2.25 0 016 13.5h2.25a2.25 2.25 0 012.25 2.25V18a2.25 2.25 0 01-2.25 2.25H6A2.25 2.25 0 013.75 18v-2.25zM13.5 6a2.25 2.25 0 012.25-2.25H18A2.25 2.25 0 0120.25 6v2.25A2.25 2.25 0 0118 10.5h-2.25a2.25 2.25 0 01-2.25-2.25V6zM13.5 15.75a2.25 2.25 0 012.25-2.25H18a2.25 2.25 0 012.25 2.25V18A2.25 2.25 0 0118 20.25h-2.25A2.25 2.25 0 0113.5 18v-2.25z" /></svg>
            </svelte:fragment>
            <svelte:fragment slot="subtext">
              <span
                class="inline-flex justify-center items-center px-2 ml-3 text-sm font-medium text-gray-800 bg-gray-200 rounded-full dark:bg-gray-700 dark:text-gray-300"
                >Pro</span>
            </svelte:fragment>
          </SidebarItem>
          <SidebarItem label="Inbox" {spanClass}>
            <svelte:fragment slot="icon">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6"><path stroke-linecap="round" stroke-linejoin="round" d="M9 3.75H6.912a2.25 2.25 0 00-2.15 1.588L2.35 13.177a2.25 2.25 0 00-.1.661V18a2.25 2.25 0 002.25 2.25h15A2.25 2.25 0 0021.75 18v-4.162c0-.224-.034-.447-.1-.661L19.24 5.338a2.25 2.25 0 00-2.15-1.588H15M2.25 13.5h3.86a2.25 2.25 0 012.012 1.244l.256.512a2.25 2.25 0 002.013 1.244h3.218a2.25 2.25 0 002.013-1.244l.256-.512a2.25 2.25 0 012.013-1.244h3.859M12 3v8.25m0 0l-3-3m3 3l3-3" /></svg>
            </svelte:fragment>
            <svelte:fragment slot="subtext">
              <span
                class="inline-flex justify-center items-center p-3 ml-3 w-3 h-3 text-sm font-medium text-blue-600 bg-blue-200 rounded-full dark:bg-blue-900 dark:text-blue-200"
                >3</span>
            </svelte:fragment>
          </SidebarItem>
          <SidebarItem label="Users">
            <svelte:fragment slot="icon">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6"><path stroke-linecap="round" stroke-linejoin="round" d="M15.75 6a3.75 3.75 0 11-7.5 0 3.75 3.75 0 017.5 0zM4.501 20.118a7.5 7.5 0 0114.998 0A17.933 17.933 0 0112 21.75c-2.676 0-5.216-.584-7.499-1.632z" /></svg>
            </svelte:fragment>
          </SidebarItem>
          <SidebarItem label="Sign In">
            <svelte:fragment slot="icon">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6"><path stroke-linecap="round" stroke-linejoin="round" d="M15.75 9V5.25A2.25 2.25 0 0013.5 3h-6a2.25 2.25 0 00-2.25 2.25v13.5A2.25 2.25 0 007.5 21h6a2.25 2.25 0 002.25-2.25V15M12 9l-3 3m0 0l3 3m-3-3h12.75" /></svg>
            </svelte:fragment>
          </SidebarItem>
          <SidebarItem label="Sign Up">
            <svelte:fragment slot="icon">
              <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6"><path stroke-linecap="round" stroke-linejoin="round" d="M4.5 12a7.5 7.5 0 0015 0m-15 0a7.5 7.5 0 1115 0m-15 0H3m16.5 0H21m-1.5 0H12m-8.457 3.077l1.41-.513m14.095-5.13l1.41-.513M5.106 17.785l1.15-.964m11.49-9.642l1.149-.964M7.501 19.795l.75-1.3m7.5-12.99l.75-1.3m-6.063 16.658l.26-1.477m2.605-14.772l.26-1.477m0 17.726l-.26-1.477M10.698 4.614l-.26-1.477M16.5 19.794l-.75-1.299M7.5 4.205L12 12m6.894 5.785l-1.149-.964M6.256 7.178l-1.15-.964m15.352 8.864l-1.41-.513M4.954 9.435l-1.41-.514M12.002 12l-3.75 6.495" /></svg>
            </svelte:fragment>
          </SidebarItem>
        </SidebarGroup>
      </SidebarWrapper>
    </Sidebar>
  </Drawer>
  
  
  <div class="flex flex-wrap justify-center gap-6 mt-10">
      <Card padding="none" class="card hover:translate-y-12">
          <a href="/">
              <img class="p-8 rounded-t-lg" src="/img/applewatch.png" alt="product 1" />
          </a>
          <div class="px-5 pb-5">
              <a href="/">
                  <h5 class='text-xl font-semibold tracking-tight text-gray-900 dark:text-white'>
                      Apple Watch Series 7 GPS, Aluminium Case, Starlight Sport
                  </h5>
              </a>
              <Rating rating={Number("4")} size="18" class="mt-2.5 mb-5">
                  <Badge slot="text" class="ml-3">4</Badge>
              </Rating>        
              <div class="flex justify-between items-center">
                  <span class="text-3xl font-bold text-gray-900 dark:text-white">$543</span>
                  <Button href="/">Buy now</Button>
              </div>
          </div>
      </Card>
      <Card padding="none" class="card">
          <a href="/">
              <img class="p-8 rounded-t-lg" src="/img/applewatch.png" alt="product 1" />
          </a>
          <div class="px-5 pb-5">
              <a href="/">
                  <h5 class='text-xl font-semibold tracking-tight text-gray-900 dark:text-white'>
                      Apple Watch Series 7 GPS, Aluminium Case, Starlight Sport
                  </h5>
              </a>
              <Rating rating={Number("4")} size="18" class="mt-2.5 mb-5">
                  <Badge slot="text" class="ml-3">4</Badge>
              </Rating>        
              <div class="flex justify-between items-center">
                  <span class="text-3xl font-bold text-gray-900 dark:text-white">$543</span>
                  <Button href="https://buy.stripe.com/test_fZe4gw28D3XIga4fYY">Buy now</Button>
              </div>
          </div>
      </Card>
      <Card padding="none" class="card">
          <a href="/">
              <img class="p-8 rounded-t-lg" src="/img/applewatch.png" alt="product 1" />
          </a>
          <div class="px-5 pb-5">
              <a href="/">
                  <h5 class='text-xl font-semibold tracking-tight text-gray-900 dark:text-white'>
                      Apple Watch Series 7 GPS, Aluminium Case, Starlight Sport
                  </h5>
              </a>
              <Rating rating={Number("4")} size="18" class="mt-2.5 mb-5">
                  <Badge slot="text" class="ml-3">4</Badge>
              </Rating>        
              <div class="flex justify-between items-center">
                  <span class="text-3xl font-bold text-gray-900 dark:text-white">$543</span>
                  <Button href="/">Buy now</Button>
              </div>
          </div>
      </Card>
  </div>
  

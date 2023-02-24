<script>
    import { Card, Button, Rating, Badge } from "flowbite-svelte";
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte'
    import { DarkMode } from 'flowbite-svelte';
    import "@fortawesome/fontawesome-free/css/all.min.css";
    import "@fortawesome/fontawesome-free/js/all.min.js";
    let btnClass = 'text-gray-500 dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700 rounded-lg text-xl p-2';
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
        <a href="form.html">
          <Button size="sm">Get started</Button>
        </a>
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
  
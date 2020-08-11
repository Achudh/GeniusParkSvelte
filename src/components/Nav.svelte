<script>
  import Hamburguer from "./Hamburguer.svelte";
  import NavLink from "./NavLink.svelte";

  export let segment;
  let expand = false;

  function toggleMobileMenu(event) {
    expand = event.detail;
  }
</script>

<nav
  class="w-full flex items-center justify-between flex-wrap bg-white p-6
  shadow-lg lg:fixed lg:top-0 z-50">

  <a href="." class="font-semibold text-xl tracking-tight mr-4">
    Genius Park Training Center
  </a>

  <div class="block lg:hidden">
    <Hamburguer on:click={toggleMobileMenu} {expand} />
  </div>
  <div class="w-full block flex-grow lg:flex lg:items-center lg:w-auto">
    <div class="{!expand && 'hidden'} lg:block lg:flex-grow">
      <NavLink text="Home" href="/" {segment} />
      <NavLink text="Courses" href="courses" {segment} />
      <NavLink text="Lessons" href="lessons" {segment} />
      <NavLink text="Services" href="serivices" {segment} />
      <NavLink text="Blog" href="blog" {segment} rel="prefetch" />
      <NavLink text="Contact Us" href="contact" {segment} />
      <NavLink text="About" href="about" {segment} />
    </div>
  </div>
</nav>

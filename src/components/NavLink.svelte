<script>
  export let segment;
  export let href;
  export let text;
  export let rel = "";
</script>

<a
  {rel}
  {href}
  class="block mt-4 lg:mx-4 lg:inline-block lg:mt-0 {segment === href ? 'text-grey-400' : 'text-black'}
  hover:text-gray-600 text-sm xxxsm:text-xs sm:text-sm md:text-base xxl:text-lg
  xxxl:text-xl">
  {text}
</a>

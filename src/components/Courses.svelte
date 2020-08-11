<script>
  import CourseCard from "./CourseCard.svelte";
</script>

<style>
  .h-80vh {
    height: 80vh;
  }
  /* .w-80vw {
    width: 80vw;
  } */
  .h-50vh {
    height: 50vh;
  }
  .w-50vw {
    width: 50vw;
  }
</style>

<svelte:head>
  <title>Courses</title>
</svelte:head>
<div
  class="h-80vh w-full lg:h-50vh lg:w-50vw flex flex-col px-3 mx-auto my-auto
  items-center">
  <!-- <h1 class="text-2xl sm:text-3xl lg:text-4xl my-4 font-bold text-center">
    Our Courses
  </h1> -->
  <div class="w-4/5 flex text-center">
    <div class="flex-1 mx-auto my-auto">
      <div class="flex flex-row">
        <div class="w-2/4 py-2 px-auto px-6" style="background: #74CEE4">
          <p class="text-white font-bold">DOWLOAD AREA</p>
          <p />
          &nbsp;
          <p class="text-white">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nesciunt,
            magni. Totam, nisi commodi repellendus
          </p>
          <button
            class="rounded-lg w-32 my-5 mx-auto px-2 py-2 bg-transparent
            text-white border-2 shadow-lg">
            Hello
          </button>
        </div>
        <div class="w-2/4 py-2 px-auto px-6 bg-orange-400">
          <div class="flex flex-col">
            <div>
              <p class="text-white font-bold">OPENING HOURS</p>
            </div>
            <div class="flex flex-row justify-between my-3 text-white">
              <div>Mon - Fri</div>
              <div>8 - 17:30</div>
            </div>
            <div class="h-xxxsm rounded-full bg-gray-300" />
            <div class="flex flex-row justify-between my-3 text-white">
              <div>Saturday</div>
              <div>9 - 17:30</div>
            </div>
            <div class="h-xxxsm rounded-full bg-gray-300" />
            <div class="flex flex-row justify-between my-3 text-white">
              <div>Sunday</div>
              <div>9 - 17:30</div>
            </div>
          </div>
        </div>
        <div />
      </div>
    </div>
    <div class="flex-1">
      <div class="flex flex-col text-left mx-8 my-6">
        <div class="text-gray-700 font-medium text-3xl">Find Your Course</div>
        <div class="flex flex-row justify-between my-3">
          <select
            name="Levels"
            class="block appearance-none w-2/5 bg-gray-200 border
            border-gray-200 text-gray-700 py-3 px-4 pr-8 rounded leading-tight
            focus:outline-none focus:bg-white focus:border-gray-500
            cursor-pointer mx-4"
            placeholder="Levels">
            <option value="0">All Levels</option>
            <option value="1">1</option>
            <option value="2">2</option>
            <option value="3">3</option>
            <option value="4">4</option>
            <option value="5">5</option>
          </select>
          <select
            name="Categories"
            class="block appearance-none w-2/5 bg-gray-200 border
            border-gray-200 text-gray-700 py-3 px-4 pr-8 rounded leading-tight
            focus:outline-none focus:bg-white focus:border-gray-500
            cursor-pointer mx-4"
            placeholder="Categories">
            <option value="0">All Categories</option>
            <option value="1">1</option>
            <option value="2">2</option>
            <option value="3">3</option>
            <option value="4">4</option>
            <option value="5">5</option>
          </select>
          <select
            name="Locations"
            class="block appearance-none w-2/5 bg-gray-200 border
            border-gray-200 text-gray-700 py-3 px-4 pr-8 rounded leading-tight
            focus:outline-none focus:bg-white focus:border-gray-500
            cursor-pointer mx-4"
            placeholder="Locations">
            <option value="0">All Locations</option>
            <option value="1">1</option>
            <option value="2">2</option>
            <option value="3">3</option>
            <option value="4">4</option>
            <option value="5">5</option>
          </select>
        </div>
        <div class="flex flex-row justify-between my-3">
          <select
            name="Typologies"
            class="block appearance-none w-2/5 bg-gray-200 border
            border-gray-200 text-gray-700 py-3 px-4 pr-8 rounded leading-tight
            focus:outline-none focus:bg-white focus:border-gray-500
            cursor-pointer mx-4"
            placeholder="Typologies">
            <option value="0">All Typologies</option>
            <option value="1">1</option>
            <option value="2">2</option>
            <option value="3">3</option>
            <option value="4">4</option>
            <option value="5">5</option>
          </select>
          <select
            name="Duriations"
            class="block appearance-none w-2/5 bg-gray-200 border
            border-gray-200 text-gray-700 py-3 px-4 pr-8 rounded leading-tight
            focus:outline-none focus:bg-white focus:border-gray-500
            cursor-pointer mx-4"
            placeholder="Duriations">
            <option value="0">All Duriations</option>
            <option value="1">1</option>
            <option value="2">2</option>
            <option value="3">3</option>
            <option value="4">4</option>
            <option value="5">5</option>
          </select>
          <button
            class="block appearance-none bg-orange-400 rounded leading-tight
            w-2/5 py-3 px-4 cursor-pointer mx-4">
            Search
          </button>
        </div>
      </div>

    </div>
  </div>
  <div class="flex flex-col w-full">
    <h2 class="font-medium text-6xl text-gray-700 text-left mx-40 my-32">
      Our Courses
      <h4 class="text-base font-medium text-gray-500 text-left mx-3">
        THE BEST IN OUR SCHOOL
      </h4>
    </h2>
    <div class="flex flex-row justify-between w-3/5">
      {#each Array(3) as _, j}
        <div class="flex flex-row">
          <CourseCard />
        </div>
      {/each}
      {#each Array(3) as _, j}
        <div class="flex flex-row">
          <CourseCard />
        </div>
      {/each}
    </div>
  </div>
</div>

<template>
  <section
    class="flex flex-col justify-start items-center text-neutral-800 py-[60px]">
    <h2 class="text-[40px] w-[100%] text-center mb-10 font-bold leading-[50px]">
      Teams
    </h2>

    <ul
      class="flex flex-col justify-start items-center w-full max-w-[1200px] mx-auto md:flex-row flex-wrap px-5">
      <li
        class="relative flex flex-col justify-center items-center w-full mb-16 shadow-md drop-shadow-md rounded-xl">
        <img
          src="https://images.teamtailor-cdn.com/images/s3/teamtailor-production/user_picture_800_crop-v3/image_uploads/d36f30a6-c043-4e71-acbd-5fef5d2bd3d1/original.jpg"
          class="rounded-xl" />
        <div class="courtain absolute top-0 left-0 w-full h-full rounded-xl">
          <span
            class="absolute bottom-5 left-5 px-5 text-white font-bold text-2xl">
            Technology
          </span>
        </div>
      </li>

      <li
        class="relative flex flex-col justify-center items-center w-full mb-10 shadow-md drop-shadow-md rounded-xl">
        <img
          src="https://images.teamtailor-cdn.com/images/s3/teamtailor-production/user_picture_800_crop-v3/image_uploads/f79d9bf1-501f-4ee8-baf9-465fb7302a0b/original.jpg"
          class="rounded-xl" />
        <div class="courtain absolute top-0 left-0 w-full h-full rounded-xl">
          <span
            class="absolute bottom-5 left-5 px-5 text-white font-bold text-2xl">
            Revenue
          </span>
        </div>
      </li>

      <li
        class="relative flex flex-col justify-center items-center w-full shadow-md drop-shadow-md rounded-xl">
        <img
          src="https://images.teamtailor-cdn.com/images/s3/teamtailor-production/user_picture_800_crop-v3/image_uploads/147579bc-87cd-4f83-85b6-2e09908db316/original.jpg"
          class="rounded-xl" />
        <div class="courtain absolute top-0 left-0 w-full h-full rounded-xl">
          <span
            class="absolute bottom-5 left-5 px-5 text-white font-bold text-2xl">
            Strategy
          </span>
        </div>
      </li>
    </ul>

    <button
      class="flex flex-row justify-evenly items-center mt-12 px-7 py-4 bg-neutral-800 shadow-md drop-shadow-md rounded-md text-white min-w-[220px]">
      <span>All Teams</span>
      <span class="text-white w-">
        
      </span>
    </button>
  </section>
</template>

<style scoped>
section {
  font-family: 'Rubik', sans-serif;
}

.courtain {
  background-color: rgba(0, 0, 0, 0.164);
}
</style>

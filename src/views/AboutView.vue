<script setup>
const cardOptions = [
  {
    title: "Бесплатный выпуск",
    icon: "free.svg",
  },
  {
    title: "До 100 млн. сум",
    icon: "books.svg",
  },
  {
    title: "55 дней без процентов",
    icon: "casca.svg",
  },
  {
    title: "Работает в любой точке мира",
    icon: "idea.svg",
  },
];
</script>
<template>
  <div class="view py-9 px-[18px]">
    <header
      class="flex items-center justify-between dark:text-white px-5 pt-8 pb-5"
    >
      <h2 class="font-bold text-[22px]">Кредитная карта.</h2>
      <button
        class="w-[30px] h-[30px] rounded-3xl bg-[#EEF2F6] dark:bg-[#314151] text-xl flex items-center justify-center"
        @click="$router.push('/')"
      >
        <img src="/icons/close.svg" alt="">
      </button>
    </header>
    <article>
      <p class="px-5 dark:text-white">
        На сегодняшний день это самая удобная и самая современная карта. Будь в
        тренде!
      </p>
      <iframe
        src="https://3d-card-view.netlify.app/"
        frameborder="0"
        class="my-5 w-full aspect-[3/2]"
      ></iframe>
    </article>
    <article>
      <div class="mx-auto">
        <div
          class="mt-6 grid grid-cols-2 gap-[10px] sm:grid-cols-2 lg:grid-cols-4 xl:gap-x-8"
        >
          <div
            v-for="o in cardOptions"
            class="dark:bg-[#20303F] border-[1px] border-[#E0E4E8] bg-[#F6F8F9] dark:border-none dark:shadow-[0_10px_40px_0_#0E1D28] rounded-[20px] p-5"
          >
            <span class="font-bold text-[16px] leading-normal text-[#333] dark:text-white"> {{ o.title }} </span>
            <div class="flex justify-between items-center mt-6">
              <span
                class="w-[30px] h-[30px] bg-white flex items-center justify-center rounded-[30px]"
              >
                <img src="/icons/check.svg" alt="" />
              </span>
              <img :src="`/icons/${o.icon}`" alt="" />
            </div>
          </div>
        </div>
        <div>
          <button type="button" class="w-full bg-[#3D9A73] my-5 p-4 rounded-[10px] text-white">Открыть карту</button>
        </div>
      </div>
    </article>
  </div>
</template>

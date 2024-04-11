<template>
  <section class="w-full flex p-10 gap-4 flex-col bg-orange text-white">
    <h2 class="font-bold text-3xl">{{ $t("search.main.visa.title") }}</h2>
    <div class="grid gap-4 grid-cols-4 grid-rows-2">
      <div
        v-for="(item, index) in items"
        :key="index"
        class="bg-white h-max hover:shadow-2xl group rounded-lg hover:rounded-t-lg hover:rounded-none gap-3 text-black relative p-2 flex flex-col"
      >
        <div class="rounded-lg overflow-hidden">
          <img :src="item.img" class="h-52 w-full" alt="..." />
        </div>

        <div class="flex flex-col gap-2 5">
          <h6 class="font-bold text-lg">{{ item.title }}</h6>
          <p class="text-gray-400">{{ item.body }}</p>
        </div>

        <div
          class="bg-white z-50 shadow-2xl group-hover:opacity-100 h-20 opacity-0 absolute transition-all duration-500 flex items-end -bottom-[4.5rem] left-0 right-0 rounded-b-lg p-2"
        >
          <button
            class="text-white p-0 h-0 group-hover:h-auto transition-all duration-500 bg-blue-500 rounded-lg group-hover:py-2 w-full"
          >
          {{ $t("search.main.visa.btn") }}
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const { t } = useI18n();
const items = ref([
  {
    title: t("search.main.visa.op1.title"),
    body: t("search.main.visa.op1.body"),
    img: "/img/search-img/visa-7.jpg",
  },
  {
    title: t("search.main.visa.op2.title"),
    body: t("search.main.visa.op2.body"),
    img: "/img/search-img/visa-4.jpg",
  },
  {
    title: t("search.main.visa.op3.title"),
    body: t("search.main.visa.op3.body"),
    img: "/img/search-img/visa-1.jpg",
  },
  {
    title: t("search.main.visa.op4.title"),
    body: t("search.main.visa.op4.body"),
    img: "/img/search-img/visa-8.jpg",
  },
  {
    title: t('search.main.visa.op5.title'),
    body: t('search.main.visa.op5.body'),
    img: "/img/search-img/visa-2.jpg",
  },
  {
    title:t('search.main.visa.op6.title'),
    body: t('search.main.visa.op6.body'),
    img: "/img/search-img/visa-6.jpg",
  },
  {
    title: t('search.main.visa.op7.title'),
    body: t('search.main.visa.op7.body'),
    img: "/img/search-img/visa-3.jpg",
  },
  {
    title: t('search.main.visa.op8.title'),
    body: t('search.main.visa.op8.body'),
    img: "/img/search-img/visa-5.jpg",
  },
]);
</script>

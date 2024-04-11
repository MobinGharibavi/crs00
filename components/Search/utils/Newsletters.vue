<template>
  <div
    class="max-w-7xl mx-auto gap-5 w-full py-16 bg-orange text-white rounded-2xl flex flex-col justify-center items-center"
  >
    <h3 class="text-2xl font-bold">
      {{ $t("search.main.news_letter.title") }}
    </h3>
    <p>
      {{ $t("search.main.news_letter.description") }}
    </p>

    <div class="flex items-center">
      <div class="bg-orange-400 w-96 py-2 px-5 rounded-l-lg rtl:rounded-r-lg">
        <input
          class="bg-transparent outline-none placeholder:text-white w-full"
          type="text"
          :placeholder="t('search.main.news_letter.email_title')"
        />
      </div>
      <button class="text-black px-3 py-2 -mr-2 bg-white rounded-lg">
        {{ $t("search.main.news_letter.button") }}
      </button>
    </div>
  </div>
</template>

<script setup>
const { t } = useI18n();
</script>

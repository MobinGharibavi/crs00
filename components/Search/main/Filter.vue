<template>
  <div class="flex items-center justify-center gap-5 -mt-52 mb-10">
    <div class="flex flex-col gap-5">
      <div class="bg-white py-3 px-5 w-80 gap-2 rounded-lg flex flex-col">
        <h3>{{ $t("search.main.search_flight.title") }}</h3>
        <div class="flex gap-5 items-center">
          <!-- radio btn -->
          <div class="flex items-center gap-2">
            <input
              type="radio"
              id="org"
              name="flight"
              checked
              class="w-4 h-4"
            />
            <label for="org">{{
              $t("search.main.search_flight.options.op1")
            }}</label>
          </div>
          <div class="flex items-center gap-2">
            <input type="radio" name="flight" id="des" class="w-4 h-4" />
            <label for="des">{{
              $t("search.main.search_flight.options.op2")
            }}</label>
          </div>
        </div>

        <!-- change flight -->
        <div class="justify-center flex flex-col gap-3 relative mt-2">
          <div class="relative w-full flex">
            <input
              class="peer transition-all px-5 py-3 w-full text-lg text-gray-600 bg-white rounded-md border outline-blue-300 select-all"
              type="text"
              placeholder=" "
            />

            <label
              class="z-2 text-gray-500 pointer-events-none absolute left-5 inset-y-0 bg-white h-fit flex items-center select-none transition-all text-sm peer-focus:text-sm peer-placeholder-shown:text-lg px-1 peer-focus:px-1 peer-placeholder-shown:px-0 peer-placeholder-shown:bg-white m-0 peer-focus:m-0 peer-placeholder-shown:m-auto rtl:right-5 gap-2 peer-focus:w-max -translate-y-1/2 peer-focus:-translate-y-1/2 peer-placeholder-shown:translate-y-0"
            >
              <Icon name="carbon:circle-filled" size="1.2rem" />
              {{ $t("search.main.search_flight.origin") }}
            </label>
          </div>

          <button type="button" class="h-full">
            <Icon
              name="humbleicons:exchange-horizontal"
              class="w-[50px] text-gray-500 rotate-90 h-[50px] rounded-[50%] absolute bg-white border-2 right-5 rtl:right-auto rtl:left-5 -translate-y-1/2 top-1/2 p-3 flex z-50 justify-center items-center"
            />

            <div class="relative w-full flex">
              <input
                class="peer transition-all px-5 py-3 w-full text-lg text-gray-600 bg-white rounded-md border outline-blue-300 select-all"
                type="text"
                placeholder=" "
              />

              <label
                class="z-2 text-gray-500 gap-2 pointer-events-none absolute left-5 inset-y-0 bg-white h-fit flex items-center select-none transition-all text-sm peer-focus:text-sm peer-placeholder-shown:text-lg px-1 peer-focus:px-1 peer-placeholder-shown:px-0 peer-placeholder-shown:bg-white m-0 peer-focus:m-0 peer-placeholder-shown:m-auto rtl:right-5 peer-focus:w-max -translate-y-1/2 peer-focus:-translate-y-1/2 peer-placeholder-shown:translate-y-0"
              >
                <Icon name="mdi:location" />
                {{ $t("search.main.search_flight.destination") }}
              </label>
            </div>
          </button>
        </div>

        <div
          class="border rounded-lg flex gap-2 text-gray-500 cursor-pointer px-5 py-3"
        >
          <Icon name="simple-line-icons:calender" />
          <span>{{ $t("search.main.search_flight.departure_date") }}</span>
        </div>
        <div
          class="border rounded-lg flex gap-2 text-gray-500 cursor-pointer px-5 py-3"
        >
          <Icon name="mdi:users" />
          <span>{{ $t("search.main.search_flight.persons") }}</span>
        </div>

        <button
          class="bg-orange text-white rounded-xl flex items-center justify-center gap-1 font-semibold py-3"
        >
          <Icon name="ic:outline-search" />
          <span>{{ $t("search.main.search_flight.btn") }}</span>
        </button>
      </div>

      <div class="flex flex-col overflow-hidden rounded-t-xl">
        <!-- <img class="w-80" src="https://www.noavarantravel.com/uploads/tourpackages/istanbul-638270062804617017.jpg" alt=""> -->
        <img class="w-80" src="/img/search-img/visa.jpg" alt="" />

        <div
          class="bg-white rounded-t-3xl -mt-5 py-4 justify-center items-center flex flex-col"
        >
          <h4 class="text-orange font-bold text-xl">
            {{ $t("search.main.banner.title") }}
          </h4>
          <p>{{ $t("search.main.banner.body") }}</p>

          <p class="font-bold mt-5">
            <span class="text-orange">CRSTRIP</span>.COM
          </p>
        </div>
      </div>
    </div>

    <SearchMainSearchData />
  </div>
</template>

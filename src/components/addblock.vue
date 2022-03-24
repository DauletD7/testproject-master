<template>
  <div class="container mx-auto">
    <div class="inpValue">
      <input
        type="text"
        placeholder="Введите название..."
        class="
          inp-filter
          w-full
          my-5
          border border-green-400
          p-4
          rounded-xl
          text-2xl
        "
      />
      <div class="result"></div>
    </div>
    <div class="addBlock"></div>
    <button class="showMore bg-black text-white p-5 mx-auto block">
      Показать еще
    </button>
    <!-- <div class="coinFetch">
    </div> -->
  </div>
</template>
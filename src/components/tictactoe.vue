<template>
  <div class="container mx-auto my-10">
    <h1 class="text-3xl text-center font-bold mb-5">TicTacToe</h1>
    <p class="turn text-3xl font-bold"></p>
    <div class="flex flex-wrap w-2/3 mx-auto justify-center items-center">
      <div class="slot w-1/3 text-5xl p-4 text-center">&nbsp</div>
      <div class="slot w-1/3 text-5xl p-4 text-center border-r-4 border-l-4 border-black">&nbsp</div>
      <div class="slot w-1/3 text-5xl p-4 text-center">&nbsp</div>

      <div class="slot w-1/3 text-5xl p-4 text-center border-t-4 border-b-4 border-black">&nbsp</div>
      <div class="slot w-1/3 text-5xl p-4 text-center border-4 border-black">&nbsp</div>
      <div class="slot w-1/3 text-5xl p-4 text-center border-t-4 border-b-4 border-black">&nbsp</div>

      <div class="slot w-1/3 text-5xl p-4 text-center">&nbsp</div>
      <div class="slot w-1/3 text-5xl p-4 text-center border-r-4 border-l-4 border-black">&nbsp</div>
      <div class="slot w-1/3 text-5xl p-4 text-center">&nbsp</div>
    </div>
    <p class="result"></p>
  </div>
</template>

<script>
export default {
  name: "tictactoe"
}
</script>
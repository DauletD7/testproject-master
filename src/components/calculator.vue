<template>
  <div class="container mx-auto">
    <h1 class="text-3xl text-center my-10 font-bold">Calculator</h1>
    <div class="calculator mt-10 bg-gray-200 p-10 rounded-3xl">
      <p class="first-arr text-right text-3xl"></p>
      <div class="first-num font-bold">
        <input class="my-4 w-full p-5 rounded-2xl text-3xl text-center" readonly type="number" placeholder="0"/>
      </div>
      <div class="flex justify-center">
          <button class="w-1/4 mx-4 my-3 bg-yellow-500 text-white rounded-3xl p-5 text-3xl clean">C</button>
          <button class="w-1/4 mx-4 my-3 bg-yellow-500 text-white rounded-3xl p-5 text-3xl ce">CE</button>
      </div>
      <div class="flex flex-wrap justify-evenly">
          <button value="1" class="w-1/4 mx-4 my-3 bg-green-500 text-white num-c rounded-3xl p-5 text-3xl">1</button>
          <button value="2" class="w-1/4 mx-4 my-3 bg-green-500 text-white num-c rounded-3xl p-5 text-3xl">2</button>
          <button value="3" class="w-1/4 mx-4 my-3 bg-green-500 text-white num-c rounded-3xl p-5 text-3xl">3</button>
          <button value="4" class="w-1/4 mx-4 my-3 bg-green-500 text-white num-c rounded-3xl p-5 text-3xl">4</button>
          <button value="5" class="w-1/4 mx-4 my-3 bg-green-500 text-white num-c rounded-3xl p-5 text-3xl">5</button>
          <button value="6" class="w-1/4 mx-4 my-3 bg-green-500 text-white num-c rounded-3xl p-5 text-3xl">6</button>
          <button value="7" class="w-1/4 mx-4 my-3 bg-green-500 text-white num-c rounded-3xl p-5 text-3xl">7</button>
          <button value="8" class="w-1/4 mx-4 my-3 bg-green-500 text-white num-c rounded-3xl p-5 text-3xl">8</button>
          <button value="9" class="w-1/4 mx-4 my-3 bg-green-500 text-white num-c rounded-3xl p-5 text-3xl">9</button>
          <button value="0" class="w-1/4 mx-4 my-3 bg-green-500 text-white num-c rounded-3xl p-5 text-3xl">0</button>
          <button value="" class="w-1/4 mx-4 my-3 bg-yellow-500 rounded-3xl p-5 text-3xl plus">+</button>
          <button value="" class="w-1/4 mx-4 my-3 bg-yellow-500 rounded-3xl p-5 text-3xl minus">-</button>
          <button value="" class="w-1/4 mx-4 my-3 bg-yellow-500 rounded-3xl p-5 text-3xl times">X</button>
          <button value="" class="w-1/4 mx-4 my-3 bg-yellow-500 rounded-3xl p-5 text-3xl divide">/</button>
          <button value="" class="w-1/4 mx-4 my-3 bg-yellow-500 rounded-3xl p-5 text-3xl ravno">=</button>
      </div>
    </div>
  </div>
</template>
<template>
  <div>
    <h1 v-if="status === 1">{{ transfer }}</h1>
    <p v-else>{{ heading }}</p>
    <button @click="changeStatus()">Click me!</button>
    <div class="flex" v-for="item of arr" :key="item.id">
      <p>{{ item.id }}.</p>
      <h1>{{ item.surname }} {{ item.name }}</h1>
    </div>
    <div class="container mx-auto">
      <div class="flex justify-between mt-10">
        <h1 class="font-bold">Цвет</h1>
        <img
          v-if="image == 1"
          src="https://images.samsung.com/kz_ru/smartphones/galaxy-s22-ultra/buy/s22ultra_colorselection_burgundy_pc_220118.jpg?imwidth=480"
          alt=""
        />
        <img
          v-if="image == 2"
          src="https://images.samsung.com/kz_ru/smartphones/galaxy-s22-ultra/buy/s22ultra_colorselection_green_pc_220118.jpg?imwidth=480"
          alt=""
        />
        <img
          v-if="image == 3"
          src="https://images.samsung.com/kz_ru/smartphones/galaxy-s22-ultra/buy/s22ultra_colorselection_phantomblack_pc_220118.jpg?imwidth=480"
          alt=""
        />
        <img
          v-if="image == 4"
          src="https://images.samsung.com/kz_ru/smartphones/galaxy-s22-ultra/buy/s22ultra_colorselection_phantomwhite_pc_220118.jpg?imwidth=480"
          alt=""
        />
        <div class="flex justify-evenly">
          <div @click="image = 1">
            <div></div>
            <p>Бургунди</p>
          </div>
          <div @click="image = 2">
            <div></div>
            <p>Зелёный</p>
          </div>
          <div @click="image = 3">
            <div></div>
            <p>Черный фантом</p>
          </div>
          <div @click="image = 4">
            <div></div>
            <p>Белый фантом</p>
          </div>
        </div>
      </div>
      <p>{{ result }} тенге</p>
      <p @click="firstMethod()">+ {{ first }} тенге</p>
      <p @click="secondMethod()">+ {{ second }} тенге</p>
      <p @click="thirdMethod()">+ {{ third }} тенге</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Test",
  data() {
    return {
      heading: "Hello Vue!",
      image: 1,
      status: 1,
      first: 60000,
      second: 70000,
      third: 25000,
      result: 650000,
      arr: [
        {
          id: 1,
          name: "Mansur",
          surname: "Yolkin",
        },
        {
          id: 2,
          name: "Batyrkhan",
          surname: "Baurzhanuly",
        },
      ],
    };
  },
  props: ["transfer"],
  methods: {
    changeStatus() {
      if (this.status === 1) {
        this.status = 0;
      } else {
        this.status = 1;
      }
    },
    firstMethod() {
        this.result = 650000;
        this.result = this.result + this.first;
    },
    secondMethod() {
        this.result = 650000;
        this.result = this.result + this.second;
    },
    thirdMethod() {
        this.result = 650000;
        this.result = this.result + this.third;
    }
  },
};
</script>
<template>
  <div class="w-full h-screen flex justify-center items-center">
    <div class="h-96 flex flex-nowrap justify-start">
      <input type="radio" name="slide" id="c1" checked />
      <label
        for="c1"
        class="w-20 rounded-3xl bg-cover cursor-pointer overflow-hidden mx-[10px] flex items-end ease-in-out shadow-2xl"
        style="background-image: url('https://picsum.photos/id/12/600/600')"
      >
        <div class="text-white flex flex-nowrap">
          <div
            class="bg-[#223] rounded-[50%] w-[50px] flex justify-center items-center m-[15px]"
          >
            1
          </div>
          <div
            class="flex justify-center flex-col overflow-hidden h-[80px] w-[520px] opacity-0"
            :class="'opacity-1'"
          >
            <h4 class="uppercase">Winter</h4>
            <p class="text-[#b0b0ba] pt-[5px]">
              Winter has so much to offer - creative activities
            </p>
          </div>
        </div>
      </label>
      <input type="radio" name="slide" id="c2" class="hidden" />
      <label
        for="c2"
        class="w-20 rounded-3xl bg-cover cursor-pointer overflow-hidden mx-[10px] flex items-end ease-in-out shadow-2xl"
        style="
          background-image: url('https://picsum.photos/id/1006/600/600?grayscale&blur=2');
        "
      >
        <div class="text-white flex flex-nowrap">
          <div
            class="bg-[#223] rounded-[50%] w-[50px] flex justify-center items-center m-[15px]"
          >
            2
          </div>
          <div
            class="flex justify-center flex-col overflow-hidden h-[80px] w-[520px] opacity-0 transform translate-y-30 transition-all duration-300 ease-in-out transition-delay-300"
          >
            <h4 class="uppercase">Digital Technology</h4>
            <p class="text-[#b0b0ba] pt-[5px]">
              Gets better every day - stay tuned
            </p>
          </div>
        </div>
      </label>
      <input type="radio" name="slide" id="c3" />
      <label
        for="c3"
        class="w-20 rounded-3xl bg-cover cursor-pointer overflow-hidden m-[0 10px] flex items-end ease-in-out shadow-2xl"
        style="
          background-image: url('https://picsum.photos/id/1006/600/600?grayscale&blur=2');
        "
      >
        <div class="text-white flex flex-nowrap">
          <div
            class="bg-[#223] rounded-[50%] w-[50px] flex justify-center items-center m-[15px]"
          >
            3
          </div>
          <div
            class="flex justify-center flex-col overflow-hidden h-[80px] w-[520px] opacity-0 transform translate-y-30 transition-all duration-300 ease-in-out transition-delay-300"
          >
            <h4 class="uppercase">Globalization</h4>
            <p class="text-[#b0b0ba] pt-[5px]">
              Help people all over the world
            </p>
          </div>
        </div>
      </label>
      <input type="radio" name="slide" id="c4" />
      <label for="c4" class="card">
        <div class="row">
          <div class="icon">4</div>
          <div class="description">
            <h4>New technologies</h4>
            <p>Space engineering becomes more and more advanced</p>
          </div>
        </div>
      </label>
    </div>
  </div>
</template>

<script setup>
const isChecked = ref(true);

const toggle = () => {
  isChecked.value = !isChecked.value;
};
</script>

<style scoped>
.container {
  height: 400px;
  display: flex;
  flex-wrap: nowrap;
  justify-content: start;
}

.card {
  width: 80px;
  background-size: cover;
  cursor: pointer;
  overflow: hidden;
  border-radius: 2rem;
  margin: 0 10px;
  display: flex;
  align-items: flex-end;
  transition: 0.6s cubic-bezier(0.28, -0.03, 0, 0.99);
  box-shadow: 0px 10px 30px -5px rgba(0, 0, 0, 0.8);
}

.card > .row {
  color: white;
  display: flex;
  flex-wrap: nowrap;
}

.card > .row > .icon {
  background-color: #223;
  color: white;
  border-radius: 50%;
  width: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 15px;
}

.card > .row > .description {
  display: flex;
  justify-content: center;
  flex-direction: column;
  overflow: hidden;
  height: 80px;
  width: 520px;
  opacity: 0;
  transform: translateY(30px);
  transition-delay: 0.3s;
  transition: all 0.3s ease;
}

.description p {
  color: #b0b0ba;
  padding-top: 5px;
}
.description h4 {
  text-transform: uppercase;
}

input {
  display: none;
}

input:checked + label {
  width: 600px;
}

input:checked + label .description {
  opacity: 1 !important;
  transform: translateY(0px) !important;
}

.card[for="c1"] {
  background-image: url("https://picsum.photos/id/1005/600/600?grayscale&blur=2");
}
.card[for="c2"] {
  background-image: url("https://picsum.photos/id/1006/600/600?grayscale&blur=2");
}
.card[for="c3"] {
  background-image: url("https://picsum.photos/id/1011/600/600?grayscale&blur=2");
}
.card[for="c4"] {
  background-image: url("https://picsum.photos/id/1008/600/600?grayscale&blur=2");
}
</style>

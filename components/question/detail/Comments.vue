<template>
  <div>
    <div v-for="item,index in 6" :key="item.id" class="py-6 px-4" :class="index === 0 ? 'rounded solution-section shadow-lg' : 'border-b '">
        <div class="pb-4 flex items-center justify-end" v-if="index === 0">
            <span class="solution-text"><svg height="21" viewBox="0 0 21 21" width="21" xmlns="http://www.w3.org/2000/svg"><path d="m.5 5.5 3 3 8.028-8" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" transform="translate(5 6)"/></svg></span>
            <span class="solution-text">Solution</span>
        </div>
      <div class="flex">
        <div class="mr-4">
          <div class="flex flex-col justify-center items-center">
            <div
              class="text-lighten hover:bg-green-100 cursor-pointer hover:text-green-700 p-0.5 rounded-full transition duration-200"
            >
              <svg
                height="42"
                viewBox="0 0 21 21"
                width="42"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="m.5 4.5 4-4 4 4"
                  fill="none"
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  transform="translate(6 8)"
                />
              </svg>
            </div>
            <div class="f-16 text-lighten py-2">12</div>
            <div
              class="text-lighten hover:bg-red-100 cursor-pointer hover:text-red-700 p-0.5 rounded-full transition duration-200"
            >
              <svg
                height="42"
                viewBox="0 0 21 21"
                width="42"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="m8.5.5-4 4-4-4"
                  fill="none"
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  transform="translate(6 8)"
                />
              </svg>
            </div>
          </div>
        </div>
        <div class="w-full">
          <div class="f-15">
            <p>
              On further investigation, I've discovered this is due to a parent
              div not resizing when the child div does. Basically, the div
              getting elements added to it by the asynchronous data loading
              grows in height, but the parent wrapping around it (and the one
              that has the background color) does not.
            </p>
          </div>
          <div class="pt-5">
            <div class="flex items-center">
              <div
                class="question-avatar-bigger"
                :style="{
                  backgroundImage: `url('https://i.ytimg.com/vi/kjNCms3JPk0/maxresdefault.jpg')`,
                }"
              ></div>
              <div class="flex flex-col pl-2">
                <div>
                  <nuxt-link
                    class="f-semibold text-gray-900 hover:text-gray-700"
                    to="/test"
                    >Hasan Muzak</nuxt-link
                  >
                </div>
                <div class="f-12 flex items-center">
                  <span class="text-lighten">Student</span>
                </div>
              </div>
            </div>
          </div>
          <div class="mt-5">
            <BodyComments />
          </div>
        </div>
      </div>
      <div class="text-right">
        <span
          class="f-12 text-lighten hover:text-pink-600 transition duration-200 cursor-pointer"
          >Add a comment</span
        >
      </div>
    </div>
  </div>
</template>

<script>
import BodyComments from "./BodyComments.vue";

export default {
  name: "Comments",
  components: {
    BodyComments,
  },
};
</script>

<style scoped lang="less">
.solution-section {
    border: 1px solid #C5E1A5;
    .solution-text {
        font-weight: 500;
        font-size: 12px;
        color: #8BC34A;
    }
}
</style>

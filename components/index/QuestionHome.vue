<template>
  <div>
    <div v-for="item in 5" :key="item.id" class="mt-0 p-4 border-b border-r transition duration-200 hover:shadow-lg border-gray-00">
      <div class="flex items-center justify-between">
        <div class="flex items-center">
          <div
            class="question-avatar"
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
              <span class="text-lighten mx-2">
                <svg
                  width="12"
                  height="12"
                  viewBox="0 0 15 15"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M9.875 7.5C9.875 8.81168 8.81168 9.875 7.5 9.875C6.18832 9.875 5.125 8.81168 5.125 7.5C5.125 6.18832 6.18832 5.125 7.5 5.125C8.81168 5.125 9.875 6.18832 9.875 7.5Z"
                    fill="currentColor"
                  ></path>
                </svg>
              </span>
              <span class="text-lighten">asked 2 mins ago</span>
              <span class="text-lighten ml-2">
                <svg
                  width="12"
                  height="12"
                  viewBox="0 0 15 15"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M7.5 11C4.80285 11 2.52952 9.62184 1.09622 7.50001C2.52952 5.37816 4.80285 4 7.5 4C10.1971 4 12.4705 5.37816 13.9038 7.50001C12.4705 9.62183 10.1971 11 7.5 11ZM7.5 3C4.30786 3 1.65639 4.70638 0.0760002 7.23501C-0.0253338 7.39715 -0.0253334 7.60288 0.0760014 7.76501C1.65639 10.2936 4.30786 12 7.5 12C10.6921 12 13.3436 10.2936 14.924 7.76501C15.0253 7.60288 15.0253 7.39715 14.924 7.23501C13.3436 4.70638 10.6921 3 7.5 3ZM7.5 9.5C8.60457 9.5 9.5 8.60457 9.5 7.5C9.5 6.39543 8.60457 5.5 7.5 5.5C6.39543 5.5 5.5 6.39543 5.5 7.5C5.5 8.60457 6.39543 9.5 7.5 9.5Z"
                    fill="currentColor"
                    fill-rule="evenodd"
                    clip-rule="evenodd"
                  ></path>
                </svg>
              </span>
              <span class="text-lighten pl-1"> 2.1k </span>
            </div>
          </div>
        </div>
        <div>
          <a-tag color="#4CAF50">
            <div class="flex items-center">
              <span
                ><svg
                  width="15"
                  height="15"
                  viewBox="0 0 15 15"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M11.4669 3.72684C11.7558 3.91574 11.8369 4.30308 11.648 4.59198L7.39799 11.092C7.29783 11.2452 7.13556 11.3467 6.95402 11.3699C6.77247 11.3931 6.58989 11.3355 6.45446 11.2124L3.70446 8.71241C3.44905 8.48022 3.43023 8.08494 3.66242 7.82953C3.89461 7.57412 4.28989 7.55529 4.5453 7.78749L6.75292 9.79441L10.6018 3.90792C10.7907 3.61902 11.178 3.53795 11.4669 3.72684Z"
                    fill="currentColor"
                    fill-rule="evenodd"
                    clip-rule="evenodd"
                  ></path></svg
              ></span>
              <span>Solved</span>
            </div>
          </a-tag>
        </div>
      </div>
      <div class="pt-2">
        <div class="py-2">
          <nuxt-link class="title f-18" to="/question/detail/test"
            >React only re-rendering one setState but not the other</nuxt-link
          >
          <div class="pt-2">
            <a-tag>Javascript</a-tag>
            <a-tag color="pink">Nginx</a-tag>
            <a-tag>Netlify</a-tag>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "QuestionHome",
  methods: {},
};
</script>

<style scoped lang="less">
.followed-tag {
  background-color: #fff6f6;
  .action-body {
    &:hover {
      background-color: #fce4ec;
      border-radius: 6px;
    }
  }
}
.title {
  color: #ad1457;
  &:hover {
    color: #d81b60;
  }
}
.action-body {
  &:hover {
    background-color: #f8f8f8;
    border-radius: 6px;
  }
}
</style>

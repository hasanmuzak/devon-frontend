<template>
  <div class="detail-section">
    <div class="border-b pb-3">
      <h1 class="f-30 mb-0">
        React only re-rendering one setState but not the other
      </h1>
      <div class="flex items-center f-13">
        <span class="text-lighten">Asked 3 min ago</span>
        <span class="text-lighten mx-2"
          ><svg
            width="15"
            height="15"
            viewBox="0 0 15 15"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M9.875 7.5C9.875 8.81168 8.81168 9.875 7.5 9.875C6.18832 9.875 5.125 8.81168 5.125 7.5C5.125 6.18832 6.18832 5.125 7.5 5.125C8.81168 5.125 9.875 6.18832 9.875 7.5Z"
              fill="currentColor"
            ></path></svg
        ></span>
        <span class="text-lighten">Viewed 2.2k times</span>
      </div>
    </div>
    <div class="w-2/3 py-4">
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
              I'm running into this problem with a program I'm working on and I
              can't figure out the solution. Basically I have a webapp, on
              initial render the entire page is height X. There is a background
              color, and that color covers the full height of the page.
            </p>
            <p>
              Moments after the initial render, data is fetched asynchronously
              and added to the page. The data causes the total height of the
              page to get larger. Unfortunately, only the original height of the
              page shows the background color, below that the background becomes
              white.
            </p>
            <p>
              On further investigation, I've discovered this is due to a parent
              div not resizing when the child div does. Basically, the div
              getting elements added to it by the asynchronous data loading
              grows in height, but the parent wrapping around it (and the one
              that has the background color) does not.
            </p>
            <p>
              During my investigation, I have found a partial solution: set the
              "height" to "auto". The problem with this solution is when the
              page initially loads, the background color is only applied to the
              part of the page with actual content, rather than filling the
              screen. So if I have the height at "auto", the color is screwed up
              when the page first loads before correcting itself after the items
              are added, and if the height is "100%" then the color is screwed
              up after the items are added.
            </p>
            <div>
              <pre class="language-html">
            <code>
              {{ html_code }}
            </code>
          </pre>
            </div>
          </div>
          <div class="pt-3 flex items-center justify-between">
            <div>
              <a-tag color="pink">Javascript</a-tag>
              <a-tag>Nginx</a-tag>
              <a-tag>Reverse Proxy</a-tag>
            </div>

            <a-popover
              v-model="show_options"
              trigger="click"
              placement="bottom"
            >
              <div slot="content" style="width: 170px">
                <div>
                  <div
                    class="flex items-center p-2 cursor-pointer transition duration-200 hover:bg-gray-200 rounded"
                  >
                    <span class="text-gray-600"
                      ><svg
                        height="20"
                        viewBox="0 0 21 21"
                        width="20"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <g
                          fill="none"
                          fill-rule="evenodd"
                          stroke="currentColor"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          transform="translate(3 3)"
                        >
                          <path d="m11.5 4.5-3.978-4-4.022 4" />
                          <path d="m7.522.521v11.979" />
                          <path
                            d="m4.5 7.5h-2c-1.1045695 0-2 .8954305-2 2v4c0 1.1045695.8954305 2 2 2h10c1.1045695 0 2-.8954305 2-2v-4c0-1.1045695-.8954305-2-2-2h-2"
                          />
                        </g></svg
                    ></span>
                    <span class="pl-2 f-12 text-gray-600">Share</span>
                  </div>
                  <div
                    class="flex items-center p-2 cursor-pointer transition duration-200 hover:bg-gray-200 rounded"
                  >
                    <span class="text-gray-600"
                      ><svg
                        height="21"
                        viewBox="0 0 21 21"
                        width="21"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="m1.5.5h6c.55228475 0 1 .44771525 1 1v12l-4-4-4 4v-12c0-.55228475.44771525-1 1-1z"
                          fill="none"
                          stroke="currentColor"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          transform="translate(6 4)"
                        /></svg
                    ></span>
                    <span class="pl-2 f-12 text-gray-600">Add to bookmark</span>
                  </div>
                  <div
                    class="flex items-center p-2 cursor-pointer transition duration-200 hover:bg-gray-200 rounded"
                  >
                    <span class="text-gray-600"
                      ><svg
                        height="21"
                        viewBox="0 0 21 21"
                        width="21"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <g
                          fill="none"
                          fill-rule="evenodd"
                          stroke="currentColor"
                          stroke-linecap="round"
                          stroke-linejoin="round"
                          transform="translate(5 4)"
                        >
                          <path d="m.5 13.5v-11" />
                          <path
                            d="m.5 2.5c.66666667-1.33333333 1.66666667-2 3-2 2 0 2 2 4 2 1.33333333 0 2.33333333-.33333333 3-1v6c-.66666667.66666667-1.66666667 1-3 1-2 0-2-2-4-2-1.33333333 0-2.33333333.66666667-3 2z"
                          />
                        </g></svg
                    ></span>
                    <span class="pl-2 f-12 text-gray-600">Report</span>
                  </div>
                </div>
              </div>
              <div
                class="p-2 rounded-full cursor-pointer transition duration-200 hover:bg-gray-200"
              >
                <svg
                  height="21"
                  viewBox="0 0 21 21"
                  width="21"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <g fill="currentColor" fill-rule="evenodd">
                    <circle cx="10.5" cy="10.5" r="1" />
                    <circle cx="5.5" cy="10.5" r="1" />
                    <circle cx="15.5" cy="10.5" r="1" />
                  </g>
                </svg>
              </div>
            </a-popover>
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
          <div class="text-right">
            <span
              class="f-12 text-lighten hover:text-pink-600 transition duration-200 cursor-pointer"
              >Add a comment</span
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// Components
import BodyComments from "./BodyComments.vue";

export default {
  name: "QuestionDetailBody",
  data() {
    return {
      show_options: false,
      html_code: `<head>
    <title>Layout Test</title>
    <style>
        * {
            margin: 0;
            padding: 0;
        }
        html {
            height: 100%;
            margin: 0;
            padding: 0;
        }
        body {
            margin: 0;
            padding: 0;
            height: 100%;
        }
        #root {
            background-color: cyan;
            height: 100%;
        }

        #root > h1 {
            text-align: center;
        }
    </style>
</head>`,
    };
  },
  components: {
    BodyComments,
  },
};
</script>

<style scoped lang="less"></style>

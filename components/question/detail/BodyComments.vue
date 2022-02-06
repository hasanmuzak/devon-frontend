<template>
  <div>
    <div class="border-t p-2">
      <div
        v-for="(item, index) in 3"
        :key="item.id"
        class="comment f-14 pb-2 mb-2"
        :class="index !== 2 ? 'border-b' : ''"
      >
        <div class="flex">
          <div class="mr-3 flex">
            <span class="text-xs f-semibold" style="margin-top: 4px"> 1 </span>
            <div>
              <div>
                <svg
                  height="21"
                  viewBox="0 0 21 21"
                  width="21"
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
              <div>
                <svg
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
                  </g>
                </svg>
              </div>
            </div>
          </div>
          <div>
            <span class="text-pink-600 f-12 cursor-pointer f-semibold"
              >@Oxibital</span
            >
            <span class="text-lighten f-12">said :</span>
            In your solution, the picture is cropped. I need it to shrink. But
            thanks anyway.
            <span class="text-lighten f-12">- 12 mins ago</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="less"></style>

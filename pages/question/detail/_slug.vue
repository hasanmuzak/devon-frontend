<template>
  <div>
    <QuestionDetailBody />
    <div class="w-2/3">
      <div class="border-t pt-5">
        <div class="flex items-center justify-between mb-5">
          <h1 class="answer-title f-20 m-0">6 Answers</h1>
          <div>
            <a-radio-group v-model="choice" button-style="solid">
              <a-radio-button :value="1"> Best </a-radio-button>
              <a-radio-button :value="2"> Newer </a-radio-button>
              <a-radio-button :value="3"> Older </a-radio-button>
            </a-radio-group>
          </div>
        </div>
        <Comments />
      </div>
    </div>
  </div>
</template>

<script>
// Components
import QuestionDetailBody from "../../../components/question/detail/QuestionDetailBody.vue";
import Comments from "../../../components/question/detail/Comments.vue";

export default {
  components: { QuestionDetailBody, Comments },
  data() {
    return {
      choice: 1
    }
  },
};
</script>

<style></style>

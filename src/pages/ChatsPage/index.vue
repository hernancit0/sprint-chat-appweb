<template>
  <div class="chat-container" style="background-color: #DFCAE1; height: 88.6vh;">
    <PrettyChatWindow
        :projectId="projectId"
        :username="username"
        :secret="secret"
    />
  </div>
</template>

<style>
.ce-new-chat-button {
  width: 32px;
  position: relative;
  bottom: 22px;
}

.chat-container {
  padding: 100px;
  padding-top: 0;
  padding-block-end: 0;
}

</style>

<script>
import { PrettyChatWindow } from "react-chat-engine-pretty";
import { applyReactInVue } from "veaury";

export default {
  data() {
    return {
      projectId: import.meta.env.VITE_CHAT_ENGINE_PROJECT_ID,
    };
  },
  components: {
    PrettyChatWindow: applyReactInVue(PrettyChatWindow),
  },
  props: {
    username: {
      type: String,
      required: true,
    },
    secret: {
      type: String,
      required: true,
    },
  },
};
</script>
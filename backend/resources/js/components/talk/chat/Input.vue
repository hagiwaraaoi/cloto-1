<template>
    <div id="talk-chat-input">
      <button>
        写真
      </button>
      <form @submit.prevent="$emit('submit-chat', text)">
          <input name="text" type="text" placeholder="Aa" v-model="text">
      </form>
    </div>
</template>

<script>
export const ChatInputComponent = {
  data() {
    return {
      text: "", // 友達/友達申請一覧
    };
  },
};

export default ChatInputComponent;
</script>

<style lang="scss" scoped>
#talk-chat-input {
  color: #fff;
  display: flex;
  justify-content: center;
  position: sticky;
  bottom: 0;
  width: 100%;
  background-color: #333;
  padding: .5rem .5rem 1.5rem;
  > * {
    margin-right: 1rem;
    :last-child{
      margin-right: 0;
    }
  }
  form{
    flex: 1 0 20rem;
    max-width: 80%;
  }
  input {
    width: 100%;
    padding: .5rem;
    background-color: #fff;
    color: #666;
    font-size: .9rem;
    outline: none;
    border-radius: .3rem;
  }
}
</style>
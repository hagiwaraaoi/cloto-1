<template>
  <div       
    id="text-message"    
    :class="{
      'text-message-left': chat.type === 'left',
      'text-message-right': chat.type === 'right',
    }">
    <v-list-item-avatar>
      <v-img :src="$storage('icon') + chat.user.icon"></v-img>
    </v-list-item-avatar>
    <v-list-item-content class="content-text">
      <small>{{chat.content}}</small>
    </v-list-item-content>
  </div>
</template>

<script>
export const TextMessageComponent = {
  props: {
    chat: Object
  }
};

export default TextMessageComponent;
</script>

<style lang="scss" scoped>
#text-message {
  display: flex;
}
.content-text{
  max-width: 20rem;
  display: inline-block;
  width: auto;
  box-shadow: 3px 3px 5px 0px rgb(51 51 51 / 22%);
  border-radius: .3rem;
  padding: .5rem;
}

.text-message-right{
  .v-avatar{
    margin-left: 10px;
    margin-right: 0px;
  }
  flex-direction: row-reverse;
}
</style>
<script>
import Message from './Message.vue';
export default {
  components: {
    Message,
  },

  data() {
    return {
      control: false,
      text: null,
    };
  },
  props: {
    companyName: {
      type: String,
      default: 'Widget',
    },
    textReply: {
      type: String,
      default: 'Typically replies within an hour',
    },
    messages: {
      type: Array,
      default: () => ['Hi there 👋 How can I help you ?'],
    },
    companyLogo: {
      type: String,
      default: '',
    },
    phoneNumber: {
      type: String,
      default: '',
    },
  },
  methods: {
    openLink() {
      let url = 'https://web.whatsapp.com/send';
      if (
        /Android|webOS|iPhone|iPad|Mac|Macintosh|iPod|BlackBerry|IEMobile|Opera Mini/i.test(
          navigator.userAgent
        )
      ) {
        url = 'whatsapp://send';
      }
      const all = url + '?phone=' + this.phoneNumber + `&text=${this.text}`;
      window.open(all, '_blank');
    },
  },
};
</script>
<template>
  <div id="wp-widget">
    <div v-if="control" id="whatsapp-chat" class="hidden">
      <div class="whatsapp-chat-header">
        <div class="whatsapp-chat-avatar">
          <img src="../assets/img/logo.png" />
        </div>
        <p class="whatsapp-chat-name-block">
          <span class="whatsapp-chat-name">{{ companyName }}</span
          ><br /><small>{{ textReply }}</small>
        </p>
      </div>

      <div class="start-chat">
        <div
          pattern="https://elfsight.com/assets/chats/patterns/whatsapp.png"
          class="WhatsappChat__Component-sc-Yvjha whatsapp-chat-body"
        >
          <Message :messages="messages" :companyName="companyName" />
        </div>

        <div class="blanter-msg">
          <textarea
            id="chat-input"
            placeholder="Write a response"
            maxlength="120"
            row="1"
            v-model="text"
          ></textarea>
          <button id="send-it" @click="openLink">
            <svg viewBox="0 0 448 448">
              <path d="M.213 32L0 181.333 320 224 0 266.667.213 416 448 224z" />
            </svg>
          </button>
        </div>
      </div>
      <a class="close-chat" @click="control = false">×</a>
    </div>
    <button
      class="blantershow-chat"
      title="Start Chat"
      @click="control = !control"
    >
      <svg width="30" viewBox="0 0 24 24">
        <defs />
        <path
          fill="#eceff1"
          d="M20.5 3.4A12.1 12.1 0 0012 0 12 12 0 001.7 17.8L0 24l6.3-1.7c2.8 1.5 5 1.4 5.8 1.5a12 12 0 008.4-20.3z"
        />
        <path
          fill="#4caf50"
          d="M12 21.8c-3.1 0-5.2-1.6-5.4-1.6l-3.7 1 1-3.7-.3-.4A9.9 9.9 0 012.1 12a10 10 0 0117-7 9.9 9.9 0 01-7 16.9z"
        />
        <path
          fill="#fafafa"
          d="M17.5 14.3c-.3 0-1.8-.8-2-.9-.7-.2-.5 0-1.7 1.3-.1.2-.3.2-.6.1s-1.3-.5-2.4-1.5a9 9 0 01-1.7-2c-.3-.6.4-.6 1-1.7l-.1-.5-1-2.2c-.2-.6-.4-.5-.6-.5-.6 0-1 0-1.4.3-1.6 1.8-1.2 3.6.2 5.6 2.7 3.5 4.2 4.2 6.8 5 .7.3 1.4.3 1.9.2.6 0 1.7-.7 2-1.4.3-.7.3-1.3.2-1.4-.1-.2-.3-.3-.6-.4z"
        />
      </svg>
    </button>
  </div>
</template>
<style scoped>
button {
  outline: none;
}
#wp-widget {
  font-family: --system-ui, 'Lato', sans-serif;
  background: #f1f1f1;
}
a:link,
a:visited {
  color: #444;
  text-decoration: none;
  transition: all 0.4s ease-in-out;
}
h1 {
  font-size: 20px;
  text-align: center;
  display: block;
  background: linear-gradient(to right top, #6f96f3, #164ed2);
  padding: 20px;
  color: #fff;
  border-radius: 50px;
}
/* CSS Multiple Whatsapp Chat */
#whatsapp-chat {
  box-sizing: border-box !important;
  outline: none !important;
  position: fixed;
  width: 350px;
  border-radius: 10px;
  box-shadow: 0 1px 15px rgba(32, 33, 36, 0.28);
  bottom: 90px;
  right: 30px;
  overflow: hidden;
  z-index: 99;
  animation-name: showchat;
  animation-duration: 1s;
  transform: scale(1);
}
button.blantershow-chat {
  /* background: #009688;
	 */
  background: #fff;
  color: #404040;
  position: fixed;
  display: flex;
  font-weight: 400;
  justify-content: space-between;
  z-index: 98;
  bottom: 25px;
  right: 30px;
  font-size: 15px;
  padding: 15px 15px;
  border-radius: 50%;
  border: 1px solid transparent;
  box-shadow: 0 10px 10px rgba(32, 33, 36, 0.28);
  cursor: pointer;
}
button.blantershow-chat svg {
  transform: scale(1.2);
}
.whatsapp-chat-header {
  background: #095e54;
  display: inline-flex;
  align-items: center;
  padding: 10px;
  height: 60px;
  width: 100%;
  height: 100%;
  color: #fff;
}
.companyLogo {
  border-radius: 100%;
  width: 50px;
  height: 50px;
  float: left;
  margin: 0 10px 0 0;
  border: 1px solid rgba(0, 0, 0, 0.2);
}
.whatsapp-chat-avatar {
  position: relative;
}
.whatsapp-chat-avatar::after {
  content: '';
  bottom: 0px;
  right: 0px;
  width: 12px;
  height: 12px;
  box-sizing: border-box;
  background-color: #4ad504;
  display: block;
  position: relative;
  z-index: 1;
  border-radius: 50%;
  border: 2px solid #095e54;
  left: 40px;
  top: 38px;
}
.whatsapp-chat-avatar img {
  border-radius: 100%;
  width: 50px;
  float: left;
  margin: 0 10px 0 0;
}
.whatsapp-chat-name-block {
  text-align: left;
}
.info-chat span {
  display: block;
}
#get-label,
span.chat-label {
  font-size: 12px;
  color: #888;
}
#get-nama,
span.chat-nama {
  margin: 5px 0 0;
  font-size: 15px;
  font-weight: 700;
  color: #222;
}
#get-label,
#get-nama {
  color: #fff;
}
span.my-number {
  display: block;
}
/* .blanter-msg {
	 color: #444;
	 padding: 20px;
	 font-size: 12.5px;
	 text-align: center;
	 border-top: 1px solid #ddd;
}
 */
textarea#chat-input {
  border: none;
  font-family: 'Arial', sans-serif;
  width: 100%;
  outline: none;
  resize: none;
  padding: 8px;
  font-size: 14px;
}
button#send-it {
  width: 30px;
  font-weight: 700;
  border-color: transparent;
  cursor: pointer;
  background: #eee;
}
button#send-it svg {
  fill: #a6a6a6;
  height: 20px;
  width: 20px;
}
.start-chat .blanter-msg {
  display: flex;
  height: 35px;
}
a.close-chat {
  position: absolute;
  top: 5px;
  right: 15px;
  color: #fff;
  font-size: 30px;
  cursor: pointer;
}
@keyframes ZpjSY {
  0% {
    background-color: #b6b5ba;
  }
  15% {
    background-color: #111;
  }
  25% {
    background-color: #b6b5ba;
  }
}
@keyframes hPhMsj {
  15% {
    background-color: #b6b5ba;
  }
  25% {
    background-color: #111;
  }
  35% {
    background-color: #b6b5ba;
  }
}
@keyframes iUMejp {
  25% {
    background-color: #b6b5ba;
  }
  35% {
    background-color: #111;
  }
  45% {
    background-color: #b6b5ba;
  }
}
@keyframes showhidden {
  from {
    transform: scale(0.5);
    opacity: 0;
  }
}
@keyframes showchat {
  from {
    transform: scale(0);
    opacity: 0;
  }
}
@media screen and (max-width: 480px) {
  #whatsapp-chat {
    width: auto;
    left: 5%;
    right: 5%;
    font-size: 80%;
  }
}
.hidden {
  display: block;
  animation-duration: 0.5s;
  transform: scale(1);
  opacity: 1;
}
.show {
  display: block;
  animation-name: showhidden;
  animation-duration: 0.5s;
  transform: scale(1);
  opacity: 1;
}
.whatsapp-chat-body {
  padding: 20px 20px 20px 10px;
  background-color: #e6ddd4;
  position: relative;
}
.whatsapp-chat-body::before {
  display: block;
  position: absolute;
  content: '';
  left: 0px;
  top: 0px;
  height: 100%;
  width: 100%;
  z-index: 0;
  opacity: 0.08;
  background-image: url('https://elfsight.com/assets/chats/patterns/whatsapp.png');
}
</style>

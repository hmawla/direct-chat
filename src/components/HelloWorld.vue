<template>
  <div id="GUIDGenerator">
    <div class="columns is-centered ">
      <div class="column is-5 is-vertical-centered">
        <h1 style="font-size: 2em; margin-bottom: 10px">WhatsApp Direct Chat</h1>
        <div class="field has-addons" style="margin: 20px">
          <a :href="'https://wa.me/' + phone">
            <button id="generateButton" class="control button is-medium is-primary is-rounded">
              Chat
            </button>
          </a>
          <div class="control" style="width:100%">
            <input ref="generator" v-model="phone" id="generator" class="input is-medium is-rounded" type="tel" placeholder="Phone">
          </div>
        </div>
        <div>
          Developed and designed by <a href="https://hmawla.com">hmawla.com</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      phone: '961'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
html {
  height: 100%;
}
body {
  height: 100%;
}
#GUIDGenerator {
  height: 100%;
}
.columns {
  height: 100%;
}
.columns.is-centered {
  justify-content: center;
  align-items: center;
}
#copyToClipboard {
  border-radius: 0px;
}
.underlined {
  text-decoration: underline;
}
#generateButton.is-rounded {
  border-top-right-radius: 0px;
  border-bottom-right-radius: 0px;
}
#generator.is-rounded {
  border-top-right-radius: 290486px;
  border-bottom-right-radius: 290486px;
}
/* Buefy snackbar css */
.notices {
  position: fixed;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 2em;
  overflow: hidden;
  z-index: 1000;
  pointer-events: none;
}

.notices .toast {
  display: -webkit-inline-box;
  display: -ms-inline-flexbox;
  display: inline-flex;
  -webkit-animation-duration: 150ms;
  animation-duration: 150ms;
  margin: 0.5em 0;
  text-align: center;
  -webkit-box-shadow: 0 1px 4px rgba(0, 0, 0, 0.12), 0 0 6px rgba(0, 0, 0, 0.04);
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.12), 0 0 6px rgba(0, 0, 0, 0.04);
  border-radius: 2em;
  padding: 0.75em 1.5em;
  pointer-events: auto;
  opacity: 0.92;
}

.notices .toast.is-white {
  color: #0a0a0a;
  background: white;
}

.notices .toast.is-black {
  color: white;
  background: #0a0a0a;
}

.notices .toast.is-light {
  color: #363636;
  background: whitesmoke;
}

.notices .toast.is-dark {
  color: whitesmoke;
  background: #363636;
}

.notices .toast.is-primary {
  color: white;
  background: #7957d5;
}

.notices .toast.is-link {
  color: white;
  background: #7957d5;
}

.notices .toast.is-info {
  color: #fff;
  background: #167df0;
}

.notices .toast.is-success {
  color: #fff;
  background: #23d160;
}

.notices .toast.is-warning {
  color: rgba(0, 0, 0, 0.7);
  background: #ffdd57;
}

.notices .toast.is-danger {
  color: #fff;
  background: #ff3860;
}

.notices .snackbar {
  display: -webkit-inline-box;
  display: -ms-inline-flexbox;
  display: inline-flex;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  -ms-flex-pack: distribute;
  justify-content: space-around;
  -webkit-animation-duration: 150ms;
  animation-duration: 150ms;
  margin: 0.5em 0;
  -webkit-box-shadow: 0 1px 4px rgba(0, 0, 0, 0.12), 0 0 6px rgba(0, 0, 0, 0.04);
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.12), 0 0 6px rgba(0, 0, 0, 0.04);
  border-radius: 3px;
  pointer-events: auto;
  background: #363636;
  color: whitesmoke;
  min-height: 3em;
}

.notices .snackbar .text {
  padding: 0.5em 1em;
}

.notices .snackbar .action {
  margin-left: auto;
  padding: 0.5em;
  padding-left: 0;
}

.notices .snackbar .action .button {
  font-weight: 600;
  text-transform: uppercase;
}

.notices .snackbar .action.is-white .button {
  color: white;
}

.notices .snackbar .action.is-black .button {
  color: #0a0a0a;
}

.notices .snackbar .action.is-light .button {
  color: whitesmoke;
}

.notices .snackbar .action.is-dark .button {
  color: #363636;
}

.notices .snackbar .action.is-primary .button {
  color: #7957d5;
}

.notices .snackbar .action.is-link .button {
  color: #7957d5;
}

.notices .snackbar .action.is-info .button {
  color: #167df0;
}

.notices .snackbar .action.is-success .button {
  color: #23d160;
}

.notices .snackbar .action.is-warning .button {
  color: #ffdd57;
}

.notices .snackbar .action.is-danger .button {
  color: #ff3860;
}

@media screen and (max-width: 768px) {
  .notices .snackbar {
    width: 100%;
    margin: 0;
    border-radius: 0;
  }
}

@media screen and (min-width: 769px), print {
  .notices .snackbar {
    min-width: 350px;
    max-width: 600px;
    overflow: hidden;
  }
}

.notices .toast.is-top,
.notices .snackbar.is-top {
  -ms-flex-item-align: center;
  align-self: center;
}

.notices .toast.is-top-right,
.notices .snackbar.is-top-right {
  -ms-flex-item-align: end;
  align-self: flex-end;
}

.notices .toast.is-bottom,
.notices .snackbar.is-bottom {
  -ms-flex-item-align: center;
  align-self: center;
}

.notices .toast.is-bottom-right,
.notices .snackbar.is-bottom-right {
  -ms-flex-item-align: end;
  align-self: flex-end;
}

.notices .toast.is-toast,
.notices .snackbar.is-toast {
  opacity: 0.92;
}

.notices.is-top {
  -webkit-box-orient: vertical;
  -webkit-box-direction: normal;
  -ms-flex-direction: column;
  flex-direction: column;
}

.notices.is-bottom {
  -webkit-box-orient: vertical;
  -webkit-box-direction: reverse;
  -ms-flex-direction: column-reverse;
  flex-direction: column-reverse;
}

.notices.has-custom-container {
  position: absolute;
}

@media screen and (max-width: 768px) {
  .notices {
    padding: 0;
    position: fixed !important;
  }
}

</style>

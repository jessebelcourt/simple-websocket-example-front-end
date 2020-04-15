<template>
  <div id="app">
    <h2>Basic WebSocket example</h2>

  </div>
</template>

<script>

export default {
  created() {
    let ws = new WebSocket("ws://localhost:40510");
    
    ws.onopen = () => {
      console.log('Websocket connection open');
      ws.send('Client is connected');
    }

    ws.onmessage = event => console.log(event);
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

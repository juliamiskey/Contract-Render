<template>
<!-- 
1.The implementation for getSentencesForTextBlock in api.js is complete and calculates all sentences from a TextBlock
2.The contract is retrieved from getContract in api.js and the contract's text is rendered as a document.
3.While hovering on text, the surrounding sentence should be highlighted in blue.
4.The user can select a single sentence on click, or multiple sentences on ctrl-click. The selected sentence(s) should be highlighted in red.
5.The user can click a button to clear their selection. The button should be disabled if no sentences are selected. -->
  <div id="app">
    <div class="container">
      <h1>Contract Render</h1>
      <getContract class="get-contract"/>
      <button 
        class="button"
        type="button"
        >
          Clear section
        </button>
    </div>
  </div>
</template>

<script>
import getContract from './components/getContract.vue'

export default {
  name: 'App',
  components: {
    getContract
  }
}
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: black;
    margin-top: 60px;
  }

  .container {
    margin: 0 auto;
    max-width: 850px;
    text-align: center;
  }

  .get-contract {
    text-align: left;
  }

  .text-clicked {
    background: red;
    color: black;
  }

  .button {
    background-color:grey;
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 1em 0;
  }
</style>

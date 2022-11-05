<template>
    <button :class="type">{{ text }}</button>
  </template>
  <script>
  export default {
    name: "Button",
    props: {
      text: {
        type: String,
        default: "",
      },
      type: {
        type: String,
        default: "primary",
      },

    },
  };
  </script>
  
  <style>
  button {
    padding: 10px 30px;
    border-radius: 20px;
    cursor: pointer;
    color:white;
    margin-top: 20px;
    margin-left: 5px;
    margin-right: 5px;
  }
  
  .primary {
    background: black;
    color: white;
    border: none;
  }
  button.primary:hover {
    background: blue;
  }
  
  button.outline {
    color: yellow;
    border: 1px solid white;
    background: transparent;

  }
  button.outline:hover {
    color: white;
    border: 1px solid blue;
    background: blue;
  }
  </style>
  
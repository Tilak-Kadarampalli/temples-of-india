<script>
    import { onMount } from 'svelte';
  
    let visited = false;
    let favorite = false;
    let message = '';
  
    function visit() {
      visited = !visited;
      showMessage(visited ? 'You visited this temple' : 'You unvisited this temple');
    }
  
    function fav() {
      favorite = !favorite;
      showMessage(favorite ? 'You added this temple to favorites' : 'You removed this temple from favorites');
    }
  
    function showMessage(msg) {
      message = msg;
      setTimeout(() => { message = ''; }, 2000);
    }
  
    onMount(() => {
      document.body.style.backgroundColor = 'transparent';
      document.body.style.color = 'black';
    });
  </script>
  
  <style>
    .container {
      display: flex;
      justify-content: space-around;
      padding: 20px;
      background-color: transparent;
      border:none;
    }
  
    .popup {
      position: fixed;
      top: 0;
      left: 50%;
      transform: translateX(-50%);
      background-color: green;
      color: #fff;
      padding: 10px;
      opacity: 0;
      transition: opacity 0.3s ease;
    }
  
    .popup.show {
      opacity: 1;
    }
  </style>
  
  <div class="container">
    <button on:click={visit}>
      {visited ? '🙏' : '🤲'} Visited
    </button>
    <button on:click={fav}>
      {favorite ? '❤️' : '🤍'} Favorite
    </button>
  </div>
  
  <div class="popup {message ? 'show' : ''}">
    {message}
  </div>
  
<!-- src/routes/index.svelte -->

<script>
    import { goto } from '$app/navigation';
  </script>
  
  <h1>Добро пожаловать в наш кинотеатр!</h1>
  
  <button on:click={() => goto('/movies')}>Посмотреть список фильмов</button>
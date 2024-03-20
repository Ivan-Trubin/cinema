<!-- src/routes/movies.svelte -->

<script context="module">
    // Заглушка данных о фильмах (ваш список фильмов)
    export const movies = [
      { title: 'Фильм 1', description: 'Описание фильма 1' },
      { title: 'Фильм 2', description: 'Описание фильма 2' },
      { title: 'Фильм 3', description: 'Описание фильма 3' },
      // Добавьте больше фильмов по вашему усмотрению
    ];
  </script>
  
  <script>
    import { onMount } from 'svelte';
  
    let title = 'Список фильмов';
    let moviesList = [];
  
    onMount(async () => {
      // Загрузка списка фильмов
      moviesList = movies;
    });
  </script>
  
  <svelte:head>
    <title>{title}</title>
  </svelte:head>
  
  <h2>{title}</h2>
  
  <ul>
    {#each moviesList as movie}
      <li><a href="movies/{encodeURIComponent(movie.title)}">{movie.title}</a></li>
    {/each}
  </ul>
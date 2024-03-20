<!-- src/routes/Movies.svelte -->

<script>
    // Заглушка данных о фильмах (ваш список фильмов)
    let movies = [
      { title: 'Фильм 1', description: 'Описание фильма 1' },
      { title: 'Фильм 2', description: 'Описание фильма 2' },
      { title: 'Фильм 3', description: 'Описание фильма 3' },
      // Добавьте больше фильмов по вашему усмотрению
    ];
  </script>
  
  <h2>Список фильмов:</h2>
  
  <ul>
    {#each movies as movie}
      <li><a href="/movies/{encodeURIComponent(movie.title)}">{movie.title}</a></li>
    {/each}
  </ul>
<!-- src/routes/movie-detail.svelte -->

<script context="module">
    export async function load({ params }) {
      // Получаем информацию о фильме из параметров маршрута
      const { title } = params;
      // Ваш код для загрузки информации о фильме по его названию
      const movie = { title: 'Фильм', description: 'Описание фильма' }; // Заглушка данных
      return { props: { movie } };
    }
  </script>
  
  <script>
    export let movie;
  
    function goBack() {
      history.back();
    }
  </script>
  
  <svelte:head>
    <title>{movie.title}</title>
  </svelte:head>
  
  <h2>{movie.title}</h2>
  <p>{movie.description}</p>
  
  <button on:click={goBack}>Назад</button>
<!-- src/routes/MovieDetail.svelte -->

<script context="module">
    export async function load({ params }) {
      // Получаем информацию о фильме из параметров маршрута
      const { title } = params;
      // Ваш код для загрузки информации о фильме по его названию
      const movie = { title: 'Фильм', description: 'Описание фильма' }; // Заглушка данных
      return { movie };
    }
  </script>
  
  <script>
    // Принимаем свойство movie, содержащее информацию о выбранном фильме
    export let movie = {};
  
    // Добавим функцию для обработки нажатия на ссылку назад
    function goBack() {
      history.back();
    }
  </script>
  
  <h2>{movie.title}</h2>
  <p>{movie.description}</p>
  
  <button on:click={goBack}>Назад</button>
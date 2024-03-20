<!-- src/routes/+layout.svelte -->

<script>
    export let title;
  </script>
  
  <main>
    <header>
      <h1>{title}</h1>
      <nav>
        <a href="/">Главная</a>
      </nav>
    </header>
    <slot></slot>
  </main>
  
  <style>
    main {
      max-width: 800px;
      margin: 0 auto;
      padding: 20px;
    }
  </style>
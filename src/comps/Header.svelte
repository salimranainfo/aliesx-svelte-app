<script>
  let showMenu = false;
</script>

<header>
  <div class="container">
    <img src="/img/logo.png" alt="" class="logo" />

    <!-- Mobile Menu -->

    <nav class="nav">
      <div class="nav-icon" on:click={() => (showMenu = !showMenu)}>
        <svg
          width="35"
          height="35"
          viewBox="0 0 35 35"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M29.2396 16.0417H5.76042C4.99527 16.0417 4.375 16.662 4.375 17.4272V17.573C4.375 18.3381 4.99527 18.9584 5.76042 18.9584H29.2396C30.0047 18.9584 30.625 18.3381 30.625 17.573V17.4272C30.625 16.662 30.0047 16.0417 29.2396 16.0417Z"
            fill="#4F4F4F"
          />
          <path
            d="M29.2396 23.3333H5.76042C4.99527 23.3333 4.375 23.9535 4.375 24.7187V24.8645C4.375 25.6296 4.99527 26.2499 5.76042 26.2499H29.2396C30.0047 26.2499 30.625 25.6296 30.625 24.8645V24.7187C30.625 23.9535 30.0047 23.3333 29.2396 23.3333Z"
            fill="#4F4F4F"
          />
          <path
            d="M29.2396 8.75H5.76042C4.99527 8.75 4.375 9.37027 4.375 10.1354V10.2813C4.375 11.0464 4.99527 11.6667 5.76042 11.6667H29.2396C30.0047 11.6667 30.625 11.0464 30.625 10.2813V10.1354C30.625 9.37027 30.0047 8.75 29.2396 8.75Z"
            fill="#4F4F4F"
          />
        </svg>
      </div>

      {#if showMenu}
        <ul class="nav-list">
          <li><a href="#!">L’offre AilesX</a></li>
          <li><a href="#!">Destinations</a></li>
          <li><a href="#!">Prix</a></li>
          <li><a href="#!">À propos</a></li>
          <li><a href="#!" class="nav-list-btn">Essayez!</a></li>
        </ul>
      {/if}
    </nav>
  </div>
</header>

<style>
  .container {
    padding: 0.75rem 1.5rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .logo {
    width: 4rem;
  }

  .nav {
    position: relative;
  }

  .nav-icon {
    cursor: pointer;
  }

  .nav-list {
    position: absolute;
    padding: 1rem;
    top: 100%;
    right: 0;
    border: 2px solid rgba(0, 0, 0, 0.25);
    box-shadow: 0 0 8px 1px rgba(0, 0, 0, 0.15);
    border-radius: 0.5rem;
  }

  .nav-list li a {
    display: inline-block;
    padding: 0.75rem 0.5rem;
    white-space: nowrap;
    width: 100%;
  }

  .nav-list li .nav-list-btn {
    background-color: #001944;
    color: white;
    text-align: center;
    border-radius: 0.75rem;
  }
</style>

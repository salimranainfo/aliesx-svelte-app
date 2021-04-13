<script>
  export let windowWidth;
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

      {#if showMenu || windowWidth >= 1024}
        <ul class="nav-list">
          <li>
            <button class="lang">
              <svg
                width="21"
                height="20"
                viewBox="0 0 21 20"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M20.5 10C20.5 8.68678 20.2413 7.38642 19.7388 6.17317C19.2362 4.95991 18.4997 3.85752 17.5711 2.92893C16.6425 2.00035 15.5401 1.26375 14.3268 0.761205C13.1136 0.258658 11.8132 0 10.5 0C7.84784 0 5.3043 1.05357 3.42893 2.92893C1.55357 4.8043 0.5 7.34784 0.5 10C0.5 12.6522 1.55357 15.1957 3.42893 17.0711C5.3043 18.9464 7.84784 20 10.5 20C13.1522 20 15.6957 18.9464 17.5711 17.0711C19.4464 15.1957 20.5 12.6522 20.5 10ZM18.43 9H15.5C15.3351 6.64814 14.5293 4.38635 13.17 2.46C14.5665 2.95597 15.7977 3.83007 16.7265 4.98484C17.6553 6.13962 18.245 7.52967 18.43 9ZM7.58 11H13.5C13.2441 13.4706 12.1911 15.7908 10.5 17.61C8.81007 15.7984 7.78119 13.4693 7.58 11ZM7.58 9C7.81289 6.54183 8.83759 4.22572 10.5 2.4C12.2047 4.20612 13.2601 6.52804 13.5 9H7.58ZM7.94 2.43C6.57355 4.36702 5.7548 6.63672 5.57 9H2.57C2.7589 7.5115 3.36261 6.10612 4.31217 4.94437C5.26172 3.78262 6.51886 2.91133 7.94 2.43ZM2.57 11H5.57C5.73469 13.3613 6.54788 15.6313 7.92 17.56C6.50397 17.0763 5.25199 16.2052 4.30627 15.0456C3.36055 13.886 2.75902 12.4844 2.57 11ZM13.12 17.55C14.4884 15.6207 15.3107 13.3577 15.5 11H18.45C18.2609 12.4802 17.6615 13.8781 16.7196 15.0356C15.7778 16.193 14.5309 17.064 13.12 17.55Z"
                  fill="#7C7C7C"
                />
              </svg>
              <svg
                width="11"
                height="5"
                viewBox="0 0 11 5"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M5.49999 4.66677C5.34422 4.66707 5.19327 4.61282 5.07332 4.51344L1.07332 1.1801C0.937179 1.06694 0.851563 0.904336 0.83531 0.728052C0.819057 0.551767 0.873498 0.376247 0.986657 0.240102C1.09982 0.103958 1.26242 0.0183417 1.43871 0.00208859C1.61499 -0.0141646 1.79051 0.0402764 1.92666 0.153435L5.49999 3.1401L9.07333 0.260103C9.14152 0.204725 9.21998 0.163371 9.30421 0.138416C9.38843 0.113462 9.47676 0.105399 9.56411 0.114692C9.65147 0.123985 9.73612 0.150449 9.81321 0.192565C9.8903 0.234681 9.95831 0.291618 10.0133 0.360102C10.0744 0.42865 10.1206 0.509068 10.1491 0.596317C10.1777 0.683566 10.1879 0.775766 10.1791 0.867142C10.1704 0.958517 10.1428 1.0471 10.0982 1.12734C10.0536 1.20757 9.99296 1.27774 9.91999 1.33344L5.91999 4.55344C5.7966 4.63711 5.64873 4.67702 5.49999 4.66677Z"
                  fill="black"
                />
              </svg>
            </button>
          </li>
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
  header {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background-color: white;
    z-index: 99;
  }

  .lang {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 0.25rem;
    padding: 0.75rem 0.5rem;
  }

  .container {
    padding: 0.75rem 1.5rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-shadow: 1px 0px 4px 1px rgba(0, 0, 0, 0.05);
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
    background-color: white;
    position: absolute;
    padding: 1rem;
    top: 100%;
    right: 0;
    border: 2px solid rgba(0, 0, 0, 0.25);
    box-shadow: 0 0 8px 1px rgba(0, 0, 0, 0.15);
    border-radius: 0.5rem;
    z-index: 100;
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

  @media (min-width: 1024px) {
    .nav-icon {
      display: none;
    }

    .nav-list {
      background-color: white;
      position: static;
      /* padding: 1rem; */
      display: flex;
      gap: 1rem;
      border: none;
      box-shadow: none;
      border-radius: 0;
      padding: 0;
    }

    .nav-list li a {
      display: inline-block;
      padding: 0.75rem 0.5rem;
      white-space: nowrap;
      width: 100%;
    }

    .nav-list li .nav-list-btn {
      padding: 0.5rem 0.75rem;
    }
  }

  /* 1200px and higher devices */
  @media (min-width: 1200px) {
    .container {
      width: 95%;
      margin-left: auto;
      margin-right: auto;
    }
  }

  /* 1600px and higher devices */
  @media (min-width: 1600px) {
    .container {
      width: 80%;
      margin-left: auto;
      margin-right: auto;
    }
  }
</style>

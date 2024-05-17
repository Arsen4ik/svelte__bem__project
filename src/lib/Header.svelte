<script>
  import { Link } from "svelte-routing";
</script>

<header class="header">
  <Link class="header__main__link" to="/">
    <img class="header__logo" src="/logo-light.svg" alt="" />
    <h1 class="header__title">Автошкола</h1>
  </Link>
  <ul class="header__links">
    <!-- <a data-sveltekit-preload-data="tap" href="#banner"
      ><li class="header__links__link">главная</li></a
    >
    <a data-sveltekit-preload-data="tap" href="#options"
      ><li class="header__links__link">опции</li></a
    >
    <li class="header__links__link">хз</li> -->
    <!-- <Link class="header__links__link" to="/">на главную</Link> -->
    <!-- <Link class="header__links__link" to="/contacts">контакты</Link> -->
    <Link class="header__links__link" to="/form">записаться</Link>
  </ul>
</header>

<style scoped lang="scss">
  .header {
    padding: 10px 50px;
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 12px;
    background-color: rgba(#3f3f46, 0.8);
    backdrop-filter: blur(8px);
    position: fixed;
    z-index: 10;
    width: 100vw;

    .header__title {
      color: var(--white-secondary-color);
    }

    .header__logo {
      width: 40px;
      height: 40px;
    }

    .header__links {
      margin-left: auto;
      display: flex;
      flex-direction: row;
      align-items: center;
      gap: 36px;
      list-style-type: none;

      & > :global(.header__links__link) {
        color: var(--white-secondary-color);
        transition: all 0.15s ease-in-out;
        text-decoration: underline;

        &:hover {
          transform: scale(1.1);
          cursor: pointer;
          color: var(--white-primary-color);
        }
      }
    }
  }
  :global(.header__main__link) {
    display: flex;
    flex-direction: row;
    gap: 16px;

    & > .header__title {
      transition: all 0.15s ease-in-out;
      color: var(--white-secondary-color);
      text-decoration: underline;
    }

    &:hover {
      cursor: pointer;

      & > .header__title {
        transform: scale(1.03);
        color: var(--white-primary-color);
      }
    }
  }
</style>

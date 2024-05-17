<script>
  import { Link } from "svelte-routing";
</script>

<section class="error">
  <p class="error__message">Упс...😵</p>
  <p class="error__status">404</p>
  <Link class="error__link" to="/">на главную</Link>
</section>

<style scoped lang="scss">
  .error {
    height: 100vh;
    display: flex;
    flex-direction: column;
    gap: 50px;
    justify-content: center;
    align-items: center;

    .error__message {
      font-size: xx-large;
    }
    .error__status {
      font-size: large;
      font-weight: bolder;
      color: var(--red-primary-color);
    }

    & > :global(.error__link) {
      color: var(--black-secondary-color);
      transition: all 0.15s ease-in-out;
      text-decoration: underline;

      &:hover {
        transform: scale(1.1);
        cursor: pointer;
        color: var(--black-primary-color);
      }
    }
  }
</style>

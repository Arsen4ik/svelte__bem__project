<script>
  const handleSubmit = (e) => {
    e.preventDefault();
    const formData = new FormData(e.target);
    const email = formData.get("email");
    console.log(email);
    if (
      !formData.get("email") ||
      !formData.get("name") ||
      !formData.get("category")
    ) {
      alert("заполните все поля");
    } else {
      alert(
        `${formData.get("name")}, когда-нибудь,на почту ${formData.get("email")} будет отправлено сообщение, в котором мы ответим, захотим ли мы вас видеть на получении прав по категории ${formData.get("category")}`
      );
      e.target.reset();
    }
  };
</script>

<section class="section">
  <form class="section__form" on:submit={handleSubmit}>
    <p class="section__form__title">Оставьте нам сообщение!</p>
    <input
      class="section__form__input"
      type="text"
      name="email"
      placeholder="почта"
    />
    <input
      class="section__form__input"
      type="text"
      name="name"
      placeholder="имя"
    />
    <input
      class="section__form__input"
      type="text"
      name="category"
      placeholder="выбранная категория"
    />
    <button class="section__form__button" type="submit">Отправить</button>
  </form>
</section>

<style scoped lang="scss">
  .section {
    position: relative;
    height: fit-content;
    padding: 120px 0;

    .section__form {
      background-color: var(--white-tertiary-color);
      padding: 30px;
      border-radius: 20px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      gap: 15px;
      margin: 0 auto;
      width: fit-content;

      .section__form__title {
        color: var(--black-secondary-color);
        font-weight: bold;
        font-size: x-large;
        text-align: center;
        margin-bottom: 15px;
      }

      .section__form__input {
        width: 400px;
        border-radius: 5px;
        border: 1px solid var(--white-secondary-color);
        padding: 5px;
        outline: none;
        color: var(--black-secondary-color);
        transition: all 0.15s ease-in-out;

        &:focus {
          border-color: var(--gray-primary-color);
        }
      }

      .section__form__button {
        width: 400px;
        background-color: var(--black-secondary-color);
        border-radius: 5px;
        border: none;
        padding: 5px;
        color: white;
        transition: all 0.15s ease-in-out;

        &:hover {
          background-color: var(--black-primary-color);
          cursor: pointer;
        }
      }
    }
  }
</style>

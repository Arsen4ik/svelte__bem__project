<section id="banner" class="section">
  <img class="banner__img" src="/car.jpg" alt="" />
  <p class="banner__text">
    <span class="banner__text__question">Фарш на колесиках?</span><br />
    <span class="banner__text__answer">- ДА!</span><br />
    <span>для начала...</span><br />
    <span class="banner__text__action">_получи права</span>
  </p>
</section>

<style lang="scss" scoped>
  .section {
    position: relative;
    height: fit-content;
    padding: 60px 0 0;
    background-color: var(--white-tertiary-color);
    box-shadow:
      0 10px 15px -3px rgb(0 0 0 / 0.1),
      0 4px 6px -4px rgb(0 0 0 / 0.1);

    .banner__img {
      width: 100%;
      height: 100%;
    }

    .banner__text {
      position: absolute;
      width: 100%;
      padding-left: 50px;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      top: 0;
      background-image: linear-gradient(
        to right,
        var(--white-primary-color) 20%,
        rgba(255, 255, 255, 0)
      );
      font-size: 40px;

      .banner__text__question {
        font-size: 50px;
        font-weight: 200;
      }

      .banner__text__answer {
        font-weight: 900;
        letter-spacing: 3px;
        -webkit-background-clip: text;
        background-clip: text;
        width: fit-content;
        -webkit-text-fill-color: transparent;
        /* background-image: linear-gradient(
          to bottom right,
          #60a5fa,
          #818cf8,
          #a78bfa
        ); */
        background-image: linear-gradient(
          to bottom right,
          #71717a 0% 20%,
          #a1a1aa 20% 40%,
          #d4d4d8 40% 60%,
          #e4e4e7 60% 80%,
          #f4f4f5 80%
        );
        /* background-image: linear-gradient(
          to right,
          #fecaca,
          #fdba74,
          #fbbf24,
          #facc15
        ); */
      }
      .banner__text__action {
        font-style: italic;
        color: var(--red-primary-color);
      }
    }
  }
</style>

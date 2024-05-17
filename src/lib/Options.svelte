<script>
  const categories = [
    {
      id: 1,
      name: "A",
      price: 123,
      vehicle: ["машина", "автобус"],
      time: 6,
      text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Cum quae exercitationem illum cumque facere nostrum! Earum magnam dolorem rem animi, exercitationem alias. Nemo nam laboriosam iusto corporis veniam dolorum ut. Excepturi, nostrum?",
    },
    {
      id: 2,
      name: "B",
      price: 14,
      vehicle: ["мотоцикл", "вертолет"],
      time: 0,
      text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Cum quae exercitationem illum cumque facere nostrum! Earum magnam dolorem rem animi, exercitationem alias. Nemo nam laboriosam iusto corporis veniam dolorum ut. Excepturi, nostrum?",
    },
    {
      id: 3,
      name: "C+",
      price: 55,
      vehicle: ["танк", "экскаватор", "камаз"],
      time: 5,
      text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Cum quae exercitationem illum cumque facere nostrum! Earum magnam dolorem rem animi, exercitationem alias. Nemo nam laboriosam iusto corporis veniam dolorum ut. Excepturi, nostrum?",
    },
    {
      id: 2,
      name: "D",
      price: 1,
      vehicle: ["квадроцикл", "звезда смерти", "что-то еще"],
      time: 2,
      text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Cum quae exercitationem illum cumque facere nostrum! Earum magnam dolorem rem animi, exercitationem alias. Nemo nam laboriosam iusto corporis veniam dolorum ut. Excepturi, nostrum?",
    },
    {
      id: 3,
      name: "E-",
      price: -3,
      vehicle: ["велосипед"],
      time: 16,
      text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Cum quae exercitationem illum cumque facere nostrum! Earum magnam dolorem rem animi, exercitationem alias. Nemo nam laboriosam iusto corporis veniam dolorum ut. Excepturi, nostrum?",
    },
  ];
</script>

<section id="options" class="options">
  {#each categories as category, ind}
    <div class="options__option">
      <p class="options__option__name">{category.name}</p>
      <div class="options__option__info">
        <p class="options__option__info__price">
          цена: <span>{category.price}</span>
        </p>
        <p class="options__option__info__vehicle">
          транспорт: {#each category.vehicle as vehicle, vehicleInd}
            <span
              >{vehicle}{#if vehicleInd < category.vehicle.length - 1}
                ,
              {/if}
            </span>
          {/each}
        </p>
        <p class="options__option__info__time">
          кол-во месяцев учебы: <span>{category.time}</span>
        </p>
      </div>
      <p class="options__option__text">{category.text}</p>
    </div>
  {/each}
</section>

<style scoped lang="scss">
  .options {
    display: flex;
    flex-direction: column;
    gap: 50px;
    padding: 100px 0;

    .options__option {
      display: grid;
      grid-template-columns: 1fr 1.75fr;
      grid-template-rows: repeat(2, auto);
      grid-row-gap: 20px;
      grid-column-gap: 40px;
      align-items: center;

      .options__option__name {
        grid-row-start: 1;
        grid-row-end: 3;
        grid-column-start: 1;
        grid-column-end: 2;
        background-color: var(--white-tertiary-color);
        border-radius: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        width: 120px;
        height: 120px;
        font-size: xx-large;
        color: var(--black-secondary-color);
        font-weight: bold;
        justify-self: end;
      }

      .options__option__info {
        display: flex;
        flex-direction: row;
        gap: 20px;
        align-items: center;
        align-self: flex-end;

        & > p {
          color: var(--black-secondary-color);
          & > span {
            text-decoration: underline;
          }
        }
      }

      .options__option__text {
        align-self: flex-start;
        color: var(--gray-primary-color);
        max-width: 600px;
        transition: all 0.15s ease-in-out;

        &:hover {
          cursor: pointer;
          color: var(--gray-tertiary-color);
        }
      }

      &:nth-child(even) {
        grid-template-columns: 1.75fr 1fr;
        .options__option__name {
          grid-column-start: 2;
          grid-column-end: 3;
          justify-self: start;
        }
        .options__option__info {
          justify-content: flex-end;
        }
        .options__option__text {
          text-align: end;
          margin-left: auto;
        }
      }
    }
  }
</style>

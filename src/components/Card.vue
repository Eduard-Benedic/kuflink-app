<template>
  <div class="card">
    <div class="card__header">
      <KuflinkSvg class="card__logo" />
      <div class="card__info">
        <h2 class="card__title">{{cardText.title}}</h2>

        <h3 v-if="cardText.subtitle" class="card__subtitle">{{cardText.subtitle}}</h3>
      </div>
    </div>
    <img src="../assets/card-icon.png" alt class="card__main-img" />
    <p class="card__p">{{cardText.description}}</p>
    <div class="card__footer">
      <div class="card__actions">
        <div>
          <a class="button button--main" href="/">Login</a>
        </div>
        <div>
          <a class="button button--secondary" href="/">Register</a>
        </div>
      </div>
      <ul class="share">
        <li class="share__item">
          <a href="/" class="share__link share__link--green">
            <font-awesome-icon icon="heart" />
          </a>
        </li>
        <li class="share__item">
          <a href="/" class="share__link share__link--green">
            <font-awesome-icon icon="share-alt" />
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import KuflinkSvg from "../assets/kuflink.svg";
export default {
  name: "Card",
  components: {
    KuflinkSvg
  },
  props: {
    cardText: Object
  }
};
</script>

<style lang="scss">
@import "../styles/components/card.scss";
</style>

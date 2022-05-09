<template>
  <MainLayout class="main text-center">
    <h2 class="main-title">Experienced & Multi-Talented</h2>
    <div class="line text-center w-100">
      <span></span>
    </div>
    <p class="text-center main-description">
      <span>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam tortor
        leo, porttitor vel dictum at, aliquam et augue. Duis vel molestie risus,
        ut lobortis felis.
      </span>
    </p>
    <div class="card-list-container">
      <CardItem
        v-for="card in cardLists"
        :key="card._id"
        :title="card.title"
        :description="card.description"
      />
    </div>
  </MainLayout>
</template>
<script>
import MainLayout from "../layouts/MainLayout";
import CardItem from "./CardItem";
export default {
  components: { MainLayout, CardItem },
  name: "CardList",
  data() {
    return {
      cardLists: [
        {
          _id: 1,
          title: "BlOCK",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut</br> vestibulum eros nisi, eu sagit- tis nisl feugiat quis.",
        },
        {
          _id: 1,
          title: "BlOCK",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. </br>Ut vestibulum eros nisi, eu sagit- tis nisl feugiat quis.",
        },
        {
          _id: 1,
          title: "BlOCK",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. </br>Ut vestibulum eros nisi, eu sagit- tis nisl feugiat quis.",
        },
        {
          _id: 1,
          title: "BlOCK",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit.</br> Ut vestibulum eros nisi, eu sagit- tis nisl feugiat quis.",
        },
        {
          _id: 1,
          title: "BlOCK",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit.</br>Ut vestibulum eros nisi, eu sagit- tis nisl feugiat quis.",
        },
        {
          _id: 1,
          title: "BlOCK",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit.</br>Ut vestibulum eros nisi, eu sagit- tis nisl feugiat quis.",
        },
        {
          _id: 1,
          title: "BlOCK",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit.</br>Ut vestibulum eros nisi, eu sagit- tis nisl feugiat quis.",
        },
        {
          _id: 1,
          title: "BlOCK",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit.</br>Ut vestibulum eros nisi, eu sagit- tis nisl feugiat quis.",
        },
      ],
    };
  },
};
</script>
<style lang="scss">
@import "~@/assets/scss/mixins.scss";

.main {
  padding-top: 85px;

  .main-title {
    line-height: 1.633;
    margin-bottom: 0;

    @include extra-small {
      font-size: 28px;
      line-height: 1.044;
      max-width: 295px;
      margin: 0 auto;
    }
  }

  .main-description {
    line-height: 1.265;
    margin: 30px auto 0 auto;
    font-size: 19px;
    max-width: 698px;

    @include extra-small {
      margin-top: 20px;
      max-width: 300px;
    }
  }

  .line {
    margin: 11px;
    height: 2px;
    display: flex;
    justify-content: center;

    span {
      width: 32px;
      height: inherit;
      background: $white;
    }
  }

  .card-list-container {
    max-width: 1566px;
    margin-top: 47px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }
}
</style>
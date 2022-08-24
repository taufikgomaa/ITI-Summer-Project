<template>
  <p class="h2 text-center">Our Categories</p>
  <div><button class="btn btn-primary" style="float: right;">Add Category</button></div>
  <div class="row">
    <div
      v-for="category of categories"
      :key="category.id"
      class="col-md-6 col-xl-4 col-12 pt-3 justify-content-around d-flex"
    >
      <CategoryBox :category="category"> </CategoryBox>
    </div>
  </div>
</template>

<script>
import CategoryBox from "@/components/Category/CategoryBox.vue";

export default {
  name: "Category",
  components: {
    CategoryBox,
  },
  data() {
    return {
      categories: [],
    };
  },
  methods: {},
  async created() {
    const res = await fetch("http://localhost:3000/category");
    this.categories = await res.json();
  },
};
</script>


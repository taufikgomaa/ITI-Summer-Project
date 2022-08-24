<template>
  <div class="card" style="width: 18rem">
    <img :src="category.imageUrl" class="card-img-top" alt="..." />
    <div class="card-body">
      <h5 class="card-title">{{category.categoryName}}</h5>
      <p class="card-text">
       {{category.description}}
      </p>
      <a href="#" class="btn btn-primary">Go somewhere</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "CategoryBox",
  props: ["category"],
};
</script>
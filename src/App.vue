<template>
  <div class=" card-container flex flex-wrap flexclass">
    <div v-for="(item, index) in items" :key="index" :class="cardClasses(item)" class="p-4 h-100 cardContent">
      <img class="h-30 w-full object-cover md:h-35 sm:h-25" src="https://flowbite.com/docs/images/blog/image-1.jpg"
        alt="Closeup code" />
      {{ item.content }}
    </div>
  </div>
</template>

<script>
import Img1 from './assets/img1.jpg';
import Img2 from './assets/img2.jpg';
import Img3 from './assets/img3.png';
export default {
  data() {
    return {
      items: [
        {
          content: "In Tailwind, use modifiers at the beginning of a utility class name to describe the state you want to target. ",
          imgUrl: Img1,
          color: "bg-yellow-500",
          width: "w-1/6"
        },
        {
          content: "We can use the v-for directive to render a list of items based on an array. The v-for directive requires a special syntax in the form of item in items",
          imgUrl: Img2,
          color: "bg-yellow-400",
          width: "w-1/6"
        },
        {
          content: "Tailwind lets you conditionally apply utility classes in different states using variant modifiers.",
          imgUrl: Img3,
          color: "bg-yellow-300",
          width: "w-1/6"
        },
        {
          content: "The default flex basis scale is a combination of the default spacing scale as well as a set of percentage based values",
          imgUrl: Img2,
          color: "bg-yellow-400",
          width: "w-1/6"
        },
        {
          content: "If you need to use a one-off flex-basis value that doesnot make sense to include in your theme, use square brackets to generate a property on the fly using any arbitrary value.",
          imgUrl: Img1,
          color: "bg-yellow-500",
          width: "w-1/6"
        },
        {
          content: "Notice how the v-for value matches the function signature of the forEach callback. In fact",
          imgUrl: Img2,
          color: "bg-yellow-300",
          width: "w-1/6"
        },
        // Add more objects as needed
      ],
    };
  },
  methods: {
    cardClasses(item) {
      return `w-full sm:w-1/2 md:w-1/3 lg:w-1/4 xl:${item.width} mb-4 ${item.color}`;
    },
  },
};
</script>
<style>
.card-container {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: space-between;
  gap: 15px;
  padding: 15px;
  box-sizing: border-box;
  overflow-y: scroll;
}

.cardContent:hover {
  box-shadow: 5px 5px 10px rgba(32, 32, 32, 0.3);
}
</style>
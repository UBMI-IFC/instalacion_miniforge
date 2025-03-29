
<template>
<footer
   class="absolute bottom-5 left-93%
   right-0 p-2"
   v-if="$nav.currentPage !== 1 && $nav.currentPage !== 2"
   >
<Link to="2">
   <div class="i-carbon:home"/>
</Link>
</footer>
</template>



<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}

h1 > code {
  -webkit-text-fill-color: green;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 15px;

}
</style>

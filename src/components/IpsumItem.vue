<template>
    <li>
        <div class=info>
          <h3>{{ipsum.title}}</h3>
          <h4>{{ipsum.author}}</h4>
          <h5>{{ipsum.category}}</h5>
        </div>
    </li>
</template>

<script>
export default {
    props: {
        ipsum: Object,
        onSelect: Function
    }
};
</script>

<style scoped>
li {
    border: 2px solid teal;
    margin: 5px;
}
img {
    display: none;
}
</style>

<template>
        <ul>
            <IpsumItem
                v-for="ipsum in ipsums"
                v-bind:key="ipsum.title"
                v-bind:ipsum="ipsum"
                @click.native="onSelect(ipsum)"
                />
        </ul>
</template>

<script>
import IpsumItem from './IpsumItem.vue';
export default {
    props: {
        ipsums: Array,
        onSelect: Function
    },
    components: {
        IpsumItem
    }
};

</script>

<style scoped>
ul {
display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow-y: auto;
}
</style>

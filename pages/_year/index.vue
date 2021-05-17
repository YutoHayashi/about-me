<template></template>
<script lang="ts">
import Vue from 'vue';
export default Vue.extend( {
    created(  ) {
        this.$router.push( `${this.$route.params.year}/01` );
    },
} )
</script>

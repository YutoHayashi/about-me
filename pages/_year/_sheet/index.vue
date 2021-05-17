<template></template>
<script lang="ts">
import Vue from 'vue';
export default Vue.extend( {
    layout: ( context ) => {
        return context.from.params.year;
    },
} );
</script>

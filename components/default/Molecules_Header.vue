<template>
<header class="heading l__Pos-relative primary-base-bg" id="header" role="heading" aria-level="1">
    <div class="heading__wrap l__Dsp-flex l__Dsp-flex-wrap">
        <h1 class="heading__wrap-label">/自己紹介</h1>
        <ul class="heading__wrap-links l__Dsp-flex">
            <li class="heading__wrap-links-item" v-for="linkItem in linkItems" :key="linkItem.label">
                <a target="_blank" :href="linkItem.href">
                    <button :class="`heading__wrap-links-item-button ${ linkItem.color }-darken2-border white-base-text-hover ${ linkItem.color }-darken2-text ${linkItem.color}-darken2-bg-hover`" role="button">{{ linkItem.label }}</button>
                </a>
            </li>
        </ul>
    </div>
</header>
</template>
<style lang="scss">
    .heading {
        top: 0;
        width: 100%;
        height: fit-content;
        padding: 10px 0;
        box-shadow: 1px 1px 2px #DDD;
        &__wrap {
            height: 100%;
            padding: 0 10px;
            &-label {
                font-size: 1.00rem;
                font-weight: initial;
                text-align: center;
                margin-right: auto;
                margin-left: auto;
                margin-bottom: 10px;
                @media screen and (min-width: 399px) {
                    margin-left: unset;
                    margin-bottom: unset;
                    text-align: unset;
                }
            }
            &-links {
                list-style-type: none;
                &-item {
                    margin: 0 5px;
                    &-button {
                        padding: 5px 15px;
                        border-radius: 4px;
                        font-weight: 400;
                        font-size: .875rem;
                    }
                }
            }
        }
    }
</style>
<script lang="ts">
import Vue from 'vue';
export default Vue.extend( {
    data: (  ) => {
        return {
            linkItems: [
                { label: 'Github', href: 'https://github.com/YutoHayashi/self-introduction', color: 'github' },
                { label: 'Facebook', href: 'https://www.facebook.com/profile.php?id=100035294776733', color: 'facebook' },
                { label: 'Twitter', href: 'https://twitter.com/CxYzOMOH6tcH1QQ', color: 'twitter' },
            ],
        };
    },
} )
</script>

<template>
    <vuetable ref="vuetable"
    api-url="http://localhost:5000/allDividend?year=2019"
    :fields="['stockId','reportYear','dividendDate','divdendContent']"
    data-path=""
    pagination-path="">
    </vuetable>
</template>

<script>
import Vuetable from 'vuetable-2'

function setState(store) {}

export default {
    name: 'table',
    components:{
        Vuetable
    }
};
</script>

<style lang="stylus" scoped>

.page-index
    display flex
    justify-content center
    align-items center
    flex-direction column

    h2
        font-size 46px
        font-weight 500
        margin-bottom 0

</style>

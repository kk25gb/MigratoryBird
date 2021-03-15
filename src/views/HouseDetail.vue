<template>
    <div class="HouseDetail">
        <HouseDTHeader></HouseDTHeader>
        <Carousel></Carousel>
        <BriefInfoBar></BriefInfoBar>
        <HouseContent></HouseContent>
        
         
    </div>
    
</template>

<script>
import HouseDTHeader from "../components/HouseDTHeader"
import Carousel from '../components/Carousel'
import BriefInfoBar from '../components/BriefInfoBar'
import HouseContent from '../components/HouseContent'

export default {
    name: 'HouseDetail',
    components: {
        HouseDTHeader,
        Carousel,
        BriefInfoBar,
        HouseContent,
          
    },
}
</script>

<style lang="scss" scoped>
$color_darkWhite: #EDEDED;
    *{
        font-family: 微軟正黑體;
        position: relative;
        box-sizing: border-box;
        padding: 0px;
    }
    .HouseDetail{
        background-color: $color_darkWhite;
    }
</style>

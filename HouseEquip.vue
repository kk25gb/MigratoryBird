<template>
    <div class="equip"> 
        <span>住屋設備</span> <br>
        <div class="equip_icon">
            <img src="../assets/media/icon_bed.png" alt="" /><br>
            <span>雙人床</span>
        </div>
        <div class="equip_icon">
            <img src="../assets/media/icon_bath.png" alt="" />
            <span>衛浴</span>
        </div>
        <div class="equip_icon">
            <img src="../assets/media/icon_wifi.png" alt="" />
            <span>網路</span>
        </div>
        <div class="equip_icon">
            <img src="../assets/media/icon_hair-dryer.png" alt="" />
            <span>吹風機</span>
        </div>
        <div class="equip_icon">
            <img src="../assets/media/icon_bed.png" alt="" />
            <span>雙人床</span>
        </div>
        <div class="equip_icon">
            <img src="../assets/media/icon_bath.png" alt="" />
            <span>衛浴</span>
        </div>
        <div class="equip_icon">
            <img src="../assets/media/icon_wifi.png" alt="" />
            <span>網路</span>
        </div>
        <div class="equip_icon">
            <img src="../assets/media/icon_hair-dryer.png" alt="" />
            <span>吹風機</span>
        </div>
    </div>
</template>
<script>
export default {
    name: 'HouseEquip',
    
}
</script>
<style lang="scss" scoped>
.equip{
    padding-top: 40px;
    font-size: 30px;
    font-weight: bolder;
    color: #666B46;
    .equip_icon{
        width: 55px;
        height: 75px;
        margin: 20px 10px 0px;
        color: #7E7E7E;
        font-size: 9px;
        display: inline-flex;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
        img{
            width: 40px;
            height: 40px;
        }
    }
}

</style>
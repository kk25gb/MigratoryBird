<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-1"></div>
            <div class="col-5">
                <span class="bookingTitle">Complete Booking</span>
            </div>
            <div class="col-2"></div>
            <div class="col-4"></div>
        </div>
        
    </div>
</template>
<script>
export default {
    
}
</script>
<style lang="scss" scoped>
@mixin size($w,$h){
    width: $w;
    height: $h;
}
$font_basic_size: 10px;

* {
    font-family: 微軟正黑體;
    position: relative;
    box-sizing: border-box;
}
.row{
    .col-1{
        @include size($w: auto,$h:50px);
        border: 1px solid #000;
    }
    .col-2{
        @include size($w: auto,$h:50px);
        border: 1px solid #000;
    }
    .col-5{
        @include size($w: auto,$h:auto);
        border: 1px solid #000;
        padding-top: 30px;
        .bookingTitle{
            font-size: $font_basic_size*6;
            color: #666B46;
        }
    }
    .col-4{
        @include size($w: auto,$h:50px);
        border: 1px solid #000;
    }
}
</style>
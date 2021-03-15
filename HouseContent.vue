<template>
        <div class="container ">
            <div class="row top">
                <div class="col-1 waste"></div>
                <div class="col-1"></div>
                <div class="col-4 profile">
                    <div class="host">
                        <div class="propic"></div>
                        <div class="host_type">
                            <span>LFR Host</span> <br> 
                            <span class="address">{{address}}-雅房</span>
                        </div>
                    </div>
                    <HouseEquip></HouseEquip>
                </div>
                <div class="col-2"></div>
                <div class="col-4 bargain">
                    <span class="b_title">Bargain</span> <hr>
                    <div class="bargainCube">議價</div>
                </div>
            </div>
            <div class="row middle">
                <div class="col-1 waste"></div>
                <div class="col-1"></div>
                <div class="col-4 aboutHouse">
                    <div class="description">
                        <span d_title>房屋描述</span> <br>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis aliquam incidunt sint eligendi doloribus, officiis magni. Ea assumenda beatae quod, vitae laudantium aliquid pariatur! Dolorem dolores illum maxime facere iusto.</p>
                    </div>
                    <HouseAround></HouseAround>
                </div>
                <div class="col-2"></div>
                <div class="col-4 houseInfo">
                    <span n_title>House Info</span> <hr>
                     <HouseInfoTable></HouseInfoTable>
                </div>
            </div>
            <div class="row map">
                <div class="col-1 waste"></div>
                <div class="col-11 mapPlace">
                    <GoogleMap></GoogleMap>
                </div>
            </div>
            <div class="row LFF">
                <div class="col-1 waste"></div>
                <div class="col-1"></div>
                <div class="col-9 LFFPlace">
                    <span class="LFFTitle">Living Friends Finding</span> <hr>
                    <input type="button" class="btnLFFplus" />
                    <div class="LFFCube">LFF</div>
                </div>
                <div class="col-1"></div>
            </div>
        </div>
    
</template>
 <script>
 import HouseEquip from '../components/HouseEquip'
 import HouseAround from '../components/HouseAround'
 import HouseInfoTable from '../components/HouseInfoTable'
 import GoogleMap from '../components/GoogleMap'
 export default {
    name: "HouseContent",
    data(){
        return{
            address: '中山區惠德街38號',
        }
    },
    components:{
        HouseEquip,
        HouseAround,
        HouseInfoTable,
        GoogleMap,
    }
 }
 </script>

<style lang="scss" scoped>
@mixin size($w,$h){
    width: $w;
    height: $h;
}
$color_darkWhite: #EDEDED;
$color_white: #ffffff;

* {
    font-family: 微軟正黑體;
    position: relative;
    box-sizing: border-box;
}
hr{
    border: 0;
    background-color: #A6B6AE;
    height: 2px;
}
.waste{
        background-color: $color_darkWhite;
    }
.top{
    background-color: $color_white;
    // border: 1px solid #000;
    .profile{
        padding-top: 40px;
        // border: 1px solid #000;
        .host{
            .propic{
                @include size($w:80px,$h:80px);
                border-radius: 50%;
                background-color: #A6B6AE;
                display: inline-block;
            }
            .host_type{
                display: inline-block;
                padding-left: 10px;
                color: #666B46;
                font-weight: bolder;
                font-size: 27px;
                .address{
                    color: #7E7E7E;
                    font-size: 18px;
                }
            }
        }
    }
    
    .bargain{
        padding-top: 80px;
        .b_title{
            color: #666B46;
            font-weight: bolder;
            font-size: 25px;
            display: block;
            text-align: left;
        }
        .bargainCube{
            @include size($w: 90%,$h:220px);
            margin-left: 20px;
            border: 1px solid #707070;
            font-size: 60px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
    }
}
.middle{
    // border: 1px solid #000;
    background-color: $color_white;
    .aboutHouse{
        padding-top: 30px;
        color: #666B46;
        font-weight: bolder;
        font-size: 25px;
        .description{
            p{
                padding-top: 15px;
                padding-left: 20px;
                color: #7e7e7e;
                font-size: 15px;
            }
        }
    }
    .houseInfo{
        padding-top: 50px;
        color: #666B46;
        font-weight: bolder;
        font-size: 25px;
    }
}
.map{
    background-color: $color_white;
    .mapPlace{
        padding-top: 40px;
        display: flex;
        justify-content: center;
    }
}
.LFF{
    background-color: $color_white;
    margin-bottom: 50px;
    .LFFPlace{
        padding-top: 30px;
        .LFFTitle{
            color: #666B46;
            font-weight: bolder;
            font-size: 25px;
        }
        .btnLFFplus{
            @include size($w:40px,$h:40px);
            border-radius: 50%;
            background-image: url(../assets/media/icon_plus.png);
            background-color: $color_darkWhite;
            background-repeat: no-repeat;
            background-position: center;
            background-size: 15px 15px;
            position: absolute;
            left: 100%;
            transform: translateX(-100%) translateY(-100%);
            cursor: pointer;
        }
        .LFFCube{
            @include size($w: 800px,$h: 250px);
            border: 1px solid #000;
            display: flex;
            justify-content: center;
            align-items: center;
            margin-top: 30px;
            font-size: 60px;
        }
    }
}
</style>
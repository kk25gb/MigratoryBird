<template>
    <div class="container-fluid mbselect">
        <span class="mbselecttitle">Mb Select</span>
        <div class="row multiple-items">
            <div class="selectitems">
                <div class="itemsdetail">
                    <div class="housetypeicon">
                        <div class="iconbg">
    
                        </div>
                    </div>
                    <div class="detail">
                        <div class="area">
                            <span class="housearea">Taipei Zoghshan</span>
                            <span class="housetype">Single room</span>
                        </div>
                        <div class="price">
                            <span class="houseprice">NTD:12500</span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="selectitems">
                <div class="itemsdetail">
                    <div class="housetypeicon">
                        <div class="iconbg">
    
                        </div>
                    </div>
                    <div class="detail">
                        <div class="area">
                            <span class="housearea">Taipei Zoghshan</span>
                            <span class="housetype">Single room</span>
                        </div>
                        <div class="price">
                            <span class="houseprice">NTD:12500</span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="selectitems">
                <div class="itemsdetail">
                    <div class="housetypeicon">
                        <div class="iconbg">
    
                        </div>
                    </div>
                    <div class="detail">
                        <div class="area">
                            <span class="housearea">Taipei Zoghshan</span>
                            <span class="housetype">Single room</span>
                        </div>
                        <div class="price">
                            <span class="houseprice">NTD:12500</span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="selectitems">
                <div class="itemsdetail">
                    <div class="housetypeicon">
                        <div class="iconbg">
    
                        </div>
                    </div>
                    <div class="detail">
                        <div class="area">
                            <span class="housearea">Taipei Zoghshan</span>
                            <span class="housetype">Single room</span>
                        </div>
                        <div class="price">
                            <span class="houseprice">NTD:12500</span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="selectitems">
                <div class="itemsdetail">
                    <div class="housetypeicon">
                        <div class="iconbg">
    
                        </div>
                    </div>
                    <div class="detail">
                        <div class="area">
                            <span class="housearea">Taipei Zoghshan</span>
                            <br>
                            <span class="housetype">Single room</span>
                        </div>
                        <div class="price">
                            <span class="houseprice">NTD:12500</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script src="../src//assets//slick-1.8.1//slick//slick.js">

</script>

<script type="text/javascript" src="../src//assets//slick-1.8.1//slick//slick.min.js">

</script>

<script>
export default {
    name: 'MbSelect',
    mounted() {
        $(document).ready(function() {
            $('.multiple-items').slick({
                infinite: true,
                slidesToShow: 3,
                slidesToScroll: 1,
                centerMode: true,
                // autoplay: true,
                autoplaySpeed: 1000
            });
        });
    },

}
</script>

<style lang="scss" scoped>
.mbselect {
    width: 100%;
    height: 600px;
    margin-top: 50px;
    .mbselecttitle {
        font-size: 30px;
        color: #666B46;
        margin-left: 100px;
    }
    .slick-center {
        transition: 0.5s;
        transform: scale(1.2);
    }
    .multiple-items {
        .selectitems {
            background-image: url('../assets/media/patrick_perkins_3wylDrjxH_E_un_bx@2x.png');
            background-position: center;
            background-size: cover;
            border-radius: 5px;
            margin-right: 50px;
            margin-left: 50px;
            margin-top: 100px;
            margin-bottom: 40px;
            height: 300px;
            display: flex;
            justify-content: center;
            align-items: flex-end;
            box-sizing: border-box;
            overflow: hidden;
            transition: 0.4s;
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
            .itemsdetail {
                width: 200px;
                height: 70px;
                background-color: white;
                margin-bottom: 30px;
                border-radius: 17px;
                box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
                display: flex;
                justify-content: center;
                align-items: center;
                box-sizing: border-box; // transform: scale(0);
                transform: translateY(130px);
                transition-duration: 0.5s;
                .housetypeicon {
                    width: 40%;
                    height: 70px;
                    display: flex;
                    margin: auto;
                    justify-content: center;
                    align-items: center; // border: solid 1px;
                    .iconbg {
                        width: 50px;
                        height: 50px;
                        background-color: darkorange; // margin: auto;
                        border-radius: 15px;
                    }
                }
                .detail {
                    width: 60%;
                    height: 80px; // border: solid 1px;
                    box-sizing: border-box;
                    display: flex;
                    flex-direction: column;
                    justify-content: space-evenly;
                    .housearea {
                        font-size: 1px;
                        color: #A6B6AE;
                    }
                    .housetype {
                        font-size: 1px;
                        color: #7AA08F;
                    }
                    .houseprice {
                        font-size: 0.5px;
                        color: #A6B6AE;
                    }
                }
            }
        }
    }
    .selectitems:hover {
        .itemsdetail {
            transform: translateY(10px);
        }
    }
}
</style>
<template>
    <div class="item">
        <div class="piccover">
            <div class="itemcontent">
                <span class="loc">Taipei</span>
                <span class="area">Zongshan</span>
                <span class="price">NTD:12500</span>
            </div>
            <div class="bookbtn">
                <span class="btn">BOOK</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Item'


}
</script>

<style lang="scss" scoped>
.item {
    background-image: url('../assets/media/patrick_perkins_3wylDrjxH_E_un_bx@2x.png');
    width: 350px;
    height: 300px;
    background-size: cover;
    background-repeat: no-repeat;
    background-position-x: -100px;
    border-radius: 20px; // filter: brightness(50%);
    .piccover {
        width: 100%;
        height: 100%;
        border-radius: 20px;
        background-color: black;
        opacity: 0.5;
        .itemcontent {
            height: 70%;
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            // border: solid 1px white;
            padding-top: 30px; // visibility: hidden;
            .loc {
                font-size: 25px;
                opacity: 1;
                transform: translateX(100px);
                transition: 0.3s ease-in-out;
            }
            .price {
                opacity: 1;
                font-size: 35px;
                text-decoration: underline;
                transform: translateX(100px);
                transition: 0.3s ease-in-out;
            }
            .area {
                opacity: 1;
                font-size: 30px;
                transform: translateX(100px);
                transition: 0.3s ease-in-out;
            }
            span {
                color: white;
                font-size: 25px;
                margin-left: 25px;
                margin-bottom: 5px;
                opacity: 1;
                visibility: hidden;
            }
        }
        .bookbtn {
            height: 30%;
            // border: solid 1px white;
            display: flex;
            justify-content: flex-end; // visibility: hidden;
            align-items: center;
            // overflow: hidden;
            // border: solid 1px
            visibility: hidden;
            transition-duration: 0.3s;
            .btn {
                color: white;
                height: 70px;
                width:90px;
                border: solid 1px;
                font-size: 18px;
                display: flex;
                justify-content: center;
                align-items: center;
                border-bottom-right-radius: 20px;
                background-color: white;
                color: black;
                margin-top: 20px;
                

            }
        }
    }
    .piccover:hover {
        .loc,.price,.area {
            transform: translateX(5px);
            visibility: visible;
            color: white;
        }
        .bookbtn{
            visibility: visible;
            
        }
    }
}
</style>
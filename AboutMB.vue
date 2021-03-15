<template>
    <div class="container bottom">
        <div class="row aboutcontent">
            <div class="col-1">
            </div>    
            <div class="col-5 about">
                <span>ABOUT MIGRA</span>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Veniam maxime officia voluptates aliquam iure harum dignissimos aspernatur itaque, totam corrupti neque eos ipsum cumque repellat nobis id nisi voluptas vitae.</p>
                <span class="morebtn">more</span>
            </div>
            <div class="col-5 aboutpic">
                <img src="../assets/media/patrick_perkins_3wylDrjxH_E_un_bx@2x.png" alt="">
            </div>
            <div class="col-1"></div>
    
        </div>
    </div>
</template>

<script>
export default {
    name: 'AboutMb'

}
</script>

<style lang="scss" scoped>
.bottom {
    // border: 1px solid #000;
    .aboutcontent {
        margin-top: 50px;
        .about {
            padding: 0;
            span {
                font-size: 45px;
                color: #666B46;
                margin-left: 15px;
            }
            p {
                padding: 10px;
                padding-right: 20px;
                margin-top: 20px;
            }
            .morebtn {
                font-size: 20px;
                margin-top: 100px;
                float: right;
                margin-right: 60px;
            }
        }
        .aboutpic {
            padding: 0;
            display: flex;
            justify-content: center;
            max-width: 670px;
            height: 400px;
            img {
                width: 100%;
                height: 100%;
            }
        }
    }
}
</style>
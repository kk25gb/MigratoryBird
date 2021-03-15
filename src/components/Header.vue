<template>
    <div class="div header">
        <div class="container">
            <div class="row">
                <div class="col-2">
                    <router-link to="/"><span>Migratory Bird</span></router-link>
                </div>
                <div class="col-5"></div>
                <div class="col-1">
                    <span class="find">Find</span>
                </div>
                <div class="col-1">
                    <span>Need</span>
                </div>
                <div class="col-1">
                    <span>Comunity</span>
                </div>
                <div class="col-1">
                    <span>About</span>
                </div>
                <div class="col-1">
                    <div class="profilepic" @click="show_hiddenNav">
    
                    </div>
                </div>
            </div>
            <!-- hidden navigation bar -->
            <div class="hidden_nav" v-show="isShow_hiddenNav">
                <a href="http://" v-on:click="show_hiddenNav">Profile</a> <br />
                <a href="http://">My Nest</a> <br />
                <a href="http://">Like</a> <br />
                <a href="http://">LFR</a> <br />
                <a href="http://">In Box</a> <br />
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Header',

    data() {
        return{
            isShow_hiddenNav: false,
        }
    },
    methods: {
        show_hiddenNav: function(){
            this.isShow_hiddenNav = !this.isShow_hiddenNav;
        }
    },
}
</script>

<style lang="scss" scoped>
$color_darkGreen: #666b46;
$color_grey: #848484;
$color_darkWhite: #E8E8E8;
*{
    position: relative;
}
.row {
    // z-index: 1;
    div {
        display: flex;
        justify-content: center;
        align-items: center;
        .profilepic {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            background-color: white;
            cursor: pointer;
        }
        .find{
            font-size: 20px;
        }
    }
    span {
        color: white;
    }
}

.header {
    display: flex;
    background-color: #666B46;
    height: 50px;
    justify-content: center;
    align-items: center;
}
.hidden_nav{
    width: 100px;
    height: auto;
    z-index: 1;
    background-color: $color_darkWhite;
    border: 1px solid $color_darkGreen;
    border-radius: 10px;
    text-align: left;
    padding: 10px 10px 10px 17px;
    position: absolute;
    left: 100%;
    transform: translateX(-50%);
    a {
        color: $color_grey;
    }
}
</style>

<template>
    <div class="container-fluid top">
        <div class="row banner">
            <div class="col-4">
                <h1 class="title">MIGRA</h1>
            </div>
            <div class="col-6"></div>
            <div class="col-2">
                <span class="opentoggle" id="opentoggle" @click="open">☰</span>
                <nav class="rightbar" id="rightbar">
                    <span class="toggle" @click="close">☰</span>
                    <div class="navitems">
                        <span>Profile</span>
                        <span>Find</span>
                        <span>Post</span>
                        <span>Comunity</span>
                        <span>Login</span>
                    </div>
                </nav>
            </div>
        </div>
        <div class="row slogan">
            <div class="col-2"></div>
            <div class="col-4">
                <h2>Safe</h2>
                <h2>Family</h2>
                <h2>Hometown</h2>
            </div>
            <div class="col-6"></div>
        </div>
        <div class="row b1">
            <div class="col-3 searchloaction">
                <span>Location</span>
                <input type="text" placeholder="Taipei">
            </div>
            <div class="col-3 searchdate">
                <span>Date</span>
                <span>2019/12/20</span>
            </div>
            <div class="col-3 searchstay">
                <span>Stay</span>
                <span>2 months</span>
            </div>
            <div class="col-3 search">
                <router-link to="/search"><span>BOOK NOW</span></router-link>
                <router-view></router-view>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MainPageTop',
    methods: {
        open() {
            document.getElementById("rightbar").style.display = "block";
            document.getElementById("opentoggle").style.display = "none";
            var elt = document.querySelector(".col-2")
            elt.setAttribute("style", "background-color: white; transition:0.5s;");
        },
        close() {
            document.getElementById("rightbar").style.display = "none";
            document.getElementById("opentoggle").style.display = "block";
            var elt = document.querySelector(".col-2")
            elt.setAttribute("style", "background-color: transparent; transition:0.5s ease-out;");

        }
    },
}
</script>

<style lang="scss" scoped>
.top {
    background-image: url('../assets/media/joyce-romero-EV_bivvSaC8-unsplash.jpg');
    width: 100%;
    height: 100%;
    background-position: center;
    background-position-y: -1000px;
    background-size: cover;
    background-repeat: no-repeat;
    position: relative;
    .banner {
        height: 80vh;
    }
    .title {
        color: white;
        font-size: 100px;
        padding-top: 50px;
        padding-left: 100px;
    } // .col-2 {
    //     height: 100vh;
    // }
    .opentoggle {
        font-size: 50px;
        margin-left: 100px; // display: none;
        color: white;
        transition: 0.5s;
    }
    .opentoggle:hover {
        cursor: pointer;
    }
    .rightbar {
        display: flex;
        flex-direction: column;
        list-style: none;
        font-size: 25px;
        color: #666B46;
        display: none;
        height: 100vh;
        transition: 0.5s;
        .toggle {
            font-size: 50px;
            margin-right: 30px;
            transition-duration: 0.4s; // border: solid 1px;
        }
        .toggle:hover {
            cursor: pointer;
        }
        .navitems {
            display: flex;
            flex-direction: column;
            box-sizing: border-box;
            span {
                margin-left: 40px;
                margin-bottom: 10px;
                transition: 0.5s ease-out;
            }
            span:hover {
                font-size: 28px;
                text-decoration: underline;
            }
        }
    }
}

.slogan {
    position: absolute;
    top: 180px;
    left: 200px;
    .col-4 {
        color: white;
        h2 {
            font-size: 50px;
        }
    }
}

.b1 {
    width: 1000px;
    height: 20vh;
    .col-3 {
        width: 300px;
        height: 100%;
        background-color: white;
        display: flex;
        flex-direction: column;
        margin: auto;
        display: flex;
        justify-content: center;
        align-items: flex-start;
    }
    .searchloaction {
        input {
            border: none;
            color: #666B46;
        }
    }
    .search {
        color: white;
        background-color: #666B46;
        justify-content: center;
        align-items: center;
        border-top-right-radius: 100px;
        transition: 0.3s;
    }
    .search:hover {
        font-size: 28px;
        text-decoration: underline;
    }
}
</style>

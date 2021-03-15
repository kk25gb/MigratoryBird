<template>
    <div class="search">
        <Header></Header>
        <div class="container">
            <div class="row searchbar">
                <div class="loc">
                    <span>Location</span>
                    <br>
                    <input type="text" placeholder="Taipei">
                </div>
                <div class="date">
                    <span>Date</span>
                    <input type='text' class="form-control" id='datetimepicker4' />
                </div>
                <div class="stay">
                    <span>Stay</span>
                </div>
                <div class="searchbtn">
                    <span>SEARCH</span>
                </div>
            </div>
        </div>
        <MbSelect></MbSelect>
        <div class="container-fulid">
            <div class="row searchresult">
                <div class="col-9">
                    <div class="row">
                        <div class="col-6">
                            <router-link to='/HouseDetail'><Item></Item></router-link>
                        </div>
                        <div class="col-6">
                            <Item></Item>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-6">
                            <Item></Item>
                        </div>
                        <div class="col-6">
                            <Item></Item>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-6">
                            <Item></Item>
                        </div>
                        <div class="col-6">
                            <Item></Item>
                        </div>
                    </div>
                </div>
                <div class="col-3"></div>
    
            </div>
        </div>
    </div>
</template>

<script src="https://code.jquery.com/jquery-3.3.1.min.js">

</script>

<script>
import Header from '../components/Header'
import MbSelect from '../components/MbSelect'
import Item from '../components/Item'
export default {
    name: 'search',
    components: {
        Header,
        MbSelect,
        Item
    },
    mounted() {
        $(document).ready(function() {
            $('#datetimepicker4').datepicker({

            });
        });

    },

}
</script>

<style lang="scss" scoped>
.searchbar {
    margin-top: 70px;
    height: 58px;
    border-radius: 10px;
    border: solid 0.5px #A6B6AE;
    span {
        color: #A6B6AE;
    }
    .loc {
        width: 30%;
        border-right: solid 0.5px #7E7E7E;
        padding-top: 5px;
        padding-left: 40px;
        input {
            border: none;
            font-size: 13px;
        }
    }
    .date {
        width: 30%;
        border-right: solid 0.5px #7E7E7E;
        padding-top: 5px;
        padding-left: 30px;
        input {
            width: 80%;
            height: 20px;
        }
    }
    .stay {
        width: 25%;
        padding-top: 5px;
        padding-left: 30px;
    }
    .searchbtn {
        width: 15%;
        background-color: #A6B6AE;
        border-top-right-radius: 10px;
        border-bottom-right-radius: 10px;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        span {
            color: white;
            font-size: 17px;
        }
    }
}

.searchresult {
    border-top: 1px solid;
    .col-3 {
        border-left: 1px solid;
    }
    .col-6 {
        display: flex;
        justify-content: center;
        align-items: center;
        padding-top: 30px;
        padding-bottom: 30px;
    }
}
</style>
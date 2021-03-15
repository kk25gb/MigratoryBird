<template>
    <div class="allTable">
        <table class="table1">
            <tr>
                <td>物件坪數</td>
                <td class="data">{{size}}坪</td>
            </tr>
            <tr>
                <td>住屋人數</td>
                <td class="data">{{capacity}}人</td>
            </tr>
            <tr>
                <td>隔間數量</td>
                <td class="data">{{room_num}}間</td>
            </tr>
            <tr>
                <td>總樓層</td>
                <td class="data">{{floor_num}}樓</td>
            </tr>
            <tr>
                <td>押金</td>
                <td class="data">NTD{{deposite}}</td>
            </tr>
        </table>
        <table class="table2">
            <tr>
                <td>開伙</td>
                <td class="data">{{cook}}</td>
            </tr>
            <tr>
                <td>養寵物</td>
                <td class="data">{{pet}}</td>
            </tr>
            <tr>
                <td>性別限制</td>
                <td class="data">{{gender_restrict}}</td>
            </tr>
            <tr>
                <td>最短租期</td>
                <td class="data">{{min_lease}}年</td>
            </tr>
            <tr>
                <td>產權登記</td>
                <td class="data">{{property_right}}</td>
            </tr>
            <tr>
                <td>法定用途</td>
                <td class="data">{{usage_of_object}}</td>
            </tr>
        </table>
    </div>
</template>
<script>
export default {
    name: 'HouseInfoTable',
    data(){
        return{
            size:'12',
            capacity: '2',
            room_num:'1',
            floor_num:'7',
            deposite:'25000',
            cook:'可',
            pet:'不可',
            gender_restrict:'男',
            min_lease:'一',
            property_right:'已辦',
            usage_of_object:'住家用',
        }
    }
}
</script>
<style lang="scss" scoped>
.allTable{
    display: flex;
    flex-direction: row; 
    .table1, .table2{
        display: inline-block;
        font-size: 15px;
        color: #7e7e7e;
        td{
            padding-top: 5px;
        }
        .data{
            display: flex;
            justify-content: left;
            padding-left: 10px;
        }
    }
    .table2{
        margin-left: 70px;
    }
}   
</style>
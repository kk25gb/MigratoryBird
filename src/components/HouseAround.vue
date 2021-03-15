<template>
    <div class="around">
        <span n_title>生活機能</span> <br>
        <div class="allTag">
            <div class="tag">近便利商店</div>
            <div class="tag">近傳統市場</div>
            <div class="tag">近公園綠地</div>
            <div class="tag">近醫療機構</div>
            <div class="tag">近超市</div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'HouseAround',
}
</script>
<style lang="scss" scoped>
.around{
    .allTag{
        padding-left: 20px;
        .tag{
            width: auto;
            height: 30px;
            display: inline-flex;
            justify-content: center;
            background-color: #A6B6AE;
            padding:5px 10px 5px;
            margin: 3px;
            border-radius: 3px;
            color: #ffffff;
            font-size: 15px;
        }
    }
}
</style>

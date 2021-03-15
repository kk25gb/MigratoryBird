<template>
    <div class="container-fluid footer">
        <div class="row">
            <div class="col-3">
                <div class="logo">
                    <img src="../assets/media/MB_LOGO_white_03@2x.png" alt="" style="border: solid 1px;">
                </div>
            </div>
            <div class="col-5">
                <span class="copyright">
                                &copy; 2020 Migratory Bird.com
                            </span>
            </div>
            <div class="col-1">
            </div>
            <div class="col-2">
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Footer'

}
</script>

<style lang="scss" scope>
.footer {
    .row {
        background-color: #A6B6AE;
        color: white;
        .logo {
            img {
                width: 106px;
                height: 63px;
            }
        }
        .col-5 {
            display: flex;
            justify-content: center;
            align-items: center;
            border: solid 1px;
            .copyright {
                border: solid 1px;
                text-align: center;
            }
        }
    }
}
</style>

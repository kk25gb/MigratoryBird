<template>

  <div id="BriefInfoBar" class="container">
    <div class="row brief_infobar">
      <div class="col-1">1</div>
      <div class="col-1 houseCity">Taipei</div>
      <div class="col-1 houseTitle">雅房</div>
      <div class="col-4"></div>
      <div class="col-3 price">
        <div class="p_table">
          <table>
            <tr>
              <td class="Ta">NTD : 14500/mon</td>
            </tr>
            <tr>
              <td class="Tb">US : 500/mon</td>
            </tr>
          </table>
        </div>
        <div class="icon_Heart">
          <img src="../assets/media/icon_Heart.png" alt="save" />
        </div>
      </div>
      <div class="col-2">
        <input type="button" value="入住" class="button_book" data-toggle="modal" data-target="#myModal"/>
        <input type="button" class="button_magnify" />
      </div>
    </div>
    <!-- datepicker -->
    <div id="myModal" class="modal fade" role="dialog">
    <div class="modal-dialog">
      <!-- Modal content-->
      <div class="modal-content">
        <div class="modal-header">
          <button type="button" class="close" data-dismiss="modal">&times;</button>
          <h4 class="modal-title">Check In</h4>
        </div>
        <div class="modal-body">
          <p>Some text in the modal.</p>
        </div>
        <div class="modal-footer">
          <router-link to='/Booking'>
            <button type="button" class="btn btn-default" data-dismiss="modal">Booking</button>
          </router-link>
        </div>
      </div>
    </div>
  </div>
  </div>

  



</template>

<script>
export default {
  name: "BriefInfoBar",
  components: {

  }
};
</script>

<style lang="scss" scoped>
@mixin size($w, $h) {
  width: $w;
  height: $h;
}
$font_basic_size: 10px;
$color_white: #ffffff;
$color_grey: #848484;
$color_darkWhite: #ededed;
$color_darkGreen: #666b46;

* {
  font-family: 微軟正黑體;
  position: relative;
  box-sizing: border-box;
}
.brief_infobar {
  @include size($w: auto, $h: 90px);
  position: relative;
  // border: 1px solid black;
  margin-top: -90px;
  .houseCity, .houseTitle {
    background-color: $color_darkWhite;
    line-height: 90px;
  }
  .col-4,.price,.col-2 {
    background-color: $color_darkWhite;
    height: 90px;
  }
  .houseCity {
    color: $color_darkGreen;
    font-size: $font_basic_size * 3;
    font-weight: bolder;
    border-radius: 10px 0px 0px 0px;
    padding-left: 10px;
  }
  .houseTitle {
    color: $color_grey;
    font-size: $font_basic_size * 1.5;
    font-weight: bold;
    padding-left: 10px;
  }
  .price {
    // border: 1px solid;
    padding-top: 20px;
    color: $color_grey;
    line-height: 30px;
    .Ta {
      // border: 1px solid
      font-size: $font_basic_size * 2.5;
    }
    .Tb {
      // border: 1px solid
      font-size: $font_basic_size * 1.5;
    }
    .icon_Heart {
      bottom: 40px;
      cursor: pointer;
    }
    .icon_Heart,
    img {
      @include size($w: 35px, $h: auto);
    }
    .p_table,
    .icon_Heart {
      // border: 1px solid
      display: inline-block;
    }
  }
  // .col-2{
  //     border: 1px solid;
  // }
  .button_book {
    @include size($w: 120px, $h: 30px);
    font-weight: bold;
    color: $color_white;
    background-color: $color_darkGreen;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
    border-radius: 10%;
    cursor: pointer;
  }
  .button_magnify {
    @include size($w: 40px, $h: 40px);
    background-image: url("../assets/media/icon_magnify.png");
    background-color: $color_darkWhite;
    background-repeat: no-repeat;
    border-radius: 100%;
    border-style: 3px $color_grey solid;
    background-size: 20px 20px;
    background-position: center;
    position: absolute;
    left: 100%;
    transform: translateX(-50%) translateY(-50%);
    cursor: pointer;
  }
}
.modal{
  height: 500px;
  position: absolute;
  top: -530%;
  // border: 1px solid #000;
  .modal-dialog{
    width: 600px;
    height: 400px;
    // border: 1px solid green;
    .modal-content{
      // border: 1px solid red;
      height: 400px;
      .modal-header{
        border-bottom: none;
        justify-content: flex-start;
      }
      .modal-body{
        border: 1px solid none;
      }
      .modal-footer{
        border-top: none;
      }
    }
  }
}
</style>

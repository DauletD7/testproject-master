<template>
  <div class="carousel relative">
    <div class="left"></div>
    <div class="right"></div>
    <div class="cont">
      <div class="inner_content flex items-center">
        <div class="slide w-full h-full relative">
          <img class="w-full" src="../assets/1.jpg" alt="" />
          <p>dbasjkbdsakjbsadkjkjas</p>
        </div>
        <div class="slide w-full h-full relative">
          <img class="w-full" src="../assets/2.jpg" alt="" />
          <p>dbasjkbdsakjbsadkjkjas</p>
        </div>
        <div class="slide w-full h-full relative">
          <img class="w-full" src="../assets/3.jpg" alt="" />
          <p>dbasjkbdsakjbsadkjkjas</p>
        </div>
      </div>
    </div>
    <p class="arrow_first"><i class="fas fa-angle-left"></i></p>
    <p class="arrow_second"><i class="fas fa-angle-right"></i></p>
    <div class="flex justify-center items-center mt-4">
      <div class="indicator active"></div>
      <div class="indicator mx-3"></div>
      <div class="indicator"></div>
    </div>
  </div>
</template>

<script>
import $ from "jquery";

export default {
  mounted() {
    var a = 0;
    var bool = true;
    $(".arrow_first").on("click", function () {
      bool = false;
      if (bool === false) {
        setInterval(function () {
          bool = true;
          console.log("bool restored");
        }, 50000);
      }
      if (a === 0) {
        $(".inner_content").css({ transform: "translateX(-66.66666%)" });
        $(".indicator:nth-child(1), .indicator:nth-child(2)").removeClass(
          "active"
        );
        $(".indicator:nth-child(3)").addClass("active");
        a = 2;
        console.log("1");
      } else if (a === 1) {
        $(".inner_content").css({ transform: "translateX(0)" });
        $(".indicator:nth-child(2), .indicator:nth-child(3)").removeClass(
          "active"
        );
        $(".indicator:nth-child(1)").addClass("active");
        a = 0;
        console.log("2");
      } else if (a === 2) {
        $(".inner_content").css({ transform: "translateX(-33.333333%)" });
        $(".indicator:nth-child(1), .indicator:nth-child(3)").removeClass(
          "active"
        );
        $(".indicator:nth-child(2)").addClass("active");
        a = 1;
        console.log("3");
      }
    });
    $(".arrow_second").on("click", function () {
      bool = false;
      setInterval(function () {
        if (bool === false) {
          bool = true;
          console.log("bool restored");
        }
      }, 5000);
      if (a === 0) {
        $(".inner_content").css({ transform: "translateX(-33.333333%)" });
        $(".indicator:nth-child(1), .indicator:nth-child(3)").removeClass(
          "active"
        );
        $(".indicator:nth-child(2)").addClass("active");
        a = 1;
      } else if (a === 1) {
        $(".inner_content").css({ transform: "translateX(-66.666666%)" });
        $(".indicator:nth-child(1), .indicator:nth-child(2)").removeClass(
          "active"
        );
        $(".indicator:nth-child(3)").addClass("active");
        a = 2;
      } else if (a === 2) {
        $(".inner_content").css({ transform: "translateX(0)" });
        $(".indicator:nth-child(2), .indicator:nth-child(3)").removeClass(
          "active"
        );
        $(".indicator:nth-child(1)").addClass("active");
        a = 0;
      }
    });

    setInterval(function () {
      if (bool === true) {
        if (a === 0) {
          $(".inner_content").css({ transform: "translateX(-33.333333%)" });
          $(".indicator:nth-child(1), .indicator:nth-child(3)").removeClass(
            "active"
          );
          $(".indicator:nth-child(2)").addClass("active");
          a = 1;
          console.log("1");
        } else if (a === 1) {
          $(".inner_content").css({ transform: "translateX(-66.666666%)" });
          $(".indicator:nth-child(1), .indicator:nth-child(2)").removeClass(
            "active"
          );
          $(".indicator:nth-child(3)").addClass("active");
          a = 2;
          console.log("2");
        } else if (a === 2) {
          $(".inner_content").css({ transform: "translateX(0)" });
          $(".indicator:nth-child(2), .indicator:nth-child(3)").removeClass(
            "active"
          );
          $(".indicator:nth-child(1)").addClass("active");
          a = 0;
          console.log("3");
        }
      }
    }, 5000);
  },
};
</script>
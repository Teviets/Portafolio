<script>
    import { onMount } from 'svelte';

    let wrap;
    let sh;

    function setCoord(coord) {
      let w = document.documentElement.clientWidth;
      let h = document.documentElement.clientHeight;
      return {
        x: w / 4 - (coord.clientX || coord.touches[0].clientX),
        y: h / 4 - (coord.clientY || coord.touches[0].clientY),
        w: w / 4,
        h: h / 4
      };
    }

    onMount(() => {
        //const elBody = document.getElementById('elBody');
        sh = document.querySelector('.shadow');
        wrap = document.querySelector('.wrapper');

        document.body.addEventListener('mousemove', handleMouseMove);
        document.body.addEventListener('touchmove', handleTouchMove);

      return () => {
        document.body.removeEventListener('mousemove', handleMouseMove);
        document.body.removeEventListener('touchmove', handleTouchMove);
      };
    });

    function handleMouseMove(e) {
      let c = setCoord(e);
      sh.style.transform = `translateX(-50%) scaleY(${c.y / 500})`;
      wrap.style.transform = `translate(-50%, -50%) rotateY(${-c.x / 10}deg) rotateX(${c.y / 10}deg)`;
    }

    function handleTouchMove(e) {
      let c = setCoord(e);
      sh.style.transform = `translateX(-50%) scaleY(${(c.w - c.y) / 500})`;
      wrap.style.transform = `translate(-50%, -50%) rotateY(${(c.w - c.x) / -10}deg) rotateX(${(c.h - c.y) / 10}deg)`;
    }
</script>

<div id="elBody">
    <div class="shadow"></div>
<div class="wrapper">
	<div class="artboard">
		<div class="forehead_1"></div>
		<div class="forehead_2"></div>
		<div class="forehead_3"></div>
		<div class="forehead_4"></div>
		<div class="el_1_left"></div>
		<div class="el_1_right"></div>
		<div class="el_3_left"></div>
		<div class="el_3_right"></div>
		<div class="el_2_left"></div>
		<div class="el_2_right"></div>
		<div class="el_4_left"></div>
		<div class="el_4_right"></div>
		<div class="el_5_left"></div>
		<div class="el_5_right"></div>
		<div class="front_n_1"></div>
		<div class="front_n_2"></div>
		<div class="y_left"></div>
		<div class="y_right"></div>
		<div class="y_left_s"></div>
		<div class="y_right_s"></div>
		<div class="und_y_left"></div>
		<div class="und_y_right"></div>
		<div class="nose"></div>
		<div class="un_nose"></div>
		<div class="aster_0_left"></div>
		<div class="aster_0_right"></div>
		<div class="aster_1_left"></div>
		<div class="aster_1_right"></div>
		<div class="aster_2_left"></div>
		<div class="aster_2_right"></div>
		<div class="aster_3_left"></div>
		<div class="aster_3_right"></div>
		<div class="des"></div>
		<div class="u_t_1"></div>
		<div class="u_t_2"></div>
		<div class="u_t_3"></div>
		<div class="u_t_4"></div>
		<div class="u_t_5"></div>
		<div class="u_t_6"></div>
		<div class="md_left"></div>
		<div class="md_right"></div>
		<div class="tg_left"></div>
		<div class="tg_right"></div>
		<div class="d_t_1"></div>
		<div class="d_t_2"></div>
		<div class="d_t_3"></div>
		<div class="d_t_4"></div>
		<div class="d_t_5"></div>
		<div class="d_t_6"></div>
		<div class="sub"></div>
	</div>
</div>
</div>


<style>
html, body {
	 width: 100%;
	 height: 100%;
	 perspective: 700px;
	 margin: 0;
	 padding: 0;
}
body .shadow {
	 content: '';
	 position: absolute;
	 width: 300px;
	 height: 10px;
	 border-radius: 40%;
	 background: #000;
	 bottom: 10vh;
	 left: 50%;
	 transform: translateX(-50%);
	 opacity: 0.2;
	 filter: blur(15px);
}
 .artboard {
	 position: absolute;
	 width: 700px;
	 height: 700px;
	 z-index: -2;
	 left: -205px;
	 top: -90px;
	 background: #b82535;
}
 .wrapper {
	 overflow: hidden;
	 position: absolute;
	 width: 300px;
	 height: 300px;
	 z-index: -3;
	 top: 50%;
	 left: 50%;
	 transform: translate(-50%, -50%);
}
 @keyframes blink {
	 0% {
		 box-shadow: -2px 5px 20px red;
	}
	 50% {
		 box-shadow: -2px 5px 15px red;
	}
	 100% {
		 box-shadow: -2px 5px 20px red;
	}
}
 .forehead_1 {
	 width: 40px;
	 height: 0;
	 position: absolute;
	 border-bottom: 30px solid rgba(255, 255, 255, 0.5);
	 border-left: 15px solid transparent;
	 border-right: 15px solid transparent;
	 border-top: 30px solid transparent;
	 transform-origin: 35px 100%;
	 transform: rotateZ(180deg);
	 left: 320px;
	 top: 100px;
	 z-index: 1;
}
 .forehead_2 {
	 width: 30px;
	 height: 0;
	 position: absolute;
	 border-bottom: 35px solid rgba(255, 255, 255, 0.9);
	 border-left: 10px solid transparent;
	 border-right: 10px solid transparent;
	 border-top: 35px solid transparent;
	 transform-origin: 25px 100%;
	 transform: rotateZ(180deg);
	 left: 330px;
	 top: 88px;
	 z-index: 2;
}
 .forehead_3 {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 30px solid rgba(255, 255, 255, 0.7);
	 border-left: 40px solid transparent;
	 border-right: 40px solid transparent;
	 border-top: 30px solid transparent;
	 transform: rotateZ(180deg);
	 left: 315px;
	 top: 180px;
}
 .el_1_left {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 40px solid rgba(255, 255, 255, 0.6);
	 border-left: 10px solid transparent;
	 border-right: 10px solid transparent;
	 border-top: 40px solid transparent;
	 transform: rotateZ(55deg);
	 left: 402px;
	 top: 115px;
}
 .el_1_right {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 40px solid rgba(255, 255, 255, 0.6);
	 border-left: 10px solid transparent;
	 border-right: 10px solid transparent;
	 border-top: 40px solid transparent;
	 transform: rotateZ(-55deg);
	 left: 288px;
	 top: 115px;
}
 .el_2_left {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 73px solid rgba(255, 255, 255, 0.55);
	 border-left: 10px solid transparent;
	 border-right: 10px solid transparent;
	 border-top: 73px solid transparent;
	 transform: rotateZ(60deg);
	 left: 449px;
	 top: 80px;
	 z-index: 2;
}
 .el_2_right {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 73px solid rgba(255, 255, 255, 0.55);
	 border-left: 10px solid transparent;
	 border-right: 10px solid transparent;
	 border-top: 73px solid transparent;
	 transform: rotateZ(-60deg);
	 left: 244px;
	 top: 80px;
	 z-index: 2;
}
 .el_3_left {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 20px solid rgba(255, 255, 255, 0.9);
	 border-left: 15.75px solid transparent;
	 border-right: 15.75px solid transparent;
	 border-top: 20px solid transparent;
	 transform: rotateZ(132deg);
	 left: 399px;
	 top: 161px;
	 z-index: 0;
}
 .el_3_right {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 20px solid rgba(255, 255, 255, 0.9);
	 border-left: 16.25px solid transparent;
	 border-right: 16.25px solid transparent;
	 border-top: 20px solid transparent;
	 transform: rotateZ(-132deg);
	 left: 279px;
	 top: 161.2px;
	 z-index: 0;
}
 .el_4_left {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 20px solid rgba(255, 255, 255, 0.9);
	 border-left: 0px solid transparent;
	 border-right: 60px solid transparent;
	 border-top: 20px solid transparent;
	 transform-origin: 0px 100%;
	 transform: rotateZ(18deg);
	 left: 312px;
	 top: 161px;
	 z-index: 2;
}
 .el_4_right {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 20px solid rgba(255, 255, 255, 0.9);
	 border-left: 58px solid transparent;
	 border-right: 2px solid transparent;
	 border-top: 20px solid transparent;
	 transform-origin: 58px 100%;
	 transform: rotateZ(-19deg);
	 left: 340px;
	 top: 160px;
	 z-index: 2;
}
 .el_5_left {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 17px solid rgba(255, 255, 255, 0.9);
	 border-left: 74px solid transparent;
	 border-right: 10px solid transparent;
	 border-top: 17px solid transparent;
	 transform-origin: 74px 100%;
	 transform: rotateZ(50deg);
	 left: 227px;
	 top: 175px;
	 z-index: 200;
}
 .el_5_right {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 17px solid rgba(255, 255, 255, 0.9);
	 border-left: 10px solid transparent;
	 border-right: 74px solid transparent;
	 border-top: 17px solid transparent;
	 transform-origin: 10px 100%;
	 transform: rotateZ(-50.7deg);
	 left: 401px;
	 top: 176px;
	 z-index: 200;
}
 .front_n_1 {
	 width: 20px;
	 height: 0;
	 position: absolute;
	 border-bottom: 30px solid rgba(255, 255, 255, 0.9);
	 border-left: 5px solid transparent;
	 border-right: 5px solid transparent;
	 border-top: 30px solid transparent;
	 transform-origin: 15px 100%;
	 transform: rotateZ(180deg);
	 left: 340px;
	 top: 134px;
	 z-index: 2;
}
 .front_n_2 {
	 width: 19px;
	 height: 0;
	 position: absolute;
	 border-bottom: 30px solid rgba(255, 255, 255, 0.7);
	 border-left: 3px solid transparent;
	 border-right: 3px solid transparent;
	 border-top: 30px solid transparent;
	 transform-origin: 12.5px 100%;
	 transform: rotateZ(0deg);
	 left: 342.5px;
	 top: 170px;
	 z-index: 2;
}
 .y_left {
	 width: 16px;
	 height: 16px;
	 position: absolute;
	 border-radius: 50%;
	 background-color: red;
	 transform: rotateZ(0deg);
	 left: 320px;
	 top: 195px;
	 z-index: 1;
	 box-shadow: 2px 5px 20px red;
	 animation: blink 1s ease infinite;
}
 .y_right {
	 width: 16px;
	 height: 16px;
	 position: absolute;
	 border-radius: 50%;
	 background-color: red;
	 transform: rotateZ(0deg);
	 left: 373px;
	 top: 195px;
	 box-shadow: -2px 5px 20px red;
	 z-index: 1;
	 animation: blink 1s ease infinite;
}
 .und_y_left {
	 width: 41px;
	 height: 20px;
	 position: absolute;
	 background-color: rgba(255, 255, 255, 0.8);
	 transform-origin: 20.5px 10px;
	 transform: rotateZ(19deg);
	 left: 309px;
	 top: 205px;
	 z-index: 0;
}
 .und_y_right {
	 width: 41px;
	 height: 20px;
	 position: absolute;
	 background-color: rgba(255, 255, 255, 0.8);
	 transform-origin: 20.5px 10px;
	 transform: rotateZ(-19deg);
	 left: 362px;
	 top: 205px;
	 z-index: 0;
}
 .nose {
	 width: 19px;
	 height: 0;
	 position: absolute;
	 border-bottom: 5px solid rgba(255, 255, 255, 0.5);
	 border-left: 3px solid transparent;
	 border-right: 3px solid transparent;
	 border-top: 5px solid transparent;
	 transform-origin: 12.5px 100%;
	 transform: rotateZ(180deg);
	 left: 343px;
	 top: 220px;
	 z-index: 2;
}
 .un_nose {
	 width: 30px;
	 height: 12px;
	 position: absolute;
	 background-color: rgba(255, 255, 255, 0.9);
	 transform-origin: 15px 6px;
	 transform: rotateZ(0deg);
	 left: 340.6px;
	 top: 230px;
	 z-index: 1;
}
 .aster_0_left {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 10px solid rgba(255, 255, 255, 0.9);
	 border-left: 15px solid transparent;
	 border-right: 15px solid transparent;
	 border-top: 10px solid transparent;
	 transform-origin: 15px 100%;
	 transform: rotateZ(10deg);
	 left: 275px;
	 top: 195px;
}
 .aster_0_right {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 10px solid rgba(255, 255, 255, 0.9);
	 border-left: 15px solid transparent;
	 border-right: 15px solid transparent;
	 border-top: 10px solid transparent;
	 transform-origin: 15px 100%;
	 transform: rotateZ(-10deg);
	 left: 408px;
	 top: 195px;
}
 .aster_1_left {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 15px solid rgba(255, 255, 255, 0.9);
	 border-left: 50px solid transparent;
	 border-right: 40px solid transparent;
	 border-top: 15px solid transparent;
	 transform-origin: 50px 100%;
	 transform: rotateZ(0deg);
	 left: 260px;
	 top: 203px;
}
 .aster_1_right {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 14px solid rgba(255, 255, 255, 0.9);
	 border-left: 40px solid transparent;
	 border-right: 50px solid transparent;
	 border-top: 14px solid transparent;
	 transform-origin: 40px 100%;
	 transform: rotateZ(0deg);
	 left: 362px;
	 top: 204px;
}
 .aster_2_left {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 18px solid rgba(255, 255, 255, 0.9);
	 border-left: 55px solid transparent;
	 border-right: 55px solid transparent;
	 border-top: 18px solid transparent;
	 transform-origin: 55px 100%;
	 transform: rotateZ(-35deg);
	 left: 260px;
	 top: 223px;
}
 .aster_2_right {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 18px solid rgba(255, 255, 255, 0.9);
	 border-left: 55px solid transparent;
	 border-right: 55px solid transparent;
	 border-top: 18px solid transparent;
	 transform-origin: 55px 100%;
	 transform: rotateZ(35deg);
	 left: 343px;
	 top: 223px;
}
 .aster_3_left {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 13px solid rgba(255, 255, 255, 0.9);
	 border-left: 30px solid transparent;
	 border-right: 30px solid transparent;
	 border-top: 13px solid transparent;
	 transform-origin: 30px 100%;
	 transform: rotateZ(-60deg);
	 left: 294px;
	 top: 259px;
}
 .aster_3_right {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 13px solid rgba(255, 255, 255, 0.9);
	 border-left: 30px solid transparent;
	 border-right: 30px solid transparent;
	 border-top: 13px solid transparent;
	 transform-origin: 30px 100%;
	 transform: rotateZ(60deg);
	 left: 358px;
	 top: 259px;
}
 .des {
	 width: 34px;
	 height: 34px;
	 position: absolute;
	 border-radius: 50%;
	 background-color: rgba(255, 255, 255, 0.45);
	 transform: rotateZ(0deg);
	 left: 338.5px;
	 top: 215px;
	 z-index: -1;
}
 .u_t_1 {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 18px solid rgba(255, 255, 255, 0.9);
	 border-left: 2.5px solid transparent;
	 border-right: 2.5px solid transparent;
	 border-top: 18px solid transparent;
	 transform: rotateZ(185deg);
	 left: 341px;
	 top: 243.5px;
	 z-index: -2;
}
 .u_t_2 {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 10px solid rgba(255, 255, 255, 0.9);
	 border-left: 2.5px solid transparent;
	 border-right: 2.5px solid transparent;
	 border-top: 10px solid transparent;
	 transform: rotateZ(180deg);
	 left: 346px;
	 top: 245.5px;
	 z-index: -2;
}
 .u_t_3 {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 10px solid rgba(255, 255, 255, 0.9);
	 border-left: 2.5px solid transparent;
	 border-right: 2.5px solid transparent;
	 border-top: 10px solid transparent;
	 transform: rotateZ(180deg);
	 left: 351px;
	 top: 245.5px;
	 z-index: -2;
}
 .u_t_4 {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 10px solid rgba(255, 255, 255, 0.9);
	 border-left: 2.5px solid transparent;
	 border-right: 2.5px solid transparent;
	 border-top: 10px solid transparent;
	 transform: rotateZ(180deg);
	 left: 356px;
	 top: 245.5px;
	 z-index: -2;
}
 .u_t_5 {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 10px solid rgba(255, 255, 255, 0.9);
	 border-left: 2.5px solid transparent;
	 border-right: 2.5px solid transparent;
	 border-top: 10px solid transparent;
	 transform: rotateZ(180deg);
	 left: 361px;
	 top: 245.5px;
	 z-index: -2;
}
 .u_t_6 {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 18px solid rgba(255, 255, 255, 0.9);
	 border-left: 2.5px solid transparent;
	 border-right: 2.5px solid transparent;
	 border-top: 18px solid transparent;
	 transform: rotateZ(175deg);
	 left: 366px;
	 top: 243.5px;
	 z-index: -2;
}
 .md_left {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 3.3333333333px solid rgba(255, 255, 255, 0.9);
	 border-left: 10px solid transparent;
	 border-right: 40px solid transparent;
	 border-top: 3.3333333333px solid transparent;
	 transform-origin: 10px 100%;
	 transform: rotateZ(85deg);
	 left: 334px;
	 top: 265px;
}
 .md_right {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 3.3333333333px solid rgba(255, 255, 255, 0.9);
	 border-left: 40px solid transparent;
	 border-right: 10px solid transparent;
	 border-top: 3.3333333333px solid transparent;
	 transform-origin: 40px 100%;
	 transform: rotateZ(-85deg);
	 left: 328px;
	 top: 265px;
}
 .tg_left {
	 width: 12px;
	 height: 0;
	 position: absolute;
	 border-bottom: 5px solid rgba(255, 255, 255, 0.9);
	 border-left: 3.5px solid transparent;
	 border-right: 3.5px solid transparent;
	 border-top: 5px solid transparent;
	 transform-origin: 9.5px 100%;
	 transform: rotateZ(90deg);
	 left: 340px;
	 top: 271px;
}
 .tg_right {
	 width: 12px;
	 height: 0;
	 position: absolute;
	 border-bottom: 5px solid rgba(255, 255, 255, 0.9);
	 border-left: 3.5px solid transparent;
	 border-right: 3.5px solid transparent;
	 border-top: 5px solid transparent;
	 transform-origin: 9.5px 100%;
	 transform: rotateZ(-90deg);
	 left: 353px;
	 top: 271px;
}
 .d_t_1 {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 17px solid rgba(255, 255, 255, 0.9);
	 border-left: 1.6666666667px solid transparent;
	 border-right: 1.6666666667px solid transparent;
	 border-top: 17px solid transparent;
	 transform: rotateZ(-2deg);
	 left: 347px;
	 top: 275px;
	 z-index: -2;
}
 .d_t_2 {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 12px solid rgba(255, 255, 255, 0.9);
	 border-left: 1.25px solid transparent;
	 border-right: 1.25px solid transparent;
	 border-top: 12px solid transparent;
	 transform: rotateZ(-2deg);
	 left: 349px;
	 top: 285px;
	 z-index: -2;
}
 .d_t_3 {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 12px solid rgba(255, 255, 255, 0.9);
	 border-left: 1.25px solid transparent;
	 border-right: 1.25px solid transparent;
	 border-top: 12px solid transparent;
	 transform: rotateZ(-2deg);
	 left: 352px;
	 top: 285px;
	 z-index: -2;
}
 .d_t_4 {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 12px solid rgba(255, 255, 255, 0.9);
	 border-left: 1.25px solid transparent;
	 border-right: 1.25px solid transparent;
	 border-top: 12px solid transparent;
	 transform: rotateZ(-2deg);
	 left: 355px;
	 top: 285px;
	 z-index: -2;
}
 .d_t_5 {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 12px solid rgba(255, 255, 255, 0.9);
	 border-left: 1.25px solid transparent;
	 border-right: 1.25px solid transparent;
	 border-top: 12px solid transparent;
	 transform: rotateZ(-2deg);
	 left: 358px;
	 top: 285px;
	 z-index: -2;
}
 .d_t_6 {
	 width: 0;
	 height: 0;
	 position: absolute;
	 border-bottom: 17px solid rgba(255, 255, 255, 0.9);
	 border-left: 1.6666666667px solid transparent;
	 border-right: 1.6666666667px solid transparent;
	 border-top: 17px solid transparent;
	 transform: rotateZ(-2deg);
	 left: 360px;
	 top: 275px;
	 z-index: -2;
}
 .sub {
	 width: 15px;
	 height: 0;
	 position: absolute;
	 border-bottom: 5px solid rgba(255, 255, 255, 0.9);
	 border-left: 1px solid transparent;
	 border-right: 1px solid transparent;
	 border-top: 5px solid transparent;
	 transform-origin: 8.5px 100%;
	 transform: rotateZ(180deg);
	 left: 347.7px;
	 top: 300px;
}
 
</style>
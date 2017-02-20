    $(document).ready(
        function () {
            var startX1,//触摸时的坐标
            startY1,
            x1 = 0, x2 = 0, //滑动的距离
            y1,
            aboveX1 = 0; //设一个全局变量记录上一次内部块滑动的位置
            var inner1 = document.getElementById("top-gund");
            function touchSatrt(e) {//触摸
                // e.preventDefault();
                var touch = e.touches[0];
                startX1 = touch.pageX; //刚触摸时的坐标
            }

            function touchMove(e) {//滑动
                //  e.preventDefault();
                var touch = e.touches[0];
                x1 = touch.pageX - startX1;//滑动的距离
                //inner.style.webkitTransform = 'translate(' + 0+ 'px, ' + y + 'px)'; //也可以用css3的方式
                inner1.style.left = aboveX1 + x1 + "px"; //这一句中的
            }
            function touchEnd(e) {//手指离开屏幕
                if (x1 == x2) {

                }
                else {
                    x2 = x1;
                    var w1 = 0;
                    $("#top-gund li").each(function () {
                        w1 += $(this).width() + 10;
                    });
                    var a1 = w1 + 43;
                    $("#top-gund").width(a1);
                    var b = $(window).width();
                    var c = a1 - b;
                    //e.preventDefault();
                    aboveX1 = parseInt(inner1.style.left);//touch结束后记录内部滑块滑动的位置 在全局变量中体现 一定要用parseInt()将其转化为整数字;
                    if (aboveX1 > 0) {
                        inner1.style.left = 0 + "px"; //这一句中的
                        aboveX1 = 0;
                    }
                    else if (aboveX1 * -1 < c) {
                        inner1.style.left = aboveX1 + "px";
                        // alert(parseInt((aboveX1 / 40)));.
                    }
                    else {
                        inner1.style.left = -1 * c + "px"; //这一句中的
                        aboveX1 = -1 * c;
                    }
                }
            }//
            document.getElementById("top-gun").addEventListener('touchstart', touchSatrt, false);
            document.getElementById("top-gun").addEventListener('touchmove', touchMove, false);
            document.getElementById("top-gun").addEventListener('touchend', touchEnd, false);
        });


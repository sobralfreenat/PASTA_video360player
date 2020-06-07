# PASTA_video360player

<!DOCTYPE html>
<html lang="en">

<head>
    <title>HOAST360</title>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, user-scalable=no, minimum-scale=1.0, maximum-scale=1.0">
</head>

<body>

    <div id="overlay">
        <div id="topfill"></div>
        <div id="headers">
            <h1><span id="h1">HOAST360</span></h1>
            <p id="hoast-text">Higher Order Ambisonics Spatial Transform <br> 360 Degree Video Player</p>
        </div>
    </div>

    <button onclick="init()">load</button>
    <button onclick="stop()">stop</button>
    
    <video-js id='hoast360-player' class='video-js vjs-fluid vjs-big-play-centered ' controls preload='auto' crossorigin="anonymous" data-setup='{}'>
        <p class='vjs-no-js'>
          To view this video please enable JavaScript, and consider upgrading to a web browser that
          <a href='https://videojs.com/html5-video-support/' target='_blank'>supports HTML5 video</a>
        </p>
    </video-js>

    <script src="./dist/hoast360.bundle.js"></script>
    <script>
        var hoast360 = new HOAST360();
        var ambisonicsOrder = 1;

        function init() {
            hoast360.initialize("./media/GABARITO 360 white2_360.mp4", "./irs/hoast_o1_01-04ch", 1);
        }

        function stop() {
            hoast360.reset();
        }
    </script>
</body>
</html>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css" />
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.2.1/css/all.min.css"
    integrity="sha512-MV7K8+y+gLIBoVD59lQIYicR65iaqukzvf/nwasF0nqhPay5w/9lJmVM2hMDcnK1OnMGCdVK+iQrJ7lzPJQd1w=="
    crossorigin="anonymous" referrerpolicy="no-referrer" />
<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.3/jquery.min.js"></script>
<style>
    .container {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 97vh;
    }

    .container svg {
        width: 22%;
        height: 22%;
    }
    canvas {
        position: absolute;
        width: 100%;
        height: 100%;
        background-color: #FFEBEB;
      }
   
</style>

<!-- aa2 -->
<style>
    * {
        margin: 0;
        padding: 0;
    }

    .body-letter {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        background-color: #fae1dd;
    }

    .letter {
        position: relative;
        z-index: 1;
    }
    .valentines {
        position: relative;
        top: 50px;
        cursor: pointer;
        animation: up 3s linear infinite;
    }

    @keyframes up {

        0%,
        100% {
            transform: translateY(0);
        }

        50% {
            transform: translateY(-30px);
        }
    }


    .envelope {
        position: relative;
        width: 300px;
        height: 200px;
        background-color: #f08080;
    }

    .envelope:before {
        background-color: #f08080;
        content: "";
        position: absolute;
        width: 212px;
        height: 212px;
        transform: rotate(45deg);
        top: -105px;
        left: 44px;
        border-radius: 30px 0 0 0;
    }

    .card {
        position: absolute;
        background-color: #eae2b7;
        width: 270px;
        height: 170px;
        top: 5px;
        left: 15px;
        box-shadow: -5px -5px 100px rgba(0, 0, 0, 0.4);
    }

    .card:before {
        content: "";
        position: absolute;
        border: 3px solid #003049;
        border-style: dotted;
        width: 240px;
        heighT: 140px;
        left: 12px;
        top: 12px;
    }

    .text {
        position: absolute;
        font-family: 'Brush Script MT', cursive;
        font-size: 28px;
        text-align: center;
        line-height: 25px;
        top: 19px;
        left: 85px;
        color: #003049;
    }

    .heart {
        background-color: #d62828;
        display: inline-block;
        height: 30px;
        margin: 0 10px;
        position: relative;
        top: 110px;
        left: 105px;
        transform: rotate(-45deg);
        width: 30px;
    }

    .heart:before,
    .heart:after {
        content: "";
        background-color: #d62828;
        border-radius: 50%;
        height: 30px;
        position: absolute;
        width: 30px;
    }

    .heart:before {
        top: -15px;
        left: 0;
    }

    .heart:after {
        left: 15px;
        top: 0;
    }

    .hearts {
        position: absolute;
        top: 0
    }

    .one,
    .two,
    .three,
    .four,
    .five {
        background-color: red;
        display: inline-block;
        height: 10px;
        margin: 0 10px;
        position: relative;
        transform: rotate(-45deg);
        width: 10px;
        top: 50px;
    }

    .one:before,
    .one:after,
    .two:before,
    .two:after,
    .three:before,
    .three:after,
    .four:before,
    .four:after,
    .five:before,
    .five:after {
        content: "";
        background-color: red;
        border-radius: 50%;
        height: 10px;
        position: absolute;
        width: 10px;
    }

    .one:before,
    .two:before,
    .three:before,
    .four:before,
    .five:before {
        top: -5px;
        left: 0;
    }

    .one:after,
    .two:after,
    .three:after,
    .four:after,
    .five:after {
        left: 5px;
        top: 0;
    }

    .one {
        left: 10px;
        animation: heart 1s ease-out infinite;
    }

    .two {
        left: 30px;
        animation: heart 2s ease-out infinite;
    }

    .three {
        left: 50px;
        animation: heart 1.5s ease-out infinite;
    }

    .four {
        left: 70px;
        animation: heart 2.3s ease-out infinite;
    }

    .five {
        left: 90px;
        animation: heart 1.7s ease-out infinite;
    }

    @keyframes heart {
        0% {
            transform: translateY(0) rotate(-45deg) scale(0.3);
            opacity: 1;
        }

        100% {
            transform: translateY(-150px) rotate(-45deg) scale(1.3);
            opacity: 0.5;
        }
    }

    .front {
        position: absolute;
        border-right: 180px solid #f4978e;
        border-top: 95px solid transparent;
        border-bottom: 100px solid transparent;
        left: 120px;
        top: 5px;
        width: 0;
        height: 0;
        z-index: 10;
    }

    .front:before {
        position: absolute;
        content: "";
        border-left: 300px solid #f8ad9d;
        border-top: 195px solid transparent;
        left: -120px;
        top: -95px;
        width: 0;
        height: 0;
    }

    .shadow {
        position: absolute;
        width: 330px;
        height: 25px;
        border-radius: 50%;
        background-color: rgba(0, 0, 0, 0.3);
        top: 265px;
        left: -15px;
        animation: scale 3s linear infinite;
        z-index: -1;
    }

    @keyframes scale {

        0%,
        100% {
            transform: scaleX(1);
        }

        50% {
            transform: scaleX(0.85);
        }
    }

    .hover-animation {
        animation: hover 1.75s ease-in-out infinite;
    }

    #castle {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
        background-color: #fae1dd;
    }

    .dustDef {
        position: absolute;
        background-color: white;
        border-radius: 100%;
        box-shadow: 0 0 3px 1px white;
        opacity: 0;
    }

    @keyframes hover {
        0% {
            margin-top: 60px;
        }

        50% {
            margin-top: 50px;
        }

        100% {
            margin-top: 60px;
        }
    }

    @keyframes glow {
        0% {
            box-shadow: 0 0 25px 0 #e8b2ca;
        }

        50% {
            box-shadow: 0 0 45px 0 #e8b2ca;
        }

        100% {
            box-shadow: 0 0 25px 0 #e8b2ca;
        }
    }

    @keyframes fall {
        5% {
            top: 209px;
            left: 105px;
            transform: rotate(55deg) scale(0.9, 0.95) skew(-18deg);
            opacity: 0.9;
        }

        30% {
            left: 90px;
        }

        55% {
            left: 130px;
        }

        60%,
        100% {
            top: 380px;
            transform: rotate(30deg) scale(0.9, 0.95) skew(-32deg);
            opacity: 0;
        }
    }

    @keyframes floatAnimate {
        0% {
            background-size: 105% 120%;
            background-position: 0 0;
            opacity: 0.7;
        }

        50% {
            background-size: 100% 100%;
            background-position: 0 0;
            opacity: 0.5;
        }

        100% {
            background-size: 105% 120%;
            background-position: 0 0;
            opacity: 0.7;
        }
    }
</style>
<style>
    svg {

        width: 80%;
        display: block;
        position: absolute;
        margin: auto;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        z-index: 1;
    }

    text {
        fill: #e6668a;
        font-family: consolas;
        font-size: 9px;
    }

    p {
        position: absolute;
        z-index: 2
    }

    label {
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        opacity: .8
    }

    /* style letter */
    /* .box-content.active {
        opacity: 1;
        visibility: visible;
        transform: scale(1);
    }

    .box-content {
        position: fixed;
        width: 100%;
        height: 100%;
        z-index: 100000000000;
        top: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        background: rgba(0, 0, 0, 0.7);
        transform: scale(0.01);
        visibility: hidden;
        transition: 0.5s;
    }

    .fa-xmark {
        position: absolute;
        right: 5%;
        top: 5%;
        font-size: 40px;
        color: #fff;
        cursor: pointer;
    }

    .fa-xmark:hover {
        filter: drop-shadow(0 0 10px #fff);
    }

    .image-decorate {
        display: flex;
        width: 700px;
        z-index: 10;
        height: 100%;
    }

    .content1 {
        position: absolute;
        width: 700px;
        height: 500px;
        background-image: radial-gradient(circle farthest-corner at center, #f9edf3 10%, #ffd3ee 100%);
        border-radius: 10px 70px 10px 70px;
        box-shadow: 5px 5px 10px rgb(0, 0, 0);
        cursor: pointer;
    }

    .textLetter {
        width: 100%;
        flex-direction: column;
        justify-content: center;
        display: flex;
        align-items: center;
        user-select: none;
    }

    .textLetter h2 {
        font-size: 30px;
        font-family: 'Dancing Script', cursive;
    }

    .textLetter .contentLetter {
        font-size: 19px;
        text-align: center;
        padding: 0px 30px;
        margin-top: 10px;
        font-family: 'Dancing Script', cursive;
        position: initial;

    } */



    .letters{
position: absolute;
width: 65px;
transition: 10s ease-in-out;
cursor: pointer;
z-index: 1000;

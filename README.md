<!DOCTYPE html>
<html>
    <head>
        <title>Dichotomy</title>
        <link rel="stylesheet" href="./ha.css">
        <style>
            @import url('https://fonts.googleapis.com/css?family=Poppins:300,400,500,600,700,800,900&display=swap');
*
{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
    scroll-behavior: smooth;
}
body
{
    min-height: 100vh;
    background: linear-gradient(#000000,#900404);
    overflow-x: hidden;
}
header
{
    position: absolute;
    top: 0;
    Left: 0;
    width: 100%;
    padding: 30px 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    z-index: 10000;
}
header .logo
{
    color: #fff;
    text-decoration: none;
    font-weight: 700;
    font-size: 2em;
    letter-spacing: 2px;
}
header ul
{
    display: flex;
    justify-content: center;
    align-items: center;
}
header ul li
{
    list-style: none;
    margin-left: 20px;
}
header ul li a
{
    text-decoration: none;
    padding: 6px 15px;
    color: #fff;
    border-radius: 20px;
}
header ul li a:hover ,
.active
{
    background: #fff;
    color:#000000
}
section
{
    position: relative;
    width: 100%;
    height: 100vh;
    padding: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
    overflow: hidden;
}
section::before
{
    content: '';
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 100px;
    background: linear-gradient(to top, #900404, transparent);
    z-index: 1000;
}
section img
{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    pointer-events: none;
}
section img#chaand
{
    mix-blend-mode: screen;
}
section img#pahaad_aage
{
    z-index: 10;
}
#text
{
    position: absolute;
    right: -350px;
    color: #fff;
    white-space: nowrap;
    font-size: 7.5vw;
    z-index: 9;
}
#btn
{
    text-decoration : none;
    display: inline-block;
    padding: 8px 30px;
    border-radius: 40px;
    background: #fff;
    color: #000000;
    font-size: 1.5em;
    z-index: 9;
    transform: translateY(100px);
}
.sec
{
   position: relative;
   padding: 100px;
   background:  #900404;
}
.sec h2
{
    font-size: 3.5em;
    margin-bottom: 10px;
    color: #fff;
}
.sec p{
    font-size: 1em;
    color: #fff;
}
        </style>
    </head>
    <body>
        <header>
            <a href="#" class="logo">Dichotomy</a>
            <ul>
                <li><a href="#" class="active">Home</a></li>
                <li><a href="#">Team</a></li>
                <li><a href="#">Portfolio</a></li>
                <li><a href="#">Reach-out</a></li>
            </ul>
        </header>
        <section>
            <img src="./stars.png" id="sitaare">
            <img src="./moon.png" id="chaand">
            <img src="./mountains_behind.png" id="pahaadpeeche">
            <h2 id="text">Mahesh Dalle</h2>
            <a href="#sec" id="btn">Dikha Dunga</a>
            <img src="./mountains_front.png" id="pahaad_aage">
        </section>
        <div class="sec" id="sec">
            <h2>Welcome to Dichotomy.co!</h2>
            <p>A web development and tech company that embraces the power of opposites to create cutting-edge digital solutions. We thrive on the balance between creativity and functionality, innovation and practicality, design and coding. With our talented team of web developers, designers, and tech enthusiasts, we specialize in crafting immersive web experiences that captivate audiences and drive results.
                <br><br> Whether you need a stunning website, robust e-commerce platform, or custom web application, Dichotomy delivers tailored solutions that seamlessly blend aesthetics with functionality. 
                <br><br>Step into the world of Dichotomy, where we turn the complexities of web development into beautifully simple solutions for your digital success.
            </p>
        </div>
        <script>
            let stars = document.getElementById('sitaare');
            let moon = document.getElementById('chaand')
            let mountains_behind = document.getElementById('pahaadpeeche')
            let text = document.getElementById('text')
            let mountains_front=document.getElementById('pahaad_aage')
            let btn = document.getElementById('btn')
            let header = document.querySelector('header')
            window.addEventListener('scroll', function(){
                let value = window.scrollY;
                stars.style.left = value * 0.25 + 'px';
                moon.style.top = value * 1.05 + 'px';
                mountains_behind.style.top = value * 0.5 + 'px';
                mountains_front.style.top = value * 0 + 'px';
                text.style.marginRight = value * 4 +'px';
                text.style.marginTop = value * 1.5 +'px';
                btn.style.marginTop = value * 1.5 +'px';
                header.style.top = value * 0.5 + 'px';
            })
        </script>
    </body>
</html>

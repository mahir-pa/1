<!DOCTYPE html>
<html>
    <head>
        <title>Dichotomy</title>
        <link rel="stylesheet" href="./ha.css">
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

<!DOCTYPE html>
<html lang="en">

<head>
    <!-- ==========================
         META TAGS
    =========================== -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <!-- ==========================
         WEBSITE TITLE
    =========================== -->
    <title>S-Y | Sherdil Yousafzai</title>

    <!-- ==========================
         GOOGLE FONTS
    =========================== -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

    <link
        href="https://fonts.googleapis.com/css2?family=Cinzel:wght@500;600;700&family=Outfit:wght@300;400;500;600;700;800&family=Poppins:wght@300;400;500;600&display=swap"
        rel="stylesheet">

    <!-- ==========================
         FONT AWESOME
    =========================== -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css">

    <!-- ==========================
         CSS FILE
    =========================== -->
    <style>
      /*=========================================
  GOOGLE FONTS
=========================================*/
@import url('https://fonts.googleapis.com/css2?family=Cinzel:wght@500;600;700&family=Outfit:wght@300;400;500;600;700;800&family=Poppins:wght@300;400;500;600&display=swap');

/*=========================================
  CSS VARIABLES
=========================================*/
:root{

    --bg:#050816;
    --bg-secondary:#0B1023;

    --card:rgba(255,255,255,.08);
    --card-border:rgba(255,255,255,.12);

    --text:#ffffff;
    --text-light:#d7def5;

    --primary:#2563EB;
    --secondary:#38BDF8;
    --accent:#7C3AED;

    --gradient:
    linear-gradient(
        135deg,
        var(--primary),
        var(--secondary),
        var(--accent)
    );

    --shadow:
    0 10px 40px rgba(37,99,235,.20);

    --blur:blur(18px);

    --radius:20px;

    --transition:.35s ease;

}

/*=========================================
  LIGHT MODE
=========================================*/
body.light-mode{

    --bg:#f7f9ff;
    --bg-secondary:#eef3ff;

    --card:rgba(255,255,255,.85);
    --card-border:rgba(0,0,0,.08);

    --text:#111827;
    --text-light:#4b5563;

}

/*=========================================
  RESET
=========================================*/
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{

    font-family:'Outfit',sans-serif;
    background:var(--bg);
    color:var(--text);

    overflow-x:hidden;

    transition:
    background .4s ease,
    color .4s ease;

}

/*=========================================
  CUSTOM SCROLLBAR
=========================================*/
::-webkit-scrollbar{
    width:10px;
}

::-webkit-scrollbar-track{
    background:var(--bg);
}

::-webkit-scrollbar-thumb{

    background:var(--gradient);

    border-radius:50px;
}

/*=========================================
  SELECTION
=========================================*/
::selection{

    background:var(--secondary);
    color:#fff;

}

/*=========================================
  GLOBAL ELEMENTS
=========================================*/
img{

    width:100%;
    display:block;

}

a{

    text-decoration:none;
    color:inherit;

}

ul{

    list-style:none;

}

button,
input,
textarea{

    font-family:inherit;
    border:none;
    outline:none;

}

button{

    cursor:pointer;

}

/*=========================================
  CONTAINER
=========================================*/
.container{

    width:min(90%,1300px);
    margin:auto;

}

/*=========================================
  SECTION SPACING
=========================================*/
section{

    padding:120px 0;

}

/*=========================================
  SECTION TITLE
=========================================*/
.section-title{

    text-align:center;
    margin-bottom:60px;

}

.section-title span{

    color:var(--secondary);

    letter-spacing:2px;

    text-transform:uppercase;

    font-size:14px;

    font-weight:700;

}

.section-title h2{

    font-family:'Cinzel',serif;

    font-size:48px;

    margin-top:12px;
    margin-bottom:18px;

}

.section-title p{

    max-width:700px;

    margin:auto;

    color:var(--text-light);

    line-height:1.8;

}

/*=========================================
  BUTTONS
=========================================*/
.btn{

    display:inline-flex;

    align-items:center;
    justify-content:center;

    gap:10px;

    padding:16px 32px;

    border-radius:50px;

    font-weight:600;

    transition:var(--transition);

}

.btn-primary{

    background:var(--gradient);

    color:#fff;

    box-shadow:var(--shadow);

}

.btn-primary:hover{

    transform:translateY(-5px);

}

.btn-secondary{

    border:1px solid var(--card-border);

    background:var(--card);

    backdrop-filter:var(--blur);

    color:var(--text);

}

.btn-secondary:hover{

    transform:translateY(-5px);

}

/*=========================================
  GLASS EFFECT
=========================================*/
.glass{

    background:var(--card);

    border:1px solid var(--card-border);

    backdrop-filter:var(--blur);

    border-radius:var(--radius);

}

/*=========================================
  ANIMATIONS
=========================================*/
@keyframes float{

    0%,100%{
        transform:translateY(0);
    }

    50%{
        transform:translateY(-20px);
    }

}

@keyframes fadeUp{

    from{

        opacity:0;

        transform:
        translateY(40px);

    }

    to{

        opacity:1;

        transform:
        translateY(0);

    }

}

/*=========================================
  BACKGROUND GLOW
=========================================*/
body::before{

    content:"";

    position:fixed;

    top:-200px;
    left:-200px;

    width:500px;
    height:500px;

    background:rgba(124,58,237,.15);

    filter:blur(120px);

    border-radius:50%;

    z-index:-2;

}

body::after{

    content:"";

    position:fixed;

    right:-200px;
    bottom:-200px;

    width:500px;
    height:500px;

    background:rgba(56,189,248,.15);

    filter:blur(120px);

    border-radius:50%;

    z-index:-2;

}
/*=========================================
  LOADER
=========================================*/

.loader{

    position:fixed;

    inset:0;

    width:100%;
    height:100vh;

    background:var(--bg);

    display:flex;
    justify-content:center;
    align-items:center;

    z-index:99999;

    transition:.8s ease;

}

.loader.hide{

    opacity:0;
    visibility:hidden;

}

.loader-content{

    text-align:center;

    animation:fadeUp 1s ease;

}

.loader-logo{

    width:140px;
    height:140px;

    margin:auto;

    border-radius:50%;

    display:flex;
    align-items:center;
    justify-content:center;

    font-size:48px;
    font-weight:800;

    color:#fff;

    background:var(--gradient);

    box-shadow:
    0 0 30px rgba(37,99,235,.45),
    0 0 60px rgba(124,58,237,.35);

    animation:
    float 3s ease-in-out infinite;

}

.loader-logo span{

    font-family:'Cinzel',serif;

}

.loader h1{

    font-family:'Cinzel',serif;

    margin-top:30px;

    font-size:38px;

    letter-spacing:2px;

}

.loader p{

    margin-top:10px;

    color:var(--text-light);

    letter-spacing:3px;

    text-transform:uppercase;

}

.loading-bar{

    width:300px;

    height:8px;

    margin:35px auto 0;

    background:rgba(255,255,255,.08);

    border-radius:50px;

    overflow:hidden;

}

.loading-bar span{

    display:block;

    width:0;

    height:100%;

    border-radius:50px;

    background:var(--gradient);

    animation:loading 4s linear forwards;

}

@keyframes loading{

    from{

        width:0;

    }

    to{

        width:100%;

    }

}

/*=========================================
  WELCOME SCREEN
=========================================*/

.welcome-screen{

    position:fixed;

    inset:0;

    width:100%;
    height:100vh;

    display:flex;

    justify-content:center;
    align-items:center;

    padding:20px;

    background:
    rgba(5,8,22,.95);

    backdrop-filter:blur(15px);

    z-index:9990;

    opacity:0;

    visibility:hidden;

    transition:.6s;

}

.welcome-screen.show{

    opacity:1;

    visibility:visible;

}

.welcome-card{

    width:100%;
    max-width:520px;

    padding:45px;

    border-radius:25px;

    background:var(--card);

    border:1px solid var(--card-border);

    backdrop-filter:var(--blur);

    text-align:center;

    box-shadow:var(--shadow);

    animation:fadeUp .8s ease;

}

.welcome-card h4{

    color:var(--secondary);

    letter-spacing:4px;

    margin-bottom:12px;

}

.welcome-card h1{

    font-family:'Cinzel',serif;

    font-size:42px;

    margin-bottom:15px;

}

.welcome-card p{

    color:var(--text-light);

    line-height:1.8;

    margin-bottom:35px;

}

.input-box{

    position:relative;

    margin-bottom:22px;

}

.input-box i{

    position:absolute;

    left:20px;
    top:50%;

    transform:translateY(-50%);

    color:var(--secondary);

    font-size:18px;

}

.input-box input{

    width:100%;

    height:60px;

    padding-left:55px;

    border-radius:50px;

    background:rgba(255,255,255,.06);

    border:1px solid var(--card-border);

    color:var(--text);

    transition:var(--transition);

}

.input-box input:focus{

    border-color:var(--secondary);

    box-shadow:
    0 0 20px rgba(56,189,248,.25);

}

.input-box input::placeholder{

    color:var(--text-light);

}

#welcomeForm button{

    width:100%;

    height:60px;

    border-radius:50px;

    background:var(--gradient);

    color:#fff;

    font-size:17px;
    font-weight:600;

    transition:var(--transition);

    box-shadow:var(--shadow);

}

#welcomeForm button:hover{

    transform:translateY(-4px);

}
/*=========================================
  HEADER
=========================================*/

header{

    position:fixed;

    top:0;
    left:0;

    width:100%;

    z-index:1000;

    padding:18px 0;

    transition:all .35s ease;

}

header.sticky{

    padding:12px 0;

    background:rgba(5,8,22,.78);

    backdrop-filter:blur(20px);

    border-bottom:1px solid rgba(255,255,255,.08);

    box-shadow:0 10px 35px rgba(0,0,0,.25);

}

/*=========================================
  NAVBAR
=========================================*/

.navbar{

    display:flex;

    align-items:center;

    justify-content:space-between;

    gap:40px;

}

/*=========================================
  LOGO
=========================================*/

.logo{

    display:flex;

    align-items:center;

    gap:15px;

}

.logo span{

    width:55px;
    height:55px;

    display:flex;

    align-items:center;
    justify-content:center;

    border-radius:50%;

    background:var(--gradient);

    color:#fff;

    font-size:20px;

    font-weight:700;

    font-family:'Cinzel',serif;

    box-shadow:var(--shadow);

}

.logo h2{

    font-family:'Cinzel',serif;

    font-size:22px;

    color:var(--text);

    transition:var(--transition);

}

/*=========================================
  NAVIGATION LINKS
=========================================*/

.nav-links{

    display:flex;

    align-items:center;

    gap:35px;

}

.nav-links li{

    position:relative;

}

.nav-links a{

    position:relative;

    color:var(--text);

    font-size:16px;

    font-weight:500;

    transition:var(--transition);

}

.nav-links a::after{

    content:"";

    position:absolute;

    left:0;
    bottom:-8px;

    width:0;

    height:2px;

    background:var(--gradient);

    transition:.35s;

    border-radius:20px;

}

.nav-links a:hover{

    color:var(--secondary);

}

.nav-links a:hover::after{

    width:100%;

}

/*=========================================
  RIGHT SIDE
=========================================*/

.nav-right{

    display:flex;

    align-items:center;

    gap:15px;

}

/*=========================================
  ICON BUTTONS
=========================================*/

.icon-btn{

    width:48px;

    height:48px;

    display:flex;

    align-items:center;

    justify-content:center;

    border-radius:50%;

    background:var(--card);

    border:1px solid var(--card-border);

    backdrop-filter:var(--blur);

    color:var(--text);

    transition:var(--transition);

}

.icon-btn:hover{

    background:var(--gradient);

    color:#fff;

    transform:translateY(-4px);

    box-shadow:var(--shadow);

}

/*=========================================
  MENU BUTTON
=========================================*/

.menu-btn{

    display:none;

    width:48px;

    height:48px;

    border-radius:50%;

    background:var(--gradient);

    color:#fff;

    transition:var(--transition);

}

.menu-btn:hover{

    transform:rotate(90deg);

}

/*=========================================
  ACTIVE NAV LINK
=========================================*/

.nav-links a.active{

    color:var(--secondary);

}

.nav-links a.active::after{

    width:100%;

}

/*=========================================
  LIGHT MODE HEADER
=========================================*/

body.light-mode header.sticky{

    background:rgba(255,255,255,.85);

    border-bottom:1px solid rgba(0,0,0,.08);

}

body.light-mode .icon-btn{

    background:rgba(255,255,255,.9);

}

/*=========================================
  NAVBAR ANIMATION
=========================================*/

.navbar{

    animation:fadeUp .8s ease;

}
/*=========================================
  MOBILE NAVIGATION
=========================================*/

.menu-btn{

    display:none;

    align-items:center;
    justify-content:center;

    font-size:20px;

    cursor:pointer;

}

@media (max-width:991px){

    .menu-btn{

        display:flex;

    }

    .nav-links{

        position:fixed;

        top:90px;
        right:-100%;

        width:320px;
        max-width:90%;

        height:calc(100vh - 90px);

        background:rgba(5,8,22,.96);

        backdrop-filter:blur(20px);

        border-left:1px solid rgba(255,255,255,.08);

        display:flex;

        flex-direction:column;

        justify-content:flex-start;

        align-items:flex-start;

        padding:40px 30px;

        gap:25px;

        transition:.4s ease;

        overflow-y:auto;

        z-index:999;

    }

    .nav-links.active{

        right:0;

    }

    .nav-links li{

        width:100%;

    }

    .nav-links a{

        display:block;

        width:100%;

        font-size:18px;

        padding:12px 0;

    }

    .nav-right{

        gap:12px;

    }

}

/*=========================================
  MOBILE MENU OVERLAY
=========================================*/

.nav-overlay{

    position:fixed;

    inset:0;

    background:rgba(0,0,0,.45);

    opacity:0;

    visibility:hidden;

    transition:.35s ease;

    z-index:998;

}

.nav-overlay.show{

    opacity:1;

    visibility:visible;

}

/*=========================================
  MENU BUTTON ANIMATION
=========================================*/

.menu-btn i{

    transition:.35s ease;

}

.menu-btn.active i{

    transform:rotate(90deg);

}

/*=========================================
  RESPONSIVE HEADER
=========================================*/

@media (max-width:991px){

    .logo h2{

        font-size:18px;

    }

}

@media (max-width:768px){

    header{

        padding:15px 0;

    }

    .logo span{

        width:48px;
        height:48px;

        font-size:18px;

    }

    .logo h2{

        font-size:16px;

    }

    .icon-btn,
    .menu-btn{

        width:44px;
        height:44px;

    }

}

@media (max-width:480px){

    .nav-links{

        width:100%;

        max-width:100%;

        top:80px;

        height:calc(100vh - 80px);

        padding:30px 20px;

    }

    .logo{

        gap:10px;

    }

    .logo h2{

        font-size:15px;

    }

}

/*=========================================
  WEBSITE CONTAINER
=========================================*/

.website{

    display:none;

    min-height:100vh;

}

.website.show{

    display:block;

    animation:fadeUp .6s ease;

}
/*=========================================
  HERO SECTION
=========================================*/

.hero{

    position:relative;

    min-height:100vh;

    display:flex;

    align-items:center;

    overflow:hidden;

    padding-top:140px;

}

.hero .container{

    display:grid;

    grid-template-columns:repeat(2,1fr);

    align-items:center;

    gap:80px;

}

/*=========================================
  HERO BACKGROUND
=========================================*/

.hero-bg{

    position:absolute;

    inset:0;

    z-index:-2;

    background:
    radial-gradient(circle at top left,
    rgba(37,99,235,.18),
    transparent 35%),

    radial-gradient(circle at bottom right,
    rgba(124,58,237,.18),
    transparent 35%),

    radial-gradient(circle at center,
    rgba(56,189,248,.12),
    transparent 45%);

}

.hero::before{

    content:"";

    position:absolute;

    width:550px;

    height:550px;

    border-radius:50%;

    background:rgba(124,58,237,.12);

    filter:blur(120px);

    top:-180px;

    right:-120px;

    z-index:-1;

}

.hero::after{

    content:"";

    position:absolute;

    width:450px;

    height:450px;

    border-radius:50%;

    background:rgba(37,99,235,.15);

    filter:blur(100px);

    bottom:-150px;

    left:-100px;

    z-index:-1;

}

/*=========================================
  HERO CONTENT
=========================================*/

.hero-content{

    animation:fadeUp 1s ease;

}

.hero-badge{

    display:inline-flex;

    align-items:center;

    gap:10px;

    padding:10px 22px;

    border-radius:50px;

    background:var(--card);

    border:1px solid var(--card-border);

    backdrop-filter:var(--blur);

    color:var(--secondary);

    font-size:14px;

    font-weight:600;

    margin-bottom:25px;

}

.hero-content h1{

    font-family:'Cinzel',serif;

    font-size:68px;

    line-height:1.15;

    margin-bottom:25px;

}

.hero-content h1 span{

    background:var(--gradient);

    -webkit-background-clip:text;

    -webkit-text-fill-color:transparent;

    background-clip:text;

}

.hero-content p{

    font-size:18px;

    color:var(--text-light);

    line-height:1.9;

    max-width:650px;

    margin-bottom:40px;

}

/*=========================================
  HERO BUTTONS
=========================================*/

.hero-buttons{

    display:flex;

    gap:20px;

    flex-wrap:wrap;

}
/*=========================================
  HERO STATS
=========================================*/

.hero-stats{

    display:flex;

    align-items:center;

    gap:25px;

    margin-top:50px;

    flex-wrap:wrap;

}

.stat{

    min-width:140px;

    padding:20px;

    border-radius:18px;

    background:var(--card);

    border:1px solid var(--card-border);

    backdrop-filter:var(--blur);

    transition:var(--transition);

}

.stat:hover{

    transform:translateY(-8px);

    box-shadow:var(--shadow);

}

.stat h2{

    font-size:34px;

    color:var(--secondary);

    margin-bottom:8px;

}

.stat p{

    margin:0;

    font-size:15px;

    color:var(--text-light);

    line-height:1.6;

}

/*=========================================
  HERO IMAGE AREA
=========================================*/

.hero-image{

    position:relative;

    display:flex;

    justify-content:center;

    align-items:center;

    min-height:650px;

}

/*=========================================
  GLASS CIRCLES
=========================================*/

.glass-circle{

    position:absolute;

    border-radius:50%;

    backdrop-filter:blur(20px);

    border:1px solid rgba(255,255,255,.08);

    animation:float 6s ease-in-out infinite;

}

.circle1{

    width:120px;
    height:120px;

    top:40px;
    left:40px;

    background:rgba(56,189,248,.18);

}

.circle2{

    width:90px;
    height:90px;

    right:30px;
    top:150px;

    background:rgba(124,58,237,.18);

    animation-delay:1s;

}

.circle3{

    width:160px;
    height:160px;

    bottom:40px;
    left:70px;

    background:rgba(37,99,235,.15);

    animation-delay:2s;

}

/*=========================================
  MAIN GLASS CARD
=========================================*/

.main-glass-card{

    width:360px;

    padding:45px 35px;

    text-align:center;

    border-radius:30px;

    background:var(--card);

    border:1px solid var(--card-border);

    backdrop-filter:var(--blur);

    box-shadow:var(--shadow);

    animation:float 5s ease-in-out infinite;

}

.logo-circle{

    width:120px;
    height:120px;

    margin:0 auto 25px;

    display:flex;

    justify-content:center;
    align-items:center;

    border-radius:50%;

    background:var(--gradient);

    color:#fff;

    font-family:'Cinzel',serif;

    font-size:34px;

    font-weight:700;

    box-shadow:
    0 0 30px rgba(37,99,235,.30);

}

.main-glass-card h2{

    font-family:'Cinzel',serif;

    font-size:30px;

    margin-bottom:12px;

}

.main-glass-card p{

    color:var(--text-light);

    line-height:1.8;

}

/*=========================================
  FLOATING CARDS
=========================================*/

.floating-card{

    position:absolute;

    padding:18px 25px;

    border-radius:18px;

    background:var(--card);

    border:1px solid var(--card-border);

    backdrop-filter:var(--blur);

    display:flex;

    align-items:center;

    gap:15px;

    box-shadow:var(--shadow);

    animation:float 4s ease-in-out infinite;

}

.floating-card i{

    font-size:28px;

    color:var(--secondary);

}

.floating-card h3{

    font-size:17px;

    font-weight:600;

}

.watch-card{

    top:70px;

    right:-10px;

}

.perfume-card{

    left:-20px;

    bottom:90px;

    animation-delay:1.5s;

}
/*=========================================
  SCROLL DOWN BUTTON
=========================================*/

.scroll-down{

    position:absolute;

    left:50%;
    bottom:35px;

    transform:translateX(-50%);

    width:42px;
    height:70px;

    border:2px solid var(--secondary);

    border-radius:50px;

    display:flex;

    justify-content:flex-start;
    align-items:center;

    padding-top:10px;

    transition:var(--transition);

}

.scroll-down span{

    width:10px;
    height:10px;

    border-radius:50%;

    background:var(--secondary);

    animation:scrollDown 1.8s infinite;

}

.scroll-down:hover{

    transform:translateX(-50%) scale(1.08);

}

@keyframes scrollDown{

    0%{

        transform:translateY(0);

        opacity:1;

    }

    100%{

        transform:translateY(34px);

        opacity:0;

    }

}

/*=========================================
  FEATURED CATEGORIES
=========================================*/

.categories{

    position:relative;

    padding:120px 0;

}

.category-grid{

    display:grid;

    grid-template-columns:repeat(4,1fr);

    gap:30px;

}

.category-card{

    text-align:center;

    padding:40px 25px;

    background:var(--card);

    border:1px solid var(--card-border);

    backdrop-filter:var(--blur);

    border-radius:24px;

    transition:var(--transition);

    overflow:hidden;

    position:relative;

}

.category-card::before{

    content:"";

    position:absolute;

    top:0;
    left:-100%;

    width:100%;
    height:100%;

    background:linear-gradient(
        90deg,
        transparent,
        rgba(255,255,255,.08),
        transparent
    );

    transition:.8s;

}

.category-card:hover::before{

    left:100%;

}

.category-card:hover{

    transform:translateY(-12px);

    box-shadow:var(--shadow);

    border-color:rgba(56,189,248,.35);

}

.category-card i{

    width:90px;
    height:90px;

    margin:0 auto 25px;

    display:flex;

    justify-content:center;
    align-items:center;

    border-radius:50%;

    background:var(--gradient);

    color:#fff;

    font-size:34px;

}

.category-card h3{

    font-size:24px;

    margin-bottom:15px;

    font-family:'Cinzel', serif;

}

.category-card p{

    color:var(--text-light);

    line-height:1.8;

}

/*=========================================
  HERO RESPONSIVE
=========================================*/

@media (max-width:1100px){

    .hero .container{

        grid-template-columns:1fr;

        text-align:center;

        gap:70px;

    }

    .hero-content p{

        margin-left:auto;
        margin-right:auto;

    }

    .hero-buttons,
    .hero-stats{

        justify-content:center;

    }

}

@media (max-width:768px){

    .hero{

        padding-top:120px;

    }

    .hero-content h1{

        font-size:48px;

    }

    .main-glass-card{

        width:100%;

        max-width:340px;

    }

    .watch-card{

        right:0;

    }

    .perfume-card{

        left:0;

    }

    .category-grid{

        grid-template-columns:repeat(2,1fr);

    }

}

@media (max-width:576px){

    .hero-content h1{

        font-size:38px;

    }

    .hero-content p{

        font-size:16px;

    }

    .hero-buttons{

        flex-direction:column;

    }

    .btn{

        width:100%;

    }

    .hero-stats{

        flex-direction:column;

    }

    .stat{

        width:100%;

    }

    .category-grid{

        grid-template-columns:1fr;

    }

    .floating-card{

        position:static;

        margin:15px auto;

    }

    .hero-image{

        min-height:auto;

    }

}
/*=========================================
  PRODUCTS SECTION
=========================================*/

.products{
    position:relative;
    overflow:hidden;
}

.product-grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:30px;
}

.product-card{

    background:var(--card);
    border:1px solid var(--card-border);
    backdrop-filter:var(--blur);

    border-radius:25px;

    overflow:hidden;

    transition:var(--transition);

    box-shadow:0 10px 30px rgba(0,0,0,.15);

}

.product-card:hover{

    transform:translateY(-12px);

    box-shadow:var(--shadow);

    border-color:rgba(56,189,248,.35);

}

.product-image{

    position:relative;

    overflow:hidden;

    height:340px;

}

.product-image img{

    width:100%;
    height:100%;

    object-fit:cover;

    transition:.6s ease;

}

.product-card:hover .product-image img{

    transform:scale(1.08);

}

.product-image::after{

    content:"";

    position:absolute;
    inset:0;

    background:linear-gradient(
        to top,
        rgba(0,0,0,.45),
        transparent
    );

    opacity:0;

    transition:.4s;

}

.product-card:hover .product-image::after{

    opacity:1;

}

/*=========================================
  WISHLIST BUTTON
=========================================*/

.wishlist{

    position:absolute;

    top:18px;
    right:18px;

    width:48px;
    height:48px;

    border-radius:50%;

    background:rgba(255,255,255,.12);

    backdrop-filter:blur(12px);

    color:#fff;

    display:flex;
    justify-content:center;
    align-items:center;

    transition:var(--transition);

    z-index:2;

}

.wishlist:hover{

    background:var(--gradient);

    transform:scale(1.08);

}

.wishlist i{

    font-size:18px;

}

/*=========================================
  PRODUCT INFO
=========================================*/

.product-info{

    padding:28px;

}

.product-info h3{

    font-size:24px;

    font-family:'Cinzel',serif;

    margin-bottom:18px;

}

.rating{

    display:flex;

    gap:6px;

    color:#FFD54A;

    margin-bottom:18px;

}

.product-info h4{

    font-size:28px;

    color:var(--secondary);

    margin-bottom:22px;

    font-weight:700;

}

.product-btn{

    display:inline-flex;

    justify-content:center;
    align-items:center;

    width:100%;

    padding:15px;

    border-radius:50px;

    background:var(--gradient);

    color:#fff;

    font-weight:600;

    transition:var(--transition);

    box-shadow:var(--shadow);

}

.product-btn:hover{

    transform:translateY(-4px);

}
/*=========================================
  PRODUCT HOVER CONTENT
=========================================*/

.product-card:hover .product-info h3{
    color:var(--secondary);
}

.product-card:hover .product-btn{
    letter-spacing:.5px;
}

.product-card:hover .wishlist i{
    transform:scale(1.15);
}

/*=========================================
  PRODUCT BADGE
=========================================*/

.product-badge{

    position:absolute;

    left:18px;
    top:18px;

    padding:8px 16px;

    border-radius:30px;

    background:var(--gradient);

    color:#fff;

    font-size:13px;
    font-weight:600;

    letter-spacing:.5px;

    box-shadow:var(--shadow);

    z-index:2;

}

/*=========================================
  PRODUCT CARD SHINE EFFECT
=========================================*/

.product-card::before{

    content:"";

    position:absolute;

    top:0;
    left:-120%;

    width:70%;
    height:100%;

    background:
    linear-gradient(
        120deg,
        transparent,
        rgba(255,255,255,.15),
        transparent
    );

    transform:skewX(-25deg);

    transition:.9s;

}

.product-card:hover::before{

    left:150%;

}

/*=========================================
  PRODUCT CARD BORDER GLOW
=========================================*/

.product-card{

    position:relative;

}

.product-card::after{

    content:"";

    position:absolute;

    inset:0;

    border-radius:25px;

    padding:1px;

    background:linear-gradient(
        135deg,
        rgba(37,99,235,.35),
        rgba(56,189,248,.35),
        rgba(124,58,237,.35)
    );

    -webkit-mask:
    linear-gradient(#fff 0 0) content-box,
    linear-gradient(#fff 0 0);

    -webkit-mask-composite:xor;

    mask-composite:exclude;

    opacity:0;

    transition:.35s;

}

.product-card:hover::after{

    opacity:1;

}

/*=========================================
  PRODUCT IMAGE OVERLAY BUTTON
=========================================*/

.product-image .quick-view{

    position:absolute;

    left:50%;
    bottom:-60px;

    transform:translateX(-50%);

    padding:12px 28px;

    border-radius:40px;

    background:var(--gradient);

    color:#fff;

    font-weight:600;

    transition:.4s;

    z-index:3;

}

.product-card:hover .quick-view{

    bottom:20px;

}

/*=========================================
  PRODUCT SECTION ANIMATION
=========================================*/

.product-card{

    animation:fadeUp .8s ease;

}

.product-card:nth-child(2){
    animation-delay:.1s;
}

.product-card:nth-child(3){
    animation-delay:.2s;
}

.product-card:nth-child(4){
    animation-delay:.3s;
}

.product-card:nth-child(5){
    animation-delay:.4s;
}

.product-card:nth-child(6){
    animation-delay:.5s;
}
/*=========================================
  PRODUCTS RESPONSIVE
=========================================*/

@media (max-width:1200px){

    .product-grid{

        grid-template-columns:repeat(3,1fr);

        gap:25px;

    }

    .product-image{

        height:300px;

    }

}

@media (max-width:992px){

    .product-grid{

        grid-template-columns:repeat(2,1fr);

        gap:25px;

    }

    .product-info{

        padding:24px;

    }

    .product-info h3{

        font-size:22px;

    }

    .product-info h4{

        font-size:24px;

    }

    .product-image{

        height:280px;

    }

}

@media (max-width:768px){

    .products{

        padding:100px 0;

    }

    .product-grid{

        gap:22px;

    }

    .product-image{

        height:260px;

    }

    .wishlist{

        width:42px;
        height:42px;

        top:15px;
        right:15px;

    }

    .wishlist i{

        font-size:16px;

    }

    .product-info{

        padding:20px;

    }

    .product-info h3{

        font-size:20px;

    }

    .product-info h4{

        font-size:22px;

    }

    .product-btn{

        padding:14px;

        font-size:15px;

    }

}

@media (max-width:576px){

    .product-grid{

        grid-template-columns:1fr;

    }

    .product-card{

        max-width:420px;

        margin:auto;

    }

    .product-image{

        height:320px;

    }

    .product-info{

        text-align:center;

    }

    .rating{

        justify-content:center;

    }

}

@media (max-width:400px){

    .product-image{

        height:280px;

    }

    .product-info{

        padding:18px;

    }

    .product-info h3{

        font-size:18px;

    }

    .product-info h4{

        font-size:20px;

    }

    .product-btn{

        font-size:14px;

        padding:13px;

    }

}
/*=========================================
  ABOUT SECTION
=========================================*/

.about{

    position:relative;

    overflow:hidden;

}

.about-wrapper{

    display:grid;

    grid-template-columns:1fr 1fr;

    align-items:center;

    gap:80px;

}

/*=========================================
  ABOUT IMAGE
=========================================*/

.about-image{

    display:flex;

    justify-content:center;

    position:relative;

}

.image-card{

    position:relative;

    width:420px;
    height:520px;

    border-radius:30px;

    background:var(--card);

    border:1px solid var(--card-border);

    backdrop-filter:var(--blur);

    box-shadow:var(--shadow);

    overflow:hidden;

    display:flex;

    justify-content:center;
    align-items:center;

}

.image-card::before{

    content:"";

    position:absolute;

    inset:0;

    background:
    linear-gradient(
        135deg,
        rgba(37,99,235,.12),
        rgba(124,58,237,.12),
        rgba(56,189,248,.12)
    );

}

/*=========================================
  EXPERIENCE BOX
=========================================*/

.experience-box{

    position:absolute;

    top:30px;
    left:-35px;

    width:170px;

    padding:25px;

    border-radius:20px;

    background:var(--gradient);

    color:#fff;

    text-align:center;

    box-shadow:var(--shadow);

    animation:float 4s ease-in-out infinite;

    z-index:2;

}

.experience-box h2{

    font-size:42px;

    margin-bottom:8px;

    font-weight:700;

}

.experience-box p{

    font-size:14px;

    line-height:1.6;

}

/*=========================================
  ABOUT LOGO
=========================================*/

.image-card .logo-circle{

    width:170px;
    height:170px;

    border-radius:50%;

    display:flex;

    justify-content:center;
    align-items:center;

    background:var(--gradient);

    color:#fff;

    font-size:48px;

    font-family:'Cinzel',serif;

    font-weight:700;

    box-shadow:
    0 0 40px rgba(37,99,235,.35);

    z-index:2;

    animation:float 5s ease-in-out infinite;

}

/*=========================================
  ABOUT CONTENT
=========================================*/

.about-content{

    animation:fadeUp .8s ease;

}

.section-tag{

    display:inline-block;

    padding:10px 22px;

    border-radius:50px;

    background:var(--card);

    border:1px solid var(--card-border);

    color:var(--secondary);

    font-size:14px;

    font-weight:700;

    letter-spacing:1px;

    margin-bottom:25px;

}

.about-content h2{

    font-family:'Cinzel',serif;

    font-size:48px;

    line-height:1.3;

    margin-bottom:25px;

}

.about-content p{

    color:var(--text-light);

    line-height:1.9;

    margin-bottom:20px;

}
/*=========================================
  ABOUT FEATURES
=========================================*/

.about-features{

    display:grid;

    grid-template-columns:repeat(2,1fr);

    gap:25px;

    margin:45px 0;

}

/*=========================================
  FEATURE CARD
=========================================*/

.feature{

    display:flex;

    align-items:flex-start;

    gap:18px;

    padding:22px;

    background:var(--card);

    border:1px solid var(--card-border);

    backdrop-filter:var(--blur);

    border-radius:20px;

    transition:var(--transition);

    position:relative;

    overflow:hidden;

}

.feature::before{

    content:"";

    position:absolute;

    top:0;
    left:-100%;

    width:100%;
    height:100%;

    background:linear-gradient(
        90deg,
        transparent,
        rgba(255,255,255,.08),
        transparent
    );

    transition:.8s;

}

.feature:hover::before{

    left:100%;

}

.feature:hover{

    transform:translateY(-8px);

    border-color:rgba(56,189,248,.35);

    box-shadow:var(--shadow);

}

/*=========================================
  FEATURE ICON
=========================================*/

.feature i{

    width:65px;
    height:65px;

    min-width:65px;

    display:flex;

    justify-content:center;
    align-items:center;

    border-radius:50%;

    background:var(--gradient);

    color:#fff;

    font-size:24px;

    box-shadow:0 10px 25px rgba(37,99,235,.25);

    transition:var(--transition);

}

.feature:hover i{

    transform:rotate(10deg) scale(1.08);

}

/*=========================================
  FEATURE TEXT
=========================================*/

.feature h4{

    font-size:22px;

    margin-bottom:8px;

    font-weight:600;

}

.feature p{

    margin:0;

    color:var(--text-light);

    line-height:1.7;

    font-size:15px;

}

/*=========================================
  ABOUT BUTTON
=========================================*/

.about-content .btn{

    margin-top:10px;

    min-width:200px;

}
/*=========================================
  WHY CHOOSE US
=========================================*/

.why-us{

    position:relative;

    overflow:hidden;

}

.why-grid{

    display:grid;

    grid-template-columns:repeat(4,1fr);

    gap:30px;

}

.why-card{

    padding:40px 30px;

    text-align:center;

    background:var(--card);

    border:1px solid var(--card-border);

    backdrop-filter:var(--blur);

    border-radius:24px;

    transition:var(--transition);

    position:relative;

    overflow:hidden;

}

.why-card::before{

    content:"";

    position:absolute;

    inset:0;

    background:linear-gradient(
        135deg,
        rgba(37,99,235,.08),
        rgba(56,189,248,.08),
        rgba(124,58,237,.08)
    );

    opacity:0;

    transition:.4s;

}

.why-card:hover::before{

    opacity:1;

}

.why-card:hover{

    transform:translateY(-12px);

    box-shadow:var(--shadow);

    border-color:rgba(56,189,248,.35);

}

.why-card i{

    width:90px;
    height:90px;

    margin:0 auto 25px;

    display:flex;
    justify-content:center;
    align-items:center;

    border-radius:50%;

    background:var(--gradient);

    color:#fff;

    font-size:34px;

    box-shadow:0 15px 35px rgba(37,99,235,.25);

    position:relative;

    z-index:1;

}

.why-card h3{

    font-size:24px;

    font-family:'Cinzel',serif;

    margin-bottom:15px;

    position:relative;

    z-index:1;

}

.why-card p{

    color:var(--text-light);

    line-height:1.8;

    position:relative;

    z-index:1;

}

/*=========================================
  STATS SECTION
=========================================*/

.stats{

    padding:80px 0;

}

.stats-grid{

    display:grid;

    grid-template-columns:repeat(4,1fr);

    gap:30px;

}

.stat-box{

    padding:40px 25px;

    text-align:center;

    background:var(--card);

    border:1px solid var(--card-border);

    backdrop-filter:var(--blur);

    border-radius:22px;

    transition:var(--transition);

}

.stat-box:hover{

    transform:translateY(-10px);

    box-shadow:var(--shadow);

    border-color:rgba(56,189,248,.35);

}

.stat-box h2{

    font-size:48px;

    color:var(--secondary);

    margin-bottom:12px;

    font-weight:700;

}

.stat-box p{

    color:var(--text-light);

    font-size:16px;

    letter-spacing:.5px;

}

/*=========================================
  RESPONSIVE
=========================================*/

@media (max-width:1100px){

    .about-wrapper{

        grid-template-columns:1fr;

        text-align:center;

        gap:60px;

    }

    .about-features{

        grid-template-columns:repeat(2,1fr);

    }

    .why-grid{

        grid-template-columns:repeat(2,1fr);

    }

    .stats-grid{

        grid-template-columns:repeat(2,1fr);

    }

}

@media (max-width:768px){

    .about-content h2{

        font-size:38px;

    }

    .image-card{

        width:100%;
        max-width:360px;
        height:450px;

    }

    .experience-box{

        left:20px;

        top:20px;

    }

    .about-features{

        grid-template-columns:1fr;

    }

}

@media (max-width:576px){

    .why-grid{

        grid-template-columns:1fr;

    }

    .stats-grid{

        grid-template-columns:1fr;

    }

    .about-content h2{

        font-size:32px;

    }

    .section-tag{

        font-size:12px;

    }

    .feature{

        flex-direction:column;

        text-align:center;

        align-items:center;

    }

    .feature i{

        margin-bottom:10px;

    }

}
/*=========================================
  REVIEWS SECTION
=========================================*/

.reviews{

    position:relative;

    overflow:hidden;

}

.reviews-grid{

    display:grid;

    grid-template-columns:repeat(3,1fr);

    gap:30px;

}

/*=========================================
  REVIEW CARD
=========================================*/

.review-card{

    position:relative;

    padding:35px 30px;

    background:var(--card);

    border:1px solid var(--card-border);

    backdrop-filter:var(--blur);

    border-radius:25px;

    transition:var(--transition);

    overflow:hidden;

}

.review-card::before{

    content:"";

    position:absolute;

    top:0;
    left:-100%;

    width:100%;
    height:100%;

    background:linear-gradient(
        90deg,
        transparent,
        rgba(255,255,255,.08),
        transparent
    );

    transition:.8s;

}

.review-card:hover::before{

    left:100%;

}

.review-card:hover{

    transform:translateY(-12px);

    border-color:rgba(56,189,248,.35);

    box-shadow:var(--shadow);

}

/*=========================================
  QUOTE ICON
=========================================*/

.quote{

    width:70px;
    height:70px;

    display:flex;

    justify-content:center;
    align-items:center;

    border-radius:50%;

    background:var(--gradient);

    color:#fff;

    font-size:28px;

    margin-bottom:25px;

    box-shadow:0 12px 30px rgba(37,99,235,.25);

}

.review-card p{

    color:var(--text-light);

    line-height:1.9;

    margin-bottom:25px;

    font-size:16px;

}

/*=========================================
  STARS
=========================================*/

.stars{

    display:flex;

    gap:6px;

    margin-bottom:30px;

    color:#FFD54A;

    font-size:18px;

}

/*=========================================
  REVIEW USER
=========================================*/

.review-user{

    display:flex;

    align-items:center;

    gap:18px;

}

.user-image{

    width:65px;
    height:65px;

    border-radius:50%;

    display:flex;

    justify-content:center;
    align-items:center;

    background:var(--gradient);

    color:#fff;

    font-size:24px;

    box-shadow:var(--shadow);

}

.review-user h4{

    font-size:20px;

    margin-bottom:5px;

    font-weight:600;

}

.review-user span{

    color:var(--text-light);

    font-size:14px;

}
/*=========================================
  NEWSLETTER SECTION
=========================================*/

.newsletter{

    position:relative;

    overflow:hidden;

}

.newsletter-box{

    max-width:900px;

    margin:auto;

    padding:70px 60px;

    text-align:center;

    border-radius:30px;

    background:var(--card);

    border:1px solid var(--card-border);

    backdrop-filter:var(--blur);

    box-shadow:var(--shadow);

    position:relative;

    overflow:hidden;

}

.newsletter-box::before{

    content:"";

    position:absolute;

    inset:0;

    background:linear-gradient(
        135deg,
        rgba(37,99,235,.08),
        rgba(56,189,248,.08),
        rgba(124,58,237,.08)
    );

    pointer-events:none;

}

.newsletter-box>*{

    position:relative;

    z-index:1;

}

.newsletter-box span{

    display:inline-block;

    color:var(--secondary);

    font-size:14px;

    font-weight:700;

    letter-spacing:3px;

    text-transform:uppercase;

    margin-bottom:15px;

}

.newsletter-box h2{

    font-family:'Cinzel',serif;

    font-size:42px;

    line-height:1.4;

    margin-bottom:20px;

}

.newsletter-box p{

    max-width:650px;

    margin:0 auto 35px;

    color:var(--text-light);

    line-height:1.9;

}

/*=========================================
  NEWSLETTER FORM
=========================================*/

.newsletter-form{

    display:flex;

    align-items:center;

    justify-content:center;

    gap:18px;

    flex-wrap:wrap;

}

.newsletter-form input{

    flex:1;

    min-width:280px;

    height:60px;

    padding:0 25px;

    border-radius:50px;

    background:rgba(255,255,255,.08);

    border:1px solid var(--card-border);

    color:var(--text);

    transition:var(--transition);

}

.newsletter-form input::placeholder{

    color:var(--text-light);

}

.newsletter-form input:focus{

    border-color:var(--secondary);

    box-shadow:0 0 20px rgba(56,189,248,.25);

}

.newsletter-form button{

    height:60px;

    padding:0 35px;

    border-radius:50px;

    display:flex;

    align-items:center;

    gap:10px;

    background:var(--gradient);

    color:#fff;

    font-weight:600;

    box-shadow:var(--shadow);

    transition:var(--transition);

}

.newsletter-form button:hover{

    transform:translateY(-4px);

}

/*=========================================
  CALL TO ACTION
=========================================*/

.cta{

    padding-top:40px;

}

.cta-box{

    text-align:center;

    padding:70px 40px;

    border-radius:30px;

    background:var(--gradient);

    color:#fff;

    box-shadow:var(--shadow);

}

.cta-box h2{

    font-family:'Cinzel',serif;

    font-size:44px;

    margin-bottom:20px;

}

.cta-box p{

    max-width:700px;

    margin:0 auto 35px;

    line-height:1.9;

    font-size:17px;

    opacity:.95;

}

.cta-box .btn{

    background:#fff;

    color:#111827;

}

.cta-box .btn:hover{

    transform:translateY(-5px);

}

/*=========================================
  RESPONSIVE
=========================================*/

@media (max-width:768px){

    .newsletter-box{

        padding:50px 30px;

    }

    .newsletter-box h2{

        font-size:34px;

    }

    .cta-box{

        padding:50px 25px;

    }

    .cta-box h2{

        font-size:34px;

    }

    .newsletter-form{

        flex-direction:column;

    }

    .newsletter-form input,
    .newsletter-form button{

        width:100%;

    }

}

@media (max-width:576px){

    .newsletter-box h2{

        font-size:28px;

    }

    .cta-box h2{

        font-size:28px;

    }

    .newsletter-box{

        padding:40px 20px;

    }

}
/*=========================================
  CONTACT SECTION
=========================================*/

.contact{

    position:relative;

    overflow:hidden;

}

.contact-wrapper{

    display:grid;

    grid-template-columns:1fr 1.3fr;

    gap:40px;

    align-items:start;

}

.contact-info{

    display:flex;

    flex-direction:column;

    gap:25px;

}

.info-box{

    display:flex;

    align-items:center;

    gap:20px;

    padding:28px;

    background:var(--card);

    border:1px solid var(--card-border);

    backdrop-filter:var(--blur);

    border-radius:22px;

    transition:var(--transition);

}

.info-box:hover{

    transform:translateY(-8px);

    box-shadow:var(--shadow);

    border-color:rgba(56,189,248,.35);

}

.info-box i{

    width:65px;
    height:65px;

    display:flex;
    align-items:center;
    justify-content:center;

    border-radius:50%;

    background:var(--gradient);

    color:#fff;

    font-size:24px;

}

.info-box h4{

    font-size:22px;

    margin-bottom:8px;

}

.info-box p{

    color:var(--text-light);

    line-height:1.7;

}

/*=========================================
  CONTACT FORM
=========================================*/

.contact-form{

    background:var(--card);

    border:1px solid var(--card-border);

    backdrop-filter:var(--blur);

    border-radius:25px;

    padding:40px;

    display:flex;

    flex-direction:column;

    gap:20px;

}

.contact-form input,
.contact-form textarea{

    width:100%;

    padding:18px 20px;

    border-radius:16px;

    background:rgba(255,255,255,.06);

    border:1px solid var(--card-border);

    color:var(--text);

    resize:none;

    transition:var(--transition);

}

.contact-form input:focus,
.contact-form textarea:focus{

    border-color:var(--secondary);

    box-shadow:0 0 18px rgba(56,189,248,.25);

}

.contact-form input::placeholder,
.contact-form textarea::placeholder{

    color:var(--text-light);

}

.contact-form button{

    margin-top:10px;

}

/*=========================================
  FOOTER
=========================================*/

footer{

    background:var(--bg-secondary);

    border-top:1px solid var(--card-border);

    padding:80px 0 30px;

}

.footer-grid{

    display:grid;

    grid-template-columns:2fr 1fr 1fr 1fr;

    gap:40px;

    margin-bottom:50px;

}

.footer-col h2{

    font-family:'Cinzel',serif;

    margin-bottom:20px;

    font-size:28px;

}

.footer-col h2 span{

    color:var(--secondary);

}

.footer-col h3{

    margin-bottom:20px;

    font-size:22px;

}

.footer-col p{

    color:var(--text-light);

    line-height:1.8;

}

.footer-col ul{

    display:flex;

    flex-direction:column;

    gap:14px;

}

.footer-col ul li a{

    color:var(--text-light);

    transition:var(--transition);

}

.footer-col ul li a:hover{

    color:var(--secondary);

    padding-left:8px;

}

/*=========================================
  SOCIAL ICONS
=========================================*/

.social-icons{

    display:flex;

    gap:15px;

    margin-top:30px;

}

.social-icons a{

    width:48px;
    height:48px;

    display:flex;

    justify-content:center;
    align-items:center;

    border-radius:50%;

    background:var(--card);

    border:1px solid var(--card-border);

    transition:var(--transition);

}

.social-icons a:hover{

    background:var(--gradient);

    color:#fff;

    transform:translateY(-5px);

}

.footer-bottom{

    text-align:center;

    padding-top:30px;

    border-top:1px solid rgba(255,255,255,.08);

}

.footer-bottom p{

    color:var(--text-light);

}

/*=========================================
  SCROLL TO TOP
=========================================*/

.scroll-top{

    position:fixed;

    right:30px;
    bottom:30px;

    width:55px;
    height:55px;

    border:none;

    border-radius:50%;

    background:var(--gradient);

    color:#fff;

    font-size:20px;

    display:flex;

    justify-content:center;
    align-items:center;

    box-shadow:var(--shadow);

    cursor:pointer;

    opacity:0;

    visibility:hidden;

    transition:var(--transition);

    z-index:999;

}

.scroll-top.show{

    opacity:1;

    visibility:visible;

}

.scroll-top:hover{

    transform:translateY(-6px);

}

/*=========================================
  RESPONSIVE
=========================================*/

@media(max-width:992px){

    .contact-wrapper{

        grid-template-columns:1fr;

    }

    .footer-grid{

        grid-template-columns:repeat(2,1fr);

    }

}

@media(max-width:768px){

    .contact-form{

        padding:30px;

    }

    .footer-grid{

        grid-template-columns:1fr;

        text-align:center;

    }

    .social-icons{

        justify-content:center;

    }

}

@media(max-width:576px){

    .contact-form{

        padding:22px;

    }

    .info-box{

        flex-direction:column;

        text-align:center;

    }

    .scroll-top{

        width:50px;
        height:50px;

        right:20px;
        bottom:20px;

    }

}
    </style>
  <script>
    /*=========================================
  LOADER
=========================================*/

window.addEventListener("load", () => {

    const loader = document.querySelector(".loader");
    const welcome = document.querySelector(".welcome-screen");

    setTimeout(() => {

        loader.classList.add("hide");

        setTimeout(() => {
            welcome.classList.add("show");
        }, 700);

    }, 4000);

});


/*=========================================
  WELCOME FORM
=========================================*/

const welcomeForm = document.getElementById("welcomeForm");
const welcomeScreen = document.querySelector(".welcome-screen");
const website = document.querySelector(".website");

if (welcomeForm) {

    welcomeForm.addEventListener("submit", function (e) {

        e.preventDefault();

        welcomeScreen.classList.remove("show");

        website.classList.add("show");

    });

}


/*=========================================
  STICKY HEADER
=========================================*/

const header = document.querySelector("header");

window.addEventListener("scroll", () => {

    if (window.scrollY > 80) {

        header.classList.add("sticky");

    } else {

        header.classList.remove("sticky");

    }

});


/*=========================================
  SCROLL TO TOP BUTTON
=========================================*/

const scrollTopBtn = document.getElementById("scrollTop");

window.addEventListener("scroll", () => {

    if (window.scrollY > 500) {

        scrollTopBtn.classList.add("show");

    } else {

        scrollTopBtn.classList.remove("show");

    }

});

scrollTopBtn.addEventListener("click", () => {

    window.scrollTo({

        top: 0,
        behavior: "smooth"

    });

});
/*=========================================
  LIGHT / DARK MODE
=========================================*/

const themeBtn = document.getElementById("themeToggle");
const body = document.body;

// Load Saved Theme
if (localStorage.getItem("theme") === "light") {

    body.classList.add("light-mode");

    if (themeBtn) {
        themeBtn.innerHTML = '<i class="fa-solid fa-moon"></i>';
    }

}

// Toggle Theme
if (themeBtn) {

    themeBtn.addEventListener("click", () => {

        body.classList.toggle("light-mode");

        if (body.classList.contains("light-mode")) {

            localStorage.setItem("theme", "light");

            themeBtn.innerHTML =
                '<i class="fa-solid fa-moon"></i>';

        } else {

            localStorage.setItem("theme", "dark");

            themeBtn.innerHTML =
                '<i class="fa-solid fa-sun"></i>';

        }

    });

}


/*=========================================
  MOBILE MENU
=========================================*/

const menuBtn = document.getElementById("menuBtn");
const navLinks = document.getElementById("navLinks");
const navOverlay = document.getElementById("navOverlay");

if (menuBtn) {

    menuBtn.addEventListener("click", () => {

        menuBtn.classList.toggle("active");

        navLinks.classList.toggle("active");

        navOverlay.classList.toggle("show");

    });

}

// Close Menu on Overlay Click
if (navOverlay) {

    navOverlay.addEventListener("click", () => {

        menuBtn.classList.remove("active");

        navLinks.classList.remove("active");

        navOverlay.classList.remove("show");

    });

}

// Close Menu After Clicking Link
document.querySelectorAll(".nav-links a").forEach(link => {

    link.addEventListener("click", () => {

        menuBtn.classList.remove("active");

        navLinks.classList.remove("active");

        navOverlay.classList.remove("show");

    });

});
/*=========================================
  ACTIVE NAVIGATION (SCROLL SPY)
=========================================*/

const sections = document.querySelectorAll("section[id]");
const navItems = document.querySelectorAll(".nav-links a");

function activeMenu() {

    const scrollY = window.pageYOffset;

    sections.forEach(section => {

        const sectionHeight = section.offsetHeight;
        const sectionTop = section.offsetTop - 150;
        const sectionId = section.getAttribute("id");

        if (
            scrollY >= sectionTop &&
            scrollY < sectionTop + sectionHeight
        ) {

            navItems.forEach(link => {

                link.classList.remove("active");

            });

            const activeLink = document.querySelector(
                `.nav-links a[href="#${sectionId}"]`
            );

            if (activeLink) {

                activeLink.classList.add("active");

            }

        }

    });

}

window.addEventListener("scroll", activeMenu);


/*=========================================
  SMOOTH SCROLL FOR NAV LINKS
=========================================*/

navItems.forEach(link => {

    link.addEventListener("click", function (e) {

        const targetId = this.getAttribute("href");

        if (targetId.startsWith("#")) {

            e.preventDefault();

            const target = document.querySelector(targetId);

            if (target) {

                window.scrollTo({

                    top: target.offsetTop - 80,
                    behavior: "smooth"

                });

            }

        }

    });

});


/*=========================================
  HEADER SHADOW ON SCROLL
=========================================*/

window.addEventListener("scroll", () => {

    if (window.scrollY > 20) {

        header.style.boxShadow =
            "0 12px 35px rgba(0,0,0,.25)";

    } else {

        header.style.boxShadow = "none";

    }

});
  </script>
</head>

<body>

    <!-- ==========================================
                    LOADER
    =========================================== -->

    <div class="loader" id="loader">

        <div class="loader-content">

            <div class="loader-logo">
                <span>S</span>-<span>Y</span>
            </div>

            <h1>Sherdil Yousafzai</h1>

            <p>Luxury Collection</p>

            <div class="loading-bar">
                <span></span>
            </div>

        </div>

    </div>

    <!-- ==========================================
                WELCOME SCREEN
    =========================================== -->

    <section class="welcome-screen" id="welcome">

        <div class="welcome-card">

            <h4>WELCOME TO</h4>

            <h1>S-Y COLLECTION</h1>

            <p>
                Premium Watches & Luxury Perfumes
            </p>

            <form id="welcomeForm">

                <div class="input-box">

                    <i class="fa-solid fa-user"></i>

                    <input type="text" placeholder="Enter Your Name" required>

                </div>

                <div class="input-box">

                    <i class="fa-solid fa-envelope"></i>

                    <input type="email" placeholder="Enter Your Email" required>

                </div>

                <button type="submit">

                    ENTER

                    <i class="fa-solid fa-arrow-right"></i>

                </button>

            </form>

        </div>

    </section>

    <!-- ==========================================
                    MAIN WEBSITE
    =========================================== -->

    <div class="website" id="website">

        <!-- ======================================
                    HEADER
        ======================================= -->

        <header>

            <div class="container">

                <nav class="navbar">

                    <!-- Logo -->

                    <a href="#" class="logo">

                        <span>S-Y</span>

                        <h2>Sherdil Yousafzai</h2>

                    </a>

                    <!-- Navigation -->

                    <ul class="nav-links">

                        <li><a href="#home">Home</a></li>

                        <li><a href="#watches">Watches</a></li>

                        <li><a href="#men">Men</a></li>

                        <li><a href="#women">Women</a></li>

                        <li><a href="#unisex">Unisex</a></li>

                        <li><a href="#about">About</a></li>

                        <li><a href="#contact">Contact</a></li>

                    </ul>

                    <!-- Right Side -->

                    <div class="nav-right">

                        <!-- Search -->

                        <button class="icon-btn">

                            <i class="fa-solid fa-magnifying-glass"></i>

                        </button>

                        <!-- Dark Mode -->

                        <button id="themeToggle" class="icon-btn">

                            <i class="fa-solid fa-moon"></i>

                        </button>

                        <!-- Mobile Menu -->

                        <button class="menu-btn">

                            <i class="fa-solid fa-bars"></i>

                        </button>

                    </div>

                </nav>

            </div>

        </header>

        <!-- ======================================
                HERO SECTION
                (NEXT PART)
        ======================================= -->
        <!-- ======================================
                    HERO SECTION
        ======================================= -->

        <section class="hero" id="home">

            <div class="hero-bg"></div>

            <div class="container">

                <div class="hero-content">

                    <span class="hero-badge">
                        Luxury Watches & Premium Perfumes
                    </span>

                    <h1>
                        Elevate Your
                        <span>Style</span>
                        With Timeless Luxury
                    </h1>

                    <p>
                        Discover an exclusive collection of premium watches
                        and luxury fragrances crafted for men, women,
                        and everyone who appreciates elegance.
                    </p>

                    <div class="hero-buttons">

                        <a href="#watches" class="btn btn-primary">
                            Explore Collection
                        </a>

                        <a href="#about" class="btn btn-secondary">
                            Learn More
                        </a>

                    </div>

                    <div class="hero-stats">

                        <div class="stat">

                            <h2>250+</h2>

                            <p>Luxury Products</p>

                        </div>

                        <div class="stat">

                            <h2>10K+</h2>

                            <p>Happy Visitors</p>

                        </div>

                        <div class="stat">

                            <h2>100%</h2>

                            <p>Premium Quality</p>

                        </div>

                    </div>

                </div>

                <div class="hero-image">

                    <div class="glass-circle circle1"></div>

                    <div class="glass-circle circle2"></div>

                    <div class="glass-circle circle3"></div>

                    <div class="floating-card watch-card">

                        <i class="fa-regular fa-clock"></i>

                        <h3>Luxury Watches</h3>

                    </div>

                    <div class="floating-card perfume-card">

                        <i class="fa-solid fa-wine-bottle"></i>

                        <h3>Premium Perfumes</h3>

                    </div>

                    <div class="main-glass-card">

                        <div class="logo-circle">

                            <span>S-Y</span>

                        </div>

                        <h2>Sherdil Yousafzai</h2>

                        <p>
                            Premium Collection
                        </p>

                    </div>

                </div>

            </div>

            <a href="#watches" class="scroll-down">

                <span></span>

            </a>

        </section>

        <!-- ======================================
                FEATURED CATEGORIES
        ======================================= -->

        <section class="categories">

            <div class="container">

                <div class="section-title">

                    <span>Our Collection</span>

                    <h2>
                        Luxury Categories
                    </h2>

                    <p>
                        Explore our premium selection crafted for
                        elegance, confidence and timeless style.
                    </p>

                </div>

                <div class="category-grid">

                    <div class="category-card">

                        <i class="fa-regular fa-clock"></i>

                        <h3>Luxury Watches</h3>

                        <p>
                            Premium timepieces for every occasion.
                        </p>

                    </div>

                    <div class="category-card">

                        <i class="fa-solid fa-user-tie"></i>

                        <h3>Men Perfumes</h3>

                        <p>
                            Powerful and long-lasting fragrances.
                        </p>

                    </div>

                    <div class="category-card">

                        <i class="fa-solid fa-heart"></i>

                        <h3>Women Perfumes</h3>

                        <p>
                            Elegant and luxurious floral scents.
                        </p>

                    </div>

                    <div class="category-card">

                        <i class="fa-solid fa-star"></i>

                        <h3>Unisex Collection</h3>

                        <p>
                            Modern fragrances loved by everyone.
                        </p>

                    </div>

                </div>

            </div>

        </section>

        <!-- ======================================
            WATCHES SECTION
            (NEXT PART)
        ======================================= -->
        <!-- ======================================
                    WATCHES SECTION
        ======================================= -->

        <section class="products" id="watches">

            <div class="container">

                <div class="section-title">

                    <span>Premium Timepieces</span>

                    <h2>Luxury Watch Collection</h2>

                    <p>
                        Discover timeless craftsmanship with our exclusive
                        luxury watch collection.
                    </p>

                </div>

                <div class="product-grid">

                    <!-- Card 1 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.rolex.avif" alt="Rolex Watch">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Rolex Submariner</h3>

                            <div class="rating">

                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>

                            </div>

                            <h4>$12,999</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Card 2 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.omega.webp" alt="Omega Watch">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Omega Seamaster</h3>

                            <div class="rating">

                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>

                            </div>

                            <h4>$9,499</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Card 3 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.patak.jfif" alt="Patek Philippe">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Patek Philippe</h3>

                            <div class="rating">

                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>

                            </div>

                            <h4>$21,999</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Card 4 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.tag hauer.webp" alt="Tag Heuer">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Tag Heuer Carrera</h3>

                            <div class="rating">

                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-regular fa-star"></i>

                            </div>

                            <h4>$6,899</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Card 5 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.casio.jfif" alt="Casio">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Casio Edifice</h3>

                            <div class="rating">

                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>
                                <i class="fa-regular fa-star"></i>

                            </div>

                            <h4>$799</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Card 6 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.seiko.jfif" alt="Seiko">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Seiko Presage</h3>

                            <div class="rating">

                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>

                            </div>

                            <h4>$1,299</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                </div>

            </div>

        </section>

        <!-- ======================================
                MEN PERFUME SECTION
                (NEXT PART)
        ======================================= -->
        <!-- ======================================
                MEN'S PERFUME COLLECTION
        ======================================= -->

        <section class="products" id="men">

            <div class="container">

                <div class="section-title">

                    <span>Luxury Fragrance</span>

                    <h2>Men's Perfume Collection</h2>

                    <p>
                        Discover premium fragrances designed for confidence,
                        elegance and unforgettable impressions.
                    </p>

                </div>

                <div class="product-grid">

                    <!-- Product 1 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.dior.jfif" alt="Dior Sauvage">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Dior Sauvage</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                            </div>

                            <h4>$165</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Product 2 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.blue.jpg" alt="Bleu de Chanel">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Bleu de Chanel</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>
                            </div>

                            <h4>$180</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Product 3 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.creed.webp" alt="Creed Aventus">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Creed Aventus</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                            </div>

                            <h4>$420</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Product 4 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.tom.webp" alt="Tom Ford Oud Wood">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Tom Ford Oud Wood</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>
                            </div>

                            <h4>$395</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Product 5 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.verche.webp" alt="Versace Eros">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Versace Eros</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-regular fa-star"></i>
                            </div>

                            <h4>$145</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Product 6 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.aqua.avif" alt="Acqua Di Gio">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Acqua Di Gio</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>
                            </div>

                            <h4>$155</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                </div>

            </div>

        </section>

        <!-- ======================================
            WOMEN'S PERFUME COLLECTION
            (PART 4.2)
        ======================================= -->
        <!-- ======================================
                WOMEN'S PERFUME COLLECTION
        ======================================= -->

        <section class="products" id="women">

            <div class="container">

                <div class="section-title">

                    <span>Luxury Fragrance</span>

                    <h2>Women's Perfume Collection</h2>

                    <p>
                        Elegant, floral and luxurious fragrances crafted
                        for women who love sophistication and timeless beauty.
                    </p>

                </div>

                <div class="product-grid">

                    <!-- Product 1 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.coco.jfif" alt="Chanel Coco Mademoiselle">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Chanel Coco Mademoiselle</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                            </div>

                            <h4>$185</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Product 2 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.bloom.webp" alt="Gucci Bloom">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Gucci Bloom</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>
                            </div>

                            <h4>$165</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Product 3 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.vsl.jpg" alt="YSL Libre">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>YSL Libre</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                            </div>

                            <h4>$172</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Product 4 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.adore.webp" alt="Dior J'adore">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Dior J'adore</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>
                            </div>

                            <h4>$178</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Product 5 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.opium.jfif" alt="Black Opium">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Black Opium</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-regular fa-star"></i>
                            </div>

                            <h4>$160</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Product 6 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.missdior.jfif" alt="Miss Dior">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Miss Dior</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>
                            </div>

                            <h4>$170</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                </div>

            </div>

        </section>

        <!-- ======================================
            UNISEX PERFUME COLLECTION
            (PART 4.3)
        ======================================= -->
        <!-- ======================================
                UNISEX PERFUME COLLECTION
        ======================================= -->

        <section class="products" id="unisex">

            <div class="container">

                <div class="section-title">

                    <span>Signature Collection</span>

                    <h2>Unisex Perfume Collection</h2>

                    <p>
                        Sophisticated fragrances designed for everyone who
                        appreciates timeless elegance and modern luxury.
                    </p>

                </div>

                <div class="product-grid">

                    <!-- Product 1 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.bakarat.jfif" alt="Baccarat Rouge 540">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Baccarat Rouge 540</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                            </div>

                            <h4>$395</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Product 2 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.vanille.jpg" alt="Tom Ford Tobacco Vanille">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Tom Ford Tobacco Vanille</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>
                            </div>

                            <h4>$320</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Product 3 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.water creed.jpg" alt="Creed Silver Mountain Water">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Creed Silver Mountain Water</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                            </div>

                            <h4>$410</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Product 4 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.jo malone.avif" alt="Jo Malone Wood Sage & Sea Salt">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>Jo Malone Wood Sage & Sea Salt</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-regular fa-star"></i>
                            </div>

                            <h4>$185</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Product 5 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.ck.jfif" alt="CK One">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>

                        </div>

                        <div class="product-info">

                            <h3>CK One</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star-half-stroke"></i>
                                <i class="fa-regular fa-star"></i>
                            </div>

                            <h4>$95</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                    <!-- Product 6 -->

                    <div class="product-card">

                        <div class="product-image">

                            <img src="./img/img.33.jfif" alt="Le Labo Santal 33">

                            <button class="wishlist">
                                <i class="fa-regular fa-heart"></i>
                            </button>
                        </div>

                        <div class="product-info">

                            <h3>Le Labo Santal 33</h3>

                            <div class="rating">
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                                <i class="fa-solid fa-star"></i>
                            </div>

                            <h4>$310</h4>

                            <a href="#" class="product-btn">
                                View Details
                            </a>

                        </div>

                    </div>

                </div>

            </div>

        </section>

        <!-- ======================================
                ABOUT US
                (PART 5.1)
        ======================================= -->
        <!-- ======================================
                    ABOUT SECTION
        ======================================= -->

        <section class="about" id="about">

            <div class="container">

                <div class="about-wrapper">

                    <!-- Left Side -->

                    <div class="about-image">

                        <div class="image-card">

                            <div class="experience-box">

                                <h2>10+</h2>

                                <p>Years of Luxury Inspiration</p>

                            </div>

                            <div class="logo-circle">

                                <span>S-Y</span>

                            </div>

                        </div>

                    </div>

                    <!-- Right Side -->

                    <div class="about-content">

                        <span class="section-tag">

                            ABOUT S-Y COLLECTION

                        </span>

                        <h2>

                            Crafted For People Who Appreciate
                            Luxury, Style & Elegance.

                        </h2>

                        <p>

                            Welcome to <strong>S-Y | Sherdil Yousafzai</strong>,
                            a premium destination where timeless luxury meets
                            modern style.

                        </p>

                        <p>

                            Our carefully selected watches and fragrances
                            represent elegance, confidence and sophistication.
                            Every product is chosen to deliver a premium
                            experience.

                        </p>

                        <!-- Features -->

                        <div class="about-features">

                            <div class="feature">

                                <i class="fa-solid fa-gem"></i>

                                <div>

                                    <h4>Premium Quality</h4>

                                    <p>
                                        Carefully selected luxury products.
                                    </p>

                                </div>

                            </div>

                            <div class="feature">

                                <i class="fa-solid fa-shield-halved"></i>

                                <div>

                                    <h4>Trusted Collection</h4>

                                    <p>
                                        Designed for style and confidence.
                                    </p>

                                </div>

                            </div>

                            <div class="feature">

                                <i class="fa-solid fa-truck-fast"></i>

                                <div>

                                    <h4>Fast Delivery</h4>

                                    <p>
                                        Quick and secure shipping experience.
                                    </p>

                                </div>

                            </div>

                            <div class="feature">

                                <i class="fa-solid fa-award"></i>

                                <div>

                                    <h4>Luxury Experience</h4>

                                    <p>
                                        Premium design with modern elegance.
                                    </p>

                                </div>

                            </div>

                        </div>

                        <a href="#contact" class="btn btn-primary">

                            Contact Us

                        </a>

                    </div>

                </div>

            </div>

        </section>

        <!-- ======================================
                WHY CHOOSE US
        ======================================= -->

        <section class="why-us">

            <div class="container">

                <div class="section-title">

                    <span>WHY CHOOSE US</span>

                    <h2>
                        Experience Premium Excellence
                    </h2>

                    <p>

                        Every detail is designed to provide
                        elegance, quality and luxury.

                    </p>

                </div>

                <div class="why-grid">

                    <div class="why-card">

                        <i class="fa-solid fa-crown"></i>

                        <h3>Luxury Products</h3>

                        <p>

                            Carefully curated premium watches
                            and fragrances.

                        </p>

                    </div>

                    <div class="why-card">

                        <i class="fa-solid fa-star"></i>

                        <h3>Top Rated</h3>

                        <p>

                            High quality collections loved
                            by luxury enthusiasts.

                        </p>

                    </div>

                    <div class="why-card">

                        <i class="fa-solid fa-lock"></i>

                        <h3>Secure Shopping</h3>

                        <p>

                            Safe browsing with a premium
                            user experience.

                        </p>

                    </div>

                    <div class="why-card">

                        <i class="fa-solid fa-headset"></i>

                        <h3>24/7 Support</h3>

                        <p>

                            Always ready to help you with
                            every inquiry.

                        </p>

                    </div>

                </div>

            </div>

        </section>

        <!-- ======================================
                ACHIEVEMENTS
        ======================================= -->

        <section class="stats">

            <div class="container">

                <div class="stats-grid">

                    <div class="stat-box">

                        <h2>500+</h2>

                        <p>Luxury Products</p>

                    </div>

                    <div class="stat-box">

                        <h2>15K+</h2>

                        <p>Happy Visitors</p>

                    </div>

                    <div class="stat-box">

                        <h2>100%</h2>

                        <p>Premium Quality</p>

                    </div>

                    <div class="stat-box">

                        <h2>24/7</h2>

                        <p>Customer Support</p>

                    </div>

                </div>

            </div>

        </section>

        <!-- ======================================
                REVIEWS
                (PART 5.2)
        ======================================= -->
        <!-- ======================================
                    CUSTOMER REVIEWS
        ======================================= -->

        <section class="reviews" id="reviews">

            <div class="container">

                <div class="section-title">

                    <span>TESTIMONIALS</span>

                    <h2>What Our Visitors Say</h2>

                    <p>
                        Discover why people love the luxury experience of
                        S-Y | Sherdil Yousafzai Collection.
                    </p>

                </div>

                <div class="reviews-grid">

                    <!-- Review 1 -->

                    <div class="review-card">

                        <div class="quote">

                            <i class="fa-solid fa-quote-left"></i>

                        </div>

                        <p>

                            Beautiful website with a truly premium feel.
                            The luxury watch collection is amazing and the
                            design looks incredibly professional.

                        </p>

                        <div class="stars">

                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>

                        </div>

                        <div class="review-user">

                            <div class="user-image">

                                <i class="fa-solid fa-user"></i>

                            </div>

                            <div>

                                <h4>James Wilson</h4>

                                <span>Watch Collector</span>

                            </div>

                        </div>

                    </div>

                    <!-- Review 2 -->

                    <div class="review-card">

                        <div class="quote">

                            <i class="fa-solid fa-quote-left"></i>

                        </div>

                        <p>

                            The perfume collection is impressive and the
                            animations make the whole website feel premium.

                        </p>

                        <div class="stars">

                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>

                        </div>

                        <div class="review-user">

                            <div class="user-image">

                                <i class="fa-solid fa-user"></i>

                            </div>

                            <div>

                                <h4>Emily Carter</h4>

                                <span>Luxury Fragrance Lover</span>

                            </div>

                        </div>

                    </div>

                    <!-- Review 3 -->

                    <div class="review-card">

                        <div class="quote">

                            <i class="fa-solid fa-quote-left"></i>

                        </div>

                        <p>

                            One of the cleanest luxury collection websites
                            I have seen. Smooth, elegant and modern.

                        </p>

                        <div class="stars">

                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>
                            <i class="fa-solid fa-star"></i>

                        </div>

                        <div class="review-user">

                            <div class="user-image">

                                <i class="fa-solid fa-user"></i>

                            </div>

                            <div>

                                <h4>Daniel Thomas</h4>

                                <span>Fashion Enthusiast</span>

                            </div>

                        </div>

                    </div>

                </div>

            </div>

        </section>

        <!-- ======================================
                    NEWSLETTER
        ======================================= -->

        <section class="newsletter">

            <div class="container">

                <div class="newsletter-box">

                    <span>JOIN OUR COMMUNITY</span>

                    <h2>

                        Stay Updated With Luxury
                        Collections & Exclusive Offers

                    </h2>

                    <p>

                        Subscribe to receive updates about premium watches,
                        luxury perfumes and upcoming collections.

                    </p>

                    <form class="newsletter-form">

                        <input type="email" placeholder="Enter Your Email Address" required>

                        <button type="submit">

                            Subscribe

                            <i class="fa-solid fa-paper-plane"></i>

                        </button>

                    </form>

                </div>

            </div>

        </section>

        <!-- ======================================
                    CALL TO ACTION
        ======================================= -->

        <section class="cta">

            <div class="container">

                <div class="cta-box">

                    <h2>

                        Experience Luxury Like Never Before

                    </h2>

                    <p>

                        Explore premium watches and luxury fragrances
                        crafted for modern elegance.

                    </p>

                    <a href="#watches" class="btn btn-primary">

                        Explore Now

                    </a>

                </div>

            </div>

        </section>

        <!-- ======================================
                CONTACT & FOOTER
                (PART 5.3)
        ======================================= -->
        <!-- ======================================
                    CONTACT SECTION
        ======================================= -->

        <section class="contact" id="contact">

            <div class="container">

                <div class="section-title">

                    <span>CONTACT US</span>

                    <h2>Get In Touch</h2>

                    <p>
                        We'd love to hear from you. Send us your message and
                        we'll get back to you as soon as possible.
                    </p>

                </div>

                <div class="contact-wrapper">

                    <!-- Contact Info -->

                    <div class="contact-info">

                        <div class="info-box">
                            <i class="fa-solid fa-location-dot"></i>

                            <div>
                                <h4>Location</h4>
                                <p>Pakistan</p>
                            </div>

                        </div>

                        <div class="info-box">

                            <i class="fa-solid fa-envelope"></i>

                            <div>

                                <h4>Email</h4>

                                <p>info@sycollection.com</p>

                            </div>

                        </div>

                        <div class="info-box">

                            <i class="fa-solid fa-phone"></i>

                            <div>

                                <h4>Phone</h4>

                                <p>+92 300 1234567</p>

                            </div>

                        </div>

                    </div>

                    <!-- Contact Form -->

                    <form class="contact-form">

                        <input type="text" placeholder="Your Name" required>

                        <input type="email" placeholder="Your Email" required>

                        <input type="text" placeholder="Subject" required>

                        <textarea rows="6" placeholder="Write Your Message..." required></textarea>

                        <button type="submit" class="btn btn-primary">

                            Send Message

                        </button>

                    </form>

                </div>

            </div>

        </section>

        <!-- ======================================
                    FOOTER
        ======================================= -->

        <footer>

            <div class="container">

                <div class="footer-grid">

                    <!-- Column 1 -->

                    <div class="footer-col">

                        <h2>

                            <span>S-Y</span>

                            Sherdil Yousafzai

                        </h2>

                        <p>

                            A premium destination for luxury watches
                            and perfumes designed with elegance,
                            style and modern craftsmanship.

                        </p>

                        <div class="social-icons">

                            <a href="#">
                                <i class="fab fa-facebook-f"></i>
                            </a>

                            <a href="#">
                                <i class="fab fa-instagram"></i>
                            </a>

                            <a href="#">
                                <i class="fab fa-x-twitter"></i>
                            </a>

                            <a href="#">
                                <i class="fab fa-linkedin-in"></i>
                            </a>

                            <a href="#">
                                <i class="fab fa-github"></i>
                            </a>

                        </div>

                    </div>

                    <!-- Column 2 -->

                    <div class="footer-col">

                        <h3>Quick Links</h3>

                        <ul>

                            <li><a href="#home">Home</a></li>

                            <li><a href="#about">About</a></li>

                            <li><a href="#contact">Contact</a></li>

                            <li><a href="#reviews">Reviews</a></li>

                        </ul>

                    </div>

                    <!-- Column 3 -->

                    <div class="footer-col">

                        <h3>Collections</h3>

                        <ul>

                            <li><a href="#watches">Luxury Watches</a></li>

                            <li><a href="#men">Men Perfumes</a></li>

                            <li><a href="#women">Women Perfumes</a></li>

                            <li><a href="#unisex">Unisex Perfumes</a></li>

                        </ul>

                    </div>

                    <!-- Column 4 -->

                    <div class="footer-col">

                        <h3>Support</h3>

                        <ul>

                            <li><a href="#">Privacy Policy</a></li>

                            <li><a href="#">Terms & Conditions</a></li>

                            <li><a href="#">Help Center</a></li>

                            <li><a href="#">FAQs</a></li>

                        </ul>

                    </div>

                </div>

                <div class="footer-bottom">

                    <p>

                        © 2026 S-Y | Sherdil Yousafzai.
                        All Rights Reserved.

                    </p>

                </div>

            </div>

        </footer>

        <!-- ======================================
                SCROLL TO TOP BUTTON
        ======================================= -->

        <button class="scroll-top" id="scrollTop">

            <i class="fa-solid fa-arrow-up"></i>

        </button>

    </div>

    <!-- ==========================
         JAVASCRIPT
    =========================== -->

    <script src="script.js"></script>

</body>

</html>

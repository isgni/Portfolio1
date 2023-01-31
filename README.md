# Portfolio1
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet" />
    <link rel="preconnect" href="https://fonts.gstatic.com" />

    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css"
      integrity="sha512-iBBXm8fW90+nuLcSKlbmrPcLa0OT92xO1BIsZ+ywDWZCvqsWgccV3gFoRBv0z+8dLJgyAHIhR35VZc2oM/gI1w=="
      crossorigin="anonymous"
    />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins:wght@300&display=swap"
      rel="stylesheet"
    />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <title>Document</title>
  </head>

  <body>
  <i class="fa fa-arrow-up" aria-hidden="true" onclick = "scrollToTop();"></i>
    <section class="sec1" id="section1">
      <div class="menuBar">
        <ul>
          <li><a href="#section1">Home</a></li>
          <li><a href="#section2">About</a></li>
          <li><a href="#section3">Skill</a></li>
          <li><a href="#section4"></a>contact</a></li>
        </ul>
      </div>
      <style>
      
      * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
      
      }
      
      html {
      font-size: 62.5%;
      scroll-behavior: smooth;
      }
      .fa{
      display:flex;
      justify-content:center;
      align-items:center;
      position:fixed;
      bottom:700px;
      right:40px;
      height:50px;
      width:50px;
      background:rgb(226, 69, 69);
      border-radius:50%;
      color:#fff;
      box-shadow:0px 0px 10px rgba(0,0,0,.5);
      background-position:center;
      background-repeat:no-repeat;
      visibility:hidden;
      opacity:0;
      /*cursor:pointer;*/
      transition:.3s;
      z-index:10000;
      
      
      }
      .fa.active{
      visibility:visible;
      opacity:1;
      bottom:40px;
      }
      
      .sec1 {
      position: relative;
      min-height: 100vh;
      width: 100%;
      background: #fff;
      display: flex;
      justify-content: center;
      align-items: flex-end;
      overflow: hidden;
      border-bottom: .1rem solid #ccc;
      
      }
      
      .menuBar {
      position: fixed;
      top: 0;
      left: 120%;
      height: 100%;
      width: 80%;
      /* background: red; */
      z-index: 2000;
      display: flex;
      align-items: center;
      justify-content: center;
      backdrop-filter: blur(10px);
      box-shadow: 0 0 5rem rgba(0, 0, 0, .5);
      transition: .5s;
      }
      
      .menuBar.active {
      left: 20%;
      }
      
      .menuBar ul {
      list-style-type: none;
      }
      
      .menuBar ul li {
      margin: 5rem 0;
      }
      
      .menuBar ul li a {
      position: relative;
      text-decoration: none;
      color: #fff;
      font-size: 2rem;
      padding: 1.5rem;
      transition: .5s;
      background: #e66060;
      padding: 1rem 3rem;
      border-radius: 3rem;
      box-shadow: 0 0 1rem rgba(0, 0, 0, .5);
      
      }
      
      
      .menuBar ul li a:hover {
      color: #e66060;
      background: #fff;
      }
      
      .navBar {
      display: flex;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background: #fff;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2rem;
      box-shadow: 0 0 .5rem rgba(0, 0, 0, .2);
      z-index: 2000;
      }
      
      .sec1__menuIcon {
      display: none;
      position: relative;
      height: 3rem;
      width: 3rem;
      background: url('IMG_20230131_162614 (1).png');
      background-size: contain;
      background-repeat: no-repeat;
      cursor: pointer;
      transition: .5s;
      }
      
      .sec1__menuIcon.active {
      background: url('IMG_20230131_162614 (1).png');
      background-repeat: no-repeat;
      background-position: center;
      background-size: contain;
      }
      
      .navBar .logo h1 {
      color: #333;
      font-size: 2rem;
      letter-spacing: .2rem;
      }
      
      .navBar .navBar__menu ul {
      display: flex;
      list-style-type: none;
      }
      
      .navBar .navBar__menu ul li {
      margin: 1.5rem;
      }
      
      .navBar .navBar__menu ul li a {
      position: relative;
      text-decoration: none;
      font-weight: 500;
      font-size: 1.5rem;
      padding-bottom: 1rem;
      color: #333;
      transition: .3s;
      }
      
      .navBar .navBar__menu ul li a:before {
      background: rgb(236, 78, 78);
      position: absolute;
      content: "";
      bottom: 0;
      left: 0;
      height: .4rem;
      width: 0%;
      border-radius: 1rem;
      transition: .4s;
      }
      
      .navBar .navBar__menu ul li a:hover:before {
      width: 100%;
      }
      
      .navBar .navBar__menu ul li a:hover {
      color: rgb(226, 86, 86);
      }
      
      .sec1__container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      margin-top: 10rem;
      /* background: blue; */
      width: 100%;
      padding: 0 5rem;
      }
      
      .sec1__content .sec1__contentDetail h1 {
      font-weight: 900;
      font-size: 5rem;
      text-transform: capitalize;
      transform: translateY(7rem);
      }
      
      .sec1__contentHider {
      overflow: hidden;
      }
      
      .sec1__content .sec1__contentDetail h1 span {
      color: rgb(236, 75, 75);
      }
      
      .sec1__content .sec1__contentDetail {
      margin-bottom: 3rem;
      }
      
      .sec1__content a {
      background: rgb(226, 69, 69);
      color: #fff;
      text-decoration: none;
      padding: 1rem 2.5rem;
      font-size: 1.5rem;
      border-radius: 1rem;
      transition: .4s;
      }
      
      .sec1__content a:hover {
      background: rgb(216, 43, 43);
      }
      
      .sec1__imgContainer {
      position: relative;
      }
      
      .sec1__imgBx {
      position: relative;
      width: 50rem;
      /* background: red; */
      }
      
      .sec1__design3 {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      border-radius: 50%;
      background: linear-gradient(rgb(255, 107, 107), rgb(184, 27, 27));
      }
      
      .sec1__design4 {
      content: "";
      position: absolute;
      top: 40%;
      left: -10%;
      height: 40%;
      width: 40%;
      border-radius: 30% 50%;
      box-shadow: 0 0 2rem rgba(0, 0, 0, .2);
      background: linear-gradient(rgb(245, 93, 93), rgb(255, 122, 122));
      animation: animate3 ease-in-out 3s infinite;
      }
      
      @keyframes animate3 {
      0% {
      transform: translateY(-3rem);
      }
      
      50% {
      transform: translateY(0rem);
      }
      
      100% {
      transform: translateY(-3rem);
      }
      }
      
      .sec1__imgBx img {
      position: relative;
      z-index: 1;
      width: 100%;
      object-fit: cover;
      filter: drop-shadow(0 0 .5rem rgba(0, 0, 0, .5));
      }
      
      .sec1__imgBx .sec1__design1 {
      position: absolute;
      top: 0;
      left: 0;
      height: 10rem;
      width: 10rem;
      background: linear-gradient(rgb(255, 107, 107), rgb(184, 27, 27));
      border-radius: 5rem 10rem 10rem 4rem;
      filter: blur(6px);
      animation: animate 3s ease-in-out infinite;
      z-index: 1000;
      }
      
      @keyframes animate {
      0% {
      transform: translateX(0rem);
      }
      
      50% {
      transform: translateX(2rem);
      }
      
      100% {
      transform: translateX(0rem);
      }
      }
      
      .sec1__imgBx .sec1__design2 {
      position: absolute;
      bottom: 2rem;
      right: 0;
      height: 10rem;
      width: 10rem;
      background: linear-gradient(rgb(255, 107, 107), rgb(184, 27, 27));
      border-radius: 2rem;
      filter: blur(2px);
      animation: animate2 ease-in-out 5s infinite;
      z-index: 1000;
      }
      
      @keyframes animate2 {
      0% {
      transform: translateY(0rem) rotateZ(0deg);
      }
      
      50% {
      transform: translateY(-2rem) rotateZ(360deg);
      }
      
      100% {
      transform: translateY(0rem) rotateZ(0deg);
      }
      }
      
      .sec2 {
      position: relative;
      min-height: 100vh;
      width: 100%;
      display: flex;
      overflow: hidden;
      flex-direction: column;
      align-items: center;
      justify-content: space-evenly;
      border-bottom: .2rem solid rgb(218, 218, 218);
      }
      
      .sec2__heading {
      overflow: hidden;
      }
      
      .sec2__heading h2 {
      position: relative;
      font-size: 5rem;
      color: #333;
      text-transform: capitalize;
      }
      
      .sec2__heading h2:before {
      content: "";
      position: absolute;
      bottom: 0;
      right: 0;
      height: .2rem;
      width: 100%;
      background-color: rgb(241, 102, 102);
      }
      
      .sec2__container {
      position: relative;
      display: flex;
      justify-content: space-evenly;
      align-items: center;
      width: 100%;
      flex-wrap: wrap;
      
      padding: 0 5rem;
      }
      
      .sec2__aboutme1 {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      flex: .5;
      }
      
      .sec2__aboutme1Img {
      position: relative;
      width: 10rem;
      overflow: hidden;
      border: .3rem solid rgb(156, 60, 60);
      padding: .3rem;
      border-radius: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
      transition: .3s;
      }
      
      .sec2__aboutme1Img:hover {
      transform: scale(1.1);
      }
      
      .sec2__aboutme1Img img {
      width: 100%;
      object-fit: cover;
      background: linear-gradient(rgb(255, 121, 121), rgb(146, 33, 33));
      border-radius: 50%;
      }
      
      .sec2__aboutme1 h2 {
      position: relative;
      font-size: 2rem;
      color: #333;
      padding-bottom: 1rem;
      
      }
      
      .sec2__aboutme1 h2:before {
      position: absolute;
      height: .2rem;
      width: 60%;
      bottom: 0;
      right: 25%;
      content: "";
      background: #ccc;
      }
      
      .sec2__aboutme1Social ul {
      display: flex;
      justify-content: space-evenly;
      align-items: center;
      margin-top: 1rem;
      list-style-type: none;
      }
      
      .sec2__aboutme1Social ul li {
      margin: 0 2rem;
      transition: .3s;
      
      }
      
      .sec2__aboutme1Social ul li a {
      text-decoration: none;
      color: #333;
      font-size: 3rem;
      transition: .3s;
      }
      
      .sec2__aboutme1Social ul li:hover {
      transform: translateY(-.3rem);
      }
      
      .sec2__aboutme1Social ul li:nth-child(1) a:hover {
      color: rgb(235, 108, 108);
      }
      
      .sec2__aboutme1Social ul li:nth-child(2) a:hover {
      color: rgb(0, 0, 0);
      }
      
      .sec2__aboutme1Social ul li:nth-child(3) a:hover {
      color: rgb(85, 109, 219);
      
      }
      
      .sec2__aboutme2 {
      position: relative;
      flex: .5;
      display: flex;
      justify-content: center;
      align-items: center;
      }
      
      .sec2__aboutme2 p {
      font-size: 1.5rem;
      }
      
      .sec3 {
      position: relative;
      min-height: 100vh;
      overflow: hidden;
      width: 100%;
      background: radial-gradient(#333, #000);
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: space-evenly;
      }
      
      .sec3 h1 {
      position: relative;
      color: #fff;
      font-size: 5rem;
      border-bottom: .2rem solid rgb(235, 102, 102);
      }
      
      .sec3__container {
      position: relative;
      display: flex;
      align-items: center;
      justify-content: space-evenly;
      width: 100%;
      flex-wrap: wrap;
      }
      
      .sec3__box .sec3__percent svg {
      position: relative;
      width: 15rem;
      height: 15rem;
      z-index: 1000;
      }
      
      .sec3__box .sec3__percent svg circle {
      width: 100%;
      height: 100%;
      fill: none;
      stroke: #191919;
      stroke-width: 10;
      stroke-linecap: round;
      transform: translate(.5rem, .5rem);
      }
      
      .sec3__percent svg circle:nth-child(2) {
      stroke-dasharray: 440;
      stroke-dashoffset: 440;
      }
      
      .sec3__card:nth-child(1) .sec3__box .sec3__percent svg circle:nth-child(2) {
      stroke: #00ff43;
      stroke-dashoffset: calc(440 - (440*75)/100);
      }
      
      .sec3__card:nth-child(2) .sec3__box .sec3__percent svg circle:nth-child(2) {
      stroke: #e66060;
      stroke-dashoffset: calc(440 - (440*70)/100);
      }
      
      .sec3__card:nth-child(3) .sec3__box .sec3__percent svg circle:nth-child(2) {
      stroke: #6074e6;
      stroke-dashoffset: calc(440 - (440*55)/100);
      }
      
      .sec3__card {
      position: relative;
      background: #000;
      padding: 5rem;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      transition: .3s;
      box-shadow: 0 0 3rem rgba(0, 0, 0, .9);
      margin: 2rem;
      }
      
      .sec3__card .sec3__box {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      }
      
      .sec3__card:before {
      content: "";
      position: absolute;
      height: 100%;
      width: 50%;
      top: 0;
      left: 0;
      background: rgba(225, 225, 225, .05);
      z-index: 1;
      transition: .3s;
      }
      
      .sec3__card:hover:before {
      transform: translateX(50%);
      width: 90%;
      }
      
      .sec3__percent {
      position: relative;
      width: 15rem;
      height: 15rem;
      border-radius: 50%;
      z-index: 1;
      box-shadow: 0 0 2rem #000;
      }
      
      .sec3__percent .number {
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      border-radius: 50%;
      z-index: 1000;
      }
      
      .number h2 {
      color: rgba(255, 255, 255, .5);
      font-size: 4rem;
      font-weight: 900;
      transition: .3s;
      }
      
      .number h2 span {
      font-size: 2rem;
      transition: .3s;
      }
      
      .sec3__card:hover .number h2 span {
      font-size: 1.5rem;
      color: #fff;
      }
      
      .sec3__text {
      color: rgba(255, 255, 255, .5);
      margin-top: 2.5rem;
      transition: .3s;
      }
      
      .sec3__card:hover .sec3__text {
      color: #fff;
      }
      
      .sec3__card:hover .number h2 {
      color: #fff;
      transform: scale(1.2);
      }
      
      .sec3__card:hover {
      transform: translateY(-1rem);
      }
      
      .sec4 {
      overflow: hidden;
      position: relative;
      min-height: 70vh;
      width: 100%;
      background: radial-gradient(#333, #000);
      display: flex;
      align-items: center;
      justify-content: center;
      }
      
      .sec4__container {
      position: relative;
      width: 100%;
      display: flex;
      justify-content: space-evenly;
      align-items: flex-start;
      padding: 2rem;
      flex-wrap: wrap;
      }
      
      .sec4__box1 {
      display: flex;
      justify-content: space-evenly;
      align-items: flex-start;
      flex-direction: column;
      flex: .5;
      }
      
      .sec4__content1 {
      margin-bottom: 1rem;
      }
      
      .sec4__content1 h2 {
      color: #fff;
      font-size: 3rem;
      border-bottom: .2rem solid #ff7b7b;
      width: fit-content;
      padding-bottom: .5rem;
      margin-bottom: .5rem;
      }
      
      
      .sec4__content1 h2 span {
      color: #ff6060;
      }
      
      .sec4__content1 p {
      color: #fff;
      }
      
      .sec4__content2Icon {
      display: flex;
      justify-content: center;
      align-items: center;
      color: #fff;
      }
      
      .sec4__content2Icon h2 {
      margin-left: .5rem;
      }
      
      .sec4__content2 {
      margin: .5rem 0;
      }
      
      .sec4__content3 ul {
      display: flex;
      justify-content: space-evenly;
      align-items: flex-start;
      list-style-type: none;
      margin-top: 1rem;
      }
      
      .sec4__content3 ul li {
      margin: 0 1.5rem 0 0;
      }
      
      .sec4__content3 ul li a {
      color: #fff;
      font-size: 2rem;
      border: .2rem solid #fff;
      padding: .4rem;
      border-radius: 20%;
      transition: .3s;
      }
      
      .sec4__content3 ul li a:hover {
      color: rgba(255, 255, 255, .5);
      }
      
      .sec4__box2 h2 {
      color: #fff;
      font-size: 3rem;
      border-bottom: .2rem solid #ff8282;
      padding-bottom: .5rem;
      margin-bottom: .5rem;
      }
      
      .sec4__links ul {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      list-style-type: none;
      }
      
      .sec4__links ul li {
      margin: .5rem 0;
      }
      
      .sec4__links ul li a {
      color: rgba(255, 255, 255, .5);
      transition: .3s;
      text-decoration: none;
      font-size: 1.5rem;
      }
      
      .sec4__links ul li a:hover {
      color: #fff;
      }
      
      .sec4__box3 h2 {
      color: #fff;
      font-size: 3rem;
      border-bottom: .2rem solid #ff7d7d;
      padding-bottom: .5rem;
      margin-bottom: .5rem;
      width: fit-content;
      }
      
      .sec4__box3 form {
      display: flex;
      flex-direction: column;
      justify-content: space-evenly;
      align-items: center;
      }
      
      .sec4__box3 form input {
      border: none;
      outline: none;
      background: #fff;
      box-shadow: 0 0 2rem rgba(0, 0, 0, .5);
      padding: .5rem 1rem;
      margin: 1rem 0;
      width: 100%;
      border-radius: 3rem;
      }
      
      .sec4__box3 form input::placeholder {
      color: #333;
      font-size: 1.1rem;
      }
      
      .sec4__box3 form button {
      border: none;
      background: none;
      outline: none;
      padding: .5rem 2rem;
      color: #fff;
      background: #e66060;
      cursor: pointer;
      transition: .3s;
      border-radius: 3rem;
      
      }
      
      .sec4__box3 form button:hover {
      color: #ff6060;
      background: #fff;
      }
      
      /* media query start here  */
      @media(max-width:360px) {
      .sec1__menuIcon {
      display: inline-block;
      }
      
      .sec1__container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      margin-top: 10rem;
      /* background: blue; */
      width: 100%;
      padding: 0 2rem;
      }
      
      .navBar__menu {
      display: none;
      }
      
      .sec1__content .sec1__contentDetail h1 {
      font-weight: 900;
      font-size: 3.5rem;
      text-transform: capitalize;
      transform: translateY(7rem);
      }
      
      .sec1__imgBx {
      position: relative;
      width: 30rem;
      /* background: red; */
      margin-top: 5rem;
      }
      
      .sec2__container {
      position: relative;
      display: flex;
      justify-content: space-evenly;
      align-items: center;
      width: 100%;
      flex-wrap: wrap;
      padding: 0 2rem;
      flex-direction: column;
      }
      
      .sec2__heading h2 {
      position: relative;
      font-size: 2.5rem;
      color: #333;
      text-transform: capitalize;
      }
      
      .sec2__aboutme1 {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      flex: .5;
      margin: 5rem 0;
      }
      
      .sec2__aboutme2 {
      position: relative;
      flex: 1;
      display: flex;
      justify-content: center;
      align-items: center;
      margin: 0 0 3rem 0;
      }
      
      .sec4__box1 {
      display: flex;
      justify-content: space-evenly;
      align-items: flex-start;
      flex-direction: column;
      flex: .5;
      margin: 2.5rem 0 4rem 0;
      }
      
      .sec4__box2 {
      margin: 2.5rem 0;
      }
      }
      </style>
      
      
      
      <div class="navBar">
        <div class="logo">
          <h1>Art</h1>
        </div>
        <div class="navBar__menu">
          <ul>
            <li>
              <a href="#section1">Home</a>
            </li>
            <li>
              <a href="#section2">About</a>
            </li>
            <li>
              <a href="#section3">Skill</a>
            </li>
            <li>
              <a href="#section4">Contact</a>
            </li>
          </ul>
        </div>
        <div class="sec1__menuIcon"></div>
      </div>
      <div class="sec1__container">
        <div class="sec1__content">
          <div class="sec1__contentDetail">
            <div class="sec1__contentHider">
              <h1>hi,</h1>
            </div>
            <div class="sec1__contentHider">
              <h1>I'am <span>Art Pimentel</span></h1>
            </div>
            <div class="sec1__contentHider">
              <h1>Web Designer</h1>
            </div>
          </div>
          <a href="https://www.instagram.com/vivek_kumar_mahali/">follow Me <i class="fab fa-instagram"></i></a>
        </div>
        <div class="sec1__imgContainer">
          <div class="sec1__imgBx">
            <img src="Screenshot_2023_0131_185733.jpg"  alt="" />
            <span class="sec1__design1"></span>
            <span class="sec1__design2"></span>
            <span class="sec1__design3"></span>
            <span class="sec1__design4"></span>
          </div>
        </div>
      </div>
    </section>
    <section class="sec2" id="section2">
      <div class="sec2__heading">
        <h2>about me</h2>
      </div>
      <div class="sec2__container">
        <div class="sec2__aboutme1" data-aos="fade-up" data-aos-offset="-90">
          <div class="sec2__aboutme1Img">
            <img src="IMG_20230131_162614 (1).png" alt="" />
          </div>
          <h2>Art Pimentel</h2>
          <div class="sec2__aboutme1Social">
            <ul>
              <li>
                <a href="https://www.instagram.com/vivek_kumar_mahali/"><i class="fab fa-instagram"></i></a>
              </li>
              <li>
                <a href="#"><i class="fab fa-google"></i></a>
              </li>
              <li>
                <a href="https://m.facebook.com/profile.php"><i class="fab fa-facebook"></i></a>
              </li>
            </ul>
          </div>
        </div>
        <div class="sec2__aboutme2" data-aos="fade-up" data-aos-delay="1000">
          <p>
            Frotend Developer
A junior developer also a student, studying at Capiz State University Mambusao Sattelite Campus taking course of Bachelor of Science in Computer Science
          </p>
        </div>
      </div>
    </section>
    <section class="sec3" id="section3">
      <h1>skills</h1>
      <div class="sec3__container">
        <div class="sec3__card" data-aos="fade-up">
          <div class="sec3__box">
            <div class="sec3__percent">
              <svg>
                <circle cx="70" cy="70" r="70"></circle>
                <circle cx="70" cy="70" r="70"></circle>
              </svg>
              <div class="number">
                <h2>75<span>%</span></h2>
              </div>
            </div>
            <h2 class="sec3__text">HTML</h2>
          </div>
        </div>
        <div class="sec3__card" data-aos="fade-up" data-aos-delay="500">
          <div class="sec3__box">
            <div class="sec3__percent">
              <svg>
                <circle cx="70" cy="70" r="70"></circle>
                <circle cx="70" cy="70" r="70"></circle>
              </svg>
              <div class="number">
                <h2>70<span>%</span></h2>
              </div>
            </div>
            <h2 class="sec3__text">CSS</h2>
          </div>
        </div>
        <div class="sec3__card" data-aos="fade-up" data-aos-delay="1000">
          <div class="sec3__box">
            <div class="sec3__percent">
              <svg>
                <circle cx="70" cy="70" r="70"></circle>
                <circle cx="70" cy="70" r="70"></circle>
              </svg>
              <div class="number">
                <h2>55<span>%</span></h2>
              </div>
            </div>
            <h2 class="sec3__text">JAVASCRIPT</h2>
          </div>
        </div>
      </div>
    </section>
    <section class="sec4" id="section4">
      <div class="sec4__container">
        <div class="sec4__box1">
          <div class="sec4__content1" data-aos="fade-right">
            <h2>A<span>R</span>T @isgni</h2>
            <p>
           Maybe you're still confused on what it is that
           you want to pursue. Maybe you don't even have
           any idea where to start. Maybe you don't know
            what your path in life is yet. Maybe you're still
           struggling with your studies. Maybe you're still 
            confused on what it is that you want to pursue. 
            Maybe you don't even have any idea where to start. 
           
           You will figure it out. You will figure everything out. 
           You're still alive. There's still hope. I believe in you.
            </p>
          </div>
          <div
            class="sec4__content2"
            data-aos="fade-right"
            data-aos-delay="200"
          >
            <div class="sec4__content2Icon">
              <i class="fas fa-phone-alt"></i>
              <h2>09099681335</h2>
            </div>
            <div class="sec4__content2Icon">
              <i class="fas fa-envelope"></i>
              <h2>artpimentel@gmail.com</h2>
            </div>
          </div>
          <div
            class="sec4__content3"
            data-aos="fade-right"
            data-aos-delay="500"
          >
            <ul>
              <li>
                <a href="https://www.instagram.com/vivek_kumar_mahali/"><i class="fab fa-instagram"></i></a>
              </li>
              <li>
                <a href="#"><i class="fab fa-google"></i></a>
              </li>
              <li>
                <a href="#"><i class="fab fa-facebook"></i></a>
              </li>
              <li>
                <a href="#"><i class="fab fa-linkedin"></i></a>
              </li>
              <li>
                <a href="#"><i class="fab fa-github"></i></a>
              </li>
            </ul>
          </div>
        </div>
        <div class="sec4__box2" data-aos="fade-in" data-aos-delay="500">
          <h2>Quick links</h2>
          <div class="sec4__links">
            <ul>
              <li><a href="#">Home</a></li>
              <li><a href="#">About</a></li>
              <li><a href="#">Skill</a></li>
            </ul>
          </div>
        </div>
        <div class="sec4__box3">
          <h2>Contact Us</h2>
          <form>
            <input
              data-aos="fade-left"
              data-aos-delay="500"
              class="sec4__email"
              type="email"
              placeholder="Enter your Email"
            />
            <input
              class="sec4__message"
              data-aos="fade-left"
              data-aos-delay="1000"
              type="text"
              placeholder="enter the feedback or suggestion"
            />
            <button type="submit">send</button>
          </form>
        </div>
      </div>
    </section>
    
    
    
    
    
    
    
    
    <script
      src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.6.1/gsap.min.js"
      integrity="sha512-cdV6j5t5o24hkSciVrb8Ki6FveC2SgwGfLE31+ZQRHAeSRxYhAQskLkq3dLm8ZcWe1N3vBOEYmmbhzf7NTtFFQ=="
      crossorigin="anonymous"
    ></script>
    <script>
      const tl = gsap.timeline({ defaults: { ease: "power1.out" } });

      tl.from(".navBar", { y: "-10rem", duration: 1 });
      tl.from(".navBar .navBar__menu ul li", {
        y: "-2rem",
        opacity: 0,
        duration: 1,
        stagger: 0.25,
      });
      tl.to(
        ".sec1__content .sec1__contentDetail h1",
        { y: "0rem", duration: 1, stagger: 0.25 },
        "=-1"
      );
      tl.from(".sec1__imgBx img", { opacity: 0, x: "50%", duration: 1.5 });
      tl.from(
        ".sec1__imgBx .sec1__design1",
        { opacity: 0, x: "3rem", duration: 1.5 },
        "=-1"
      );
      tl.from(
        ".sec1__imgBx .sec1__design2",
        { opacity: 0, x: "-3rem", duration: 1.5 },
        "=-1"
      );
      tl.from(
        ".sec1__design3",
        { opacity: 0, x: "-30%", duration: 1.5 },
        "=-2"
      );
      tl.from(".sec1__design4", { opacity: 0, duration: 1.5 }, "=-2");
      tl.from(".sec1__content a", { opacity: 0, duration: 1.5 }, "=-3");
    </script>
    <!-- our AOs will occur here -->
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
      AOS.init({
        duration: 1000,
        offset:0,
      });
    </script>
    <script>
      var sec1__menuIcon = document.querySelector(".sec1__menuIcon");
      var menuBar = document.querySelector(".menuBar");
      sec1__menuIcon.addEventListener("click", function () {
        sec1__menuIcon.classList.toggle("active");
        menuBar.classList.toggle("active");
      });
    </script>
    <script type = "text/javascript">
        window.addEventListener('scroll',function(){
            var scroll = document.querySelector('.fa');
            scroll.classList.toggle("active",window.scrollY>500)
        })
        function scrollToTop(){
            window.scrollTo({
                top:0,
                behavior:'smooth'
            })
        }
    </script>
  </body>
</html>

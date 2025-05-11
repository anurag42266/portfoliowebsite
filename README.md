
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Portfolio Website</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css" integrity="sha512-Evv84Mr4kqVGRNSgIGL/F/aIDqQb7xQ2vcrdIwxfjThSH8CSR7PBEakCr51Ck+w+/U6swU2Im1vVX0SVk9ABhg==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <link rel="stylesheet" href="style.css">
    <style>
      *{
    margin: 0;
    padding: 0;
    font-family: 'poppins', sans-serif;
    box-sizing: border-box;
}
html{
    scroll-behavior: smooth;
}
body{
    background-color: #080808;
    color: #fff;
}
#header{
    width: 100%;
    height: 100vh;
    background-image: url(bganurag2.jpg);
    background-size: cover;
    background-position: center;
}
.container{
    padding: 10px 10%;
}
nav{
    display:flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
}
.logo{
    width: 140px;

}
nav ul li{
    display: inline-block;
    list-style: none;
    margin: 10px 20px;
}
nav ul li a{
    color: #fff;
    text-decoration: none;
    font-size: 18px;
    position: relative;
}
nav ul li a::after{
    content: ' ';
    width: 0;
    height: 3px;
    background: #ff004f;
    position: absolute;
    left:0;
    bottom: -6px;
    transition: 0.5s;
}
nav ul li a:hover::after{
    width: 100%; 
}
.header-text{
     margin-top: 20%;
     font-size: 30px; 
}
.header-text h1{
     font-size: 60px;
     margin-top: 20px;
}
.header-text h1 span{
    color:#ff004f ;
}
/* about */
#about{
    padding: 80px 0;
    color: #ababab; 
}
.row{
    display: flex;
    justify-content:space-between ;
    flex-wrap: wrap;
}
.about-col-1{
    flex-basis: 35%;

}
.about-col-1 img{
    width:100%;
    border-radius: 15px;
}
.about-col-2{
    flex-basis: 60%;
}
.sub-title{
    font-size: 60px;
    font-weight: 600;
    color: #fff;
}
.tab-titles{
    display: flex;
    margin: 20px 0 40px;
}
.tab-links{
    margin-right: 50px;
    font-size: 18px;
    font-weight: 500;
    cursor: pointer;
    position: relative;
}
.tab-links::after{
    content: ' ';
    width: 0;
    height: 3px;
    background: #ff004f;
    position: absolute;
    left: 0;
    bottom: -8px;
    transition: 0.5s;
}
.tab-links.active-link::after{
    width: 50%;
}
.tab-contents ul li{
    list-style: none;
    margin: 10px 0;
}
.tab-contents ul li span{
 color: #b54769;
 font-size: 14px;
}
.tab-contents{
    display: none;
}
.tab-contents.active-tab{
    display: block;
}
/*  services */
#services{
    padding: 30px 0;

}
.serviceslist{
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
    grid-gap: 40px;
    margin-top: 50px;
}
.serviceslist div{
    background: #262626;
    padding: 40px;
    font-size: 13px;
    font-weight: 300;
    border-radius: 10px; 
    transition: background 0.5s, transform 0.5s ;
}
.serviceslist div i{
    font-size: 50px;
    margin-bottom: 30px;
}
.serviceslist div h2{
    font-size: 30px;
    font-weight: 500;
    margin-bottom: 15px;
}
.serviceslist div a{
    text-decoration: none;
    color: #fff;
    font-size: 12px;
    margin-top:20px;
    display: inline-block;
}
.serviceslist div:hover{
    background:#ff004f;
    transform: translateY(-10px);
}
/* -----portfolio---- */
#portfolio{
    padding: 50px 0 ;
}
.work-list{
    display: grid;
    grid-template-columns: repeat(auto-fit,minmax(250px,1fr));
    grid-gap: 40px;
    margin-top: 50px;
}
.work{
    border-radius: 10px;
    position: relative;
    overflow: hidden;
}
.work img{
    width: 100%;
    border-radius:10px;
    transition: transform 0.5s;
}
.layer{
    width: 100%;
    height: 0;
    background:linear-gradient(rgba(0,0,0,0.6),#ff004f) ;
    border-radius: 10px;
    position: absolute;
    left: 0;
    bottom: 0;
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction:column ;
    padding:0 40px ;
    text-align: center;
    font-size: 14px;
    transition: height 0.5s;
}
.layer h3{
    font-weight: 500;
    margin-bottom: 20px;
}
.layer a{
    margin-top: 20px;
    color: #ff004f;
    text-decoration: none;
    font-size: 18px;
    line-height: 60px;
    background-color: #fff;
    width: 60px;
    height: 60px;
    border-radius: 50%;
    text-align: center;
}
.work:hover img{
  transform: scale(1.1);
}
.work:hover .layer{
    height: 100%;
}
.btn{
    display: block;
    margin: 50px auto;
    width: fit-content;
    border: 1px solid #ff004f;
    padding: 14px 50px;
    border-radius: 6px;
    text-decoration: none;
    color: white;
    transition: background 0.5s;
}
.btn:hover{
    background: #ff004f;
    
}
/* contact */
.contact-left{
    flex-basis: 35%;
}
.contact-right{
    flex-basis: 60%;
}
.contact-left p{
    margin-top: 30px;
}
.contact-left p i{
    color: #ff004f;
    margin-right: 15px; 
    font-size: 25px;
}
.social-icon{
    margin-top: 30px;

}
.social-icon a{
    text-decoration: none;
    font-size:30px ;
    margin-right: 15px;
    color: #ababab ;
    display: inline-block;
    transition: transform 0.5s;
}
.social-icon a :hover{
    color: #ff004f;
    transform: translateY(-5px);
}
.btn.btn2{
    display: inline-block;
    background-color: #ff004f;

}
.contact-right form{
      width: 100%;
}
form input, form textarea{
    width: 100%;
    border: 0;
    outline: none;
    background: #262626;
    padding: 15px;
    margin: 15px 0;
    color: #fff;
    font-size: 18px;
    border-radius: 15px;
}
form .btn2{
    padding: 15px 60px;
    font-size: 18px;
    margin-top: 20px;
    cursor: pointer;

}
.copyright{
    width: 100%;
    text-align: center;
    padding: 25px 0;
    background: #262626;
    font-weight: 300;
    margin-top: 20px;
}
.copyright i{
    color: #ff004f;
}
/* css for small screen */
nav .fas{
    display: none;
}
@media only screen and (max-width:700px){
   #header{
    background-image: url(photo1__1_-removebg-preview.png) ;
   } 
   .header-text{
    margin-top:75%;
    font-size: 16px;
   }
   .header-text{
    font-size: 30px;
   }
   nav .fas{
    display: block;
    font-size: 25px;
   }
   nav ul{
    background-color: #262626;
    position: fixed;
    top: 0;
    right: -200px;
    width: 200px ;
    height: 100vh;
    padding-top: 50px;
    z-index: 2;
    transition:right 0.5s ;
   }
   nav ul li{
    display: block;
    margin: 25px;
   }
     nav ul .fas{
        position: absolute;
        top: 25px;
        left: 25px;
        cursor: pointer;
     }
     .sub-title{
        font-size: 40px;
     }
     .about-col-1,.about-col-2{
        flex-basis: 100%;
     }
     .about-col-1{
        margin-bottom:30px ;
     }
     .about-col-2{
        font-size: 14px;
     }
     .tab-links{
        font-size: 16px;
        margin-right:20px;
     }
}
    </style>
</head>
<body>
<div id="header">
    <div class="container">
        <nav>
            <img src="logo.png" class="logo" >
            <ul id="sidemenu">
                <li> <a href="#header">Home</a></li>
                <li> <a href="#about">About</a></li>
                <li> <a href="#services">services</a></li>
                <li> <a href="#portfolio">portfolio</a></li>
                <li> <a href="#contact">Contact</a></li>
                <i class=" fas fa-solid fa-xmark" onclick="closemenu()"></i>
            </ul>
            <i class=" fas fa-solid fa-bars" onclick="openmenu()"></i>
        </nav>
        <div class="header-text">
            <p>UI/UX</p>
            <h1>Hi,I'm <span> Anurag</span><br> kushwaha from India </h1>
        </div>
    </div>
</div> 
<!-- About -->
   <div id="about">
    <div class="container">
       <div class="row">
        <div class="about-col-1">
            <img src="user.png" alt="">
        </div>
         <div class="about-col-2">
            <h1 class="sub-title">About Me</h1>
            <p>We confess that it is our purpose to prepare the German people again for the role of the hammer. We admit freely and openly that if our movement is victorious, we will be concerned day and night with the question of how to produce the armed forces, which are forbidden us by the peace treaty</p>
            <div class="tab-titles">
                <p class="tab-links active-link " onclick="opentab('skills')">Skills</p>
                <p class="tab-links"onclick="opentab('experience')">Experience</p>
                <p class="tab-links"onclick="opentab('education')">Education</p>
            </div>
            <div class="tab-contents active-tab" id="skills">
                <ul>
                <li> <span>UI/UX</span><br>Designing Web/App interfaces</li>
                <li> <span>Web Development</span><br> Web/App Development</li>
                <li><span>App Development</span><br>Building Android/Apps</li>
                </ul>
            </div>
             <!-- experience -->
            <div class="tab-contents" id="experience">
                <ul>
                <li> <span>current</span><br>Studying in the IIIt Sonepat</li>
                <li> <span>2023-2024</span><br> Prepare for Jee</li>
                <li><span>2020-2023</span><br>Did Nothing</li>
                </ul>
            </div>
              <!-- education -->
            <div class="tab-contents" id="education">
                <ul>
                <li> <span>current</span><br>UPSC Aspirant</li>
                <li> <span>2024-2028</span><br> Btech from IIIT Sonepat</li>
                <li><span>2023</span><br>Completed School</li>
                </ul>
            </div>
         </div>
       </div>
    </div>
   </div>
    <!--     services -->
         <div id="services">
            <div class="container">
                <h1 class="sub-title">My Services</h1>
                <div class="serviceslist">
                   <div>
                    <i class="fa-solid fa-code"></i>
                    <h2>Web Designing</h2>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
                        Ea nobis totam quibusdam facilis odit sint et vero ipsa adipisci eveniet quod, 
                        nulla tenetur in exercitationem ullam quos. Itaque, voluptas placeat?</p>
                        <a href="#">Learn more</a>
                   </div> 
                   <div>
                    <i class="fa-solid fa-crop"></i>
                    <h2>UI/UX</h2>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
                        Ea nobis totam quibusdam facilis odit sint et vero ipsa adipisci eveniet quod, 
                        nulla tenetur in exercitationem ullam quos. Itaque, voluptas placeat?</p>
                        <a href="#">Learn more</a>
                   </div>
                   <div>
                    <i class="fa-brands fa-app-store"></i>
                    <h2>App Design</h2>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
                        Ea nobis totam quibusdam facilis odit sint et vero ipsa adipisci eveniet quod, 
                        nulla tenetur in exercitationem ullam quos. Itaque, voluptas placeat?</p>
                        <a href="#">Learn more</a>
                   </div>
                   
                </div>
            </div>
         </div>

<!-- portfolio -->
  <div id="portfolio">
      <div class="container">
        <h1 class="sub-title">My Work</h1>
        <div class="work-list">
                <div class="work">
                    <img src="work-1.png" alt="no-image">
                    <div class="layer">
                        <h3>Social Media App</h3>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias dignissimos voluptatibus, commodi  
                            magni atque. Reprehenderit dolorem unde minus ipsam?</p>
                        <a href="#"><i class="fa-solid fa-arrow-up-right-from-square"></i></a>
                    </div>
                    </div>
                <div class="work">
                    <img src="work-2.png" alt="no-image">
                    <div class="layer">
                        <h3>music App</h3>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias dignissimos voluptatibus, commodi 
                            magni atque. Reprehenderit dolorem unde minus ipsam?</p>
                        <a href="#"><i class="fa-solid fa-arrow-up-right-from-square"></i></a>
                    </div>
                   </div>
                   <div class="work">
                    <img src="work-3.png" alt="no-image">
                    <div class="layer">
                        <h3>online shopping App</h3>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias dignissimos voluptatibus, commodi 
                            magni atque. Reprehenderit dolorem unde minus ipsam?</p>
                        <a href="#"><i class="fa-solid fa-arrow-up-right-from-square"></i></a>
                    </div>
                   </div>
        </div>
        <a href="#" class="btn">See more</a>
      </div>
  </div>
<!------contact------->
<div id="contact">
      <div class="container">
        <div class="row">
            <div class="contact-left">
                <h1 class="sub-title">Contact me</h1>
                <p><i class="fa-solid fa-paper-plane"></i>contact@example.com</p>
                <p><i class="fa-solid fa-phone"></i>0938171728</p>
                <div class="social-icon">
                    <a href="https://www.facebook.com/"><i class="fa-brands fa-facebook"></i></a>
                    <a href="https://www.instagram.com/"><i class="fa-brands fa-x-twitter"></i></a>
                    <a href="https://www.instagram.com/"><i class="fa-brands fa-instagram"></i></a>
                    <a href="www.linkedin.com/in/anurag-kushwaha-60142a32a"><i class="fa-brands fa-linkedin"></i></a>
                </div>
                <a href="my-cv.pdf"  download  class="btn btn2">Download CV</a>
            </div>
             <div class="contact-right">
                <form action="">
                    <input type="text" name="Name" placeholder="Your Name">
                    <input type="email" name="email" id="email" placeholder="Your Email Required">
                    <textarea name="message" id="" rows="6" placeholder="Your Message"></textarea>
                    <button type="submit" class="btn btn2">Submit</button>
                </form>
             </div>
        </div>
      </div>
      <div class="copyright">
        <p>Copyright @ Anurag kushwaha <i class="fa-solid fa-heart"></i></p>
      </div>
</div>




   <script>
    var tablinks=document.getElementsByClassName("tab-links");
    var tabconents=document.getElementsByClassName("tab-contents");
    function opentab(tabname){
        for(tablink of tablinks){
            tablink.classList.remove("active-link")
        }
        for(tabconent of tabconents){
            tabconent.classList.remove("active-tab")
        }
        event.currentTarget.classList.add("active-link");
        document.getElementById(tabname).classList.add("active-tab")
    }

   </script>
   <script>
    let sidemenu=document.getElementById("sidemenu");
   function openmenu(){
      sidemenu.style.right="0";
   }
   function closemenu(){
      sidemenu.style.right="-200px";
   }
   </script>
</body>
</html>

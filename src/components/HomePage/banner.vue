<template>
    <section>
        <div class="container">
           <div class="banner d-flex justify-content-center align-items-center flex-column gap-3 ">
                <div class="hello">
                    <span class="top-svg">
                        <img src="../../assets/images/hello-1.svg" alt="hello svg" >
                    </span>

                    <p class="text-capitalize"> hello!</p>

                    <span class="bottom-svg">
                        <img src="../../assets/images/hello-1.svg" alt="hello svg" >
                    </span>
                </div>
                
                <div>
                    <h1>
                        I’m <span>Nourhan</span>, <br/> UX UI Designer
                    </h1>
                </div>

                <div class="main-img position-relative">
                    <span class="group-9">
                        <img src="../../assets/images/Group9.png" >
                    </span>

                    <span class="group-7">
                        <img src="../../assets/images/Group7.png" >
                    </span>

                    <span class="group-6">
                        <img src="../../assets/images/Group6.png" >
                    </span>

                    <span class="group-5">
                        <img src="../../assets/images/Group5.png" >
                    </span>

                    <span class="group-4">
                        <img src="../../assets/images/Group4.png" >
                    </span>

                    <span class="group-2">
                        <img src="../../assets/images/Group-2.png" >
                    </span>

                    <span class="group-3">
                        <img src="../../assets/images/Group3.png" >
                    </span>

                    <span class="group-14">
                        <img src="../../assets/images/Group4.png" >
                    </span>

                    <span class="group-10">
                        <img src="../../assets/images/Group10.png" >
                    </span>

                    <span class="group-15">
                        <img src="../../assets/images/Group5.png" >
                    </span>

                    <span class="group-11">
                        <img src="../../assets/images/Group11.png" >
                    </span>

                    <span class="group-12">
                        <img src="../../assets/images/Group12.png" >
                    </span>

                    <span class="group-13">
                        <img src="../../assets/images/Group13.png" >
                    </span>

                   <div class="d-flex justify-content-center banner-img-container">
                    <img src="../../assets/images/user-1.png" alt="banner image" class="image-1">
                   </div>
                    <div class="d-flex justify-content-center bottom-container"> 
                        <div class="contact-bottom">
                        <a href="https://www.behance.net/nourhanmahmoud7" target="blank">Porfolio <img src="../../assets/images/up right.png"></a>
                        <a  href="tel:+1234567890">Hire me</a>
                    </div>
                    </div>
                </div>

           </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
.container{
    padding-top: 150px;
}
    h1{
        font-family: "Passero One", serif;
        text-align: center;
        font-size: 55px;
        margin-top: 10px;
        span{
            color:#42307D;
            font-family: inherit
        }
    }

    .hello{
        position: relative;
        p{
            font-family: "Poppins", sans-serif;
            font-size: 20px;
            color: #171717;
            border: 1px solid #171717;
            padding: 6px 32px;
            border-radius: 28px;
            font-weight: 500;
        }
        span{
            position: absolute;
        }
        .top-svg{
            top: -34px;
            right: -26px;
            transform: translate(10px,10px) rotate(180deg);
        }
        .bottom-svg{
            bottom: -7px;
            left: -40px;
            transform: translate(10px,10px);
        }
    }
    .image-1{
        width: 320px;
        height: auto
    }
    .main-img{
        background-image: url('../../assets/images/Ellipse2.png');
        background-repeat: no-repeat;
        background-size: contain;
        background-position: bottom center;
        width: 80%;
        margin:10px auto;
        margin-top: 40px;
        text-align: center;
        flex-shrink: 0;
        .image-1{
            transform: translateY(23px);
        }
    }
    .bottom-container{
        transform: translateY(-21px);
    }
    .contact-bottom{
        background: rgb(255 255 255 / 10%);
        backdrop-filter: blur(10px); /* Apply the blur effect */
        -webkit-backdrop-filter: blur(10px);
        border-radius: 41px;
        padding: 7px;
        width: 339px;
        display: flex;
        justify-content:  center;
        align-items: center;
        gap: 10px;
        border: 1px solid #ddddddc4;

        a{
            display: inline-block;
            font-size: 25px;
            text-decoration: none;
            font-weight: 400;
        }
        a:nth-of-type(1){
            background: #42307D;
            color: #fff;
            border-radius: 32px;
            padding: 7px 40px;
            display: inline-flex;
            justify-content: center;
            align-items: center;
            gap : 10px
        }
        a:nth-of-type(2){
            color: #42307D;
        }
        img{
            width: 20px;
        }
    }
/************************* */
.group-9{
    position: absolute;
    right: 41%;
    top: -10%;
}
.group-7{
    position: absolute;
    right: 25%;
    top: 3%;
}
.group-6{
    position: absolute;
    right: 16%;
    top: 6%;
}
.group-5{
    position: absolute;
    right: 13%;
    top: 37%;
}
.group-15{
    position: absolute;
    left: 21%;
    top: 2%;
}
.group-3{
    position: absolute;
    right: -1%;
    top: 48%;
}
.group-2{
    position: absolute;
    top: 55%;
    right: 17%;
    z-index: 100;
}
.group-8{
    position: absolute;
    right: 35%;
    top: 20%;
}
.group-10{
    position: absolute;
    right: 61%;
    top: -5%;
}
.group-11{
    position: absolute;
    right: 65%;
    top: 16%;
}
.group-12{
    position: absolute;
    left: 0%;
    top: 39%;
}
.group-13{
    position: absolute;
    left: 12%;
    top: 73%;
    z-index: 100;
}
.group-4{
    position: absolute;
    top: 64%;
    right: 12%;
}
.group-14{
    position: absolute;
    top: 42%;
    right: 22%;
}
/*************************** */
    @media screen and (max-width :992.8px) {
        .hello p{
            margin-top: 25px;
        }
        .hello .top-svg {
            top: -11px;
        }

        .group-11,.group-9,.group-3,.group-6,.group-8,.group-13{
            img{
                width: 100px;
            }
        }
        .group-5{
            right: 1%;
            top: 31%;
        }
        .group-4{
            display: none;
        }
        .group-3{
            top: 65%;
            img{
                width:  120px;
            }
        }
        .group-15{
            left: 14%;
        }
        .group-2{
            top: 50%;
            right: 8%;
            img{
                width: 60px;
            }
        }
        .group-12{
            img{
                width: 180px
            }
        }
        .group-13{
            left: 4%;
        }
        .group-10{
            img{
                width: 70px;
            }
        }

        .main-img{
            width: 100%; 
            .image-1{
                transform: translateY(44px);
            }
        }
        .bottom-container{
            transform: translateY(-9px);
            a{
                font-size: 18px;
            }
        }
        .contact-bottom{
            width: 254px;
            a:nth-of-type(1){
                padding: 7px 20px;
            }
        }
    }

    @media screen and (max-width :578px) {
        .image-1{
            width: 164px !important; 
        }
        span{
            img{width: 30px;}
        }
    }
    @media screen and (min-width : 578.8px) and (max-width : 768px){
        .image-1{
            width: 212px;
        }
      
    }
    @media screen and (min-width :768px) and (max-width: 992.8px) {
        .image-1{
            width: 203px;
        }
        .bottom-container {
            transform: translateY(-9px);
        }
    }
</style>
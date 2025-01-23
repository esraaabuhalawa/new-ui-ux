<template>
    <section id="contact">
        <div class="container">
            <div class="social">
                <!---------image start-->
                <div class="d-flex justify-content-center">
                    <div class="user-img">
                        <img src="../../assets/images/footer-img.png" alt="" width="" height="" class="img-fluid">
                    </div>
                </div>
                <!-----image end----------->
                <!------start of social------->
                <div class="social-info ">
                    <div class="text-center designer">
                        <p>Nourhan Mahmoud </p>
                        <p>Senior UX UI Designer</p>
                        <span>Follow us</span>
                    </div>
                    <div class="d-flex justify-content-center align-items-center gap-5 mt-5 mb-5 social-hover">
                        <a target="blank" href="https://www.facebook.com/profile.php?id=61557703628129">
                            <img src="../../assets/images/my profile icon/my profile icon/facebook.svg" alt="facebook account">
                        </a>
                        <a href="">
                            <img src="../../assets/images/my profile icon/my profile icon/instagram.svg" alt="facebook account">
                        </a>
                        <a target="blank" href="https://www.linkedin.com/posts/mahmoz_%D9%80%D9%85%D9%88%D9%82%D8%B9-%D9%85%D9%83%D9%86%D8%AA%D8%B4-%D9%85%D8%B5%D8%AF%D9%82-%D8%A7%D9%86%D9%87-%D9%85%D8%AC%D8%A7%D9%86%D9%8A-%D9%84%D9%88-%D9%86%D9%81%D8%B3%D9%83-%D8%AA%D8%B6%D9%8A%D9%81-ugcPost-7274079433932632064-_n1k?utm_source=share&utm_medium=member_android">
                            <img src="../../assets/images/my profile icon/my profile icon/linkedin.svg" alt="facebook account">

                        </a>
                        <a href="mailto:nourhanmahmoudahmed46@gmail.com">
                            <img src="../../assets/images/my profile icon/my profile icon/gmail.svg" alt="Gmail icon for email contact">
                        </a>
                    </div>
                </div>
                <!----end of social----------->
                <!--------email and whats----------->
                <div class="d-flex justify-content-between align-items-center flex-column flex-md-row gap-3 email-accounts">
                    <div>
                        <h4>Email me</h4>
                        <div>
                            <a href="mailto:nourhanmahmoudahmed46@gmail.com" class="d-flex align-items-center gap-2">
                                <img src="../../assets/images/my profile icon/my profile icon/skill-icons_gmail-light.svg">
                                nourhanmahmoudahmed46@gmail.com
                            </a>
                        </div>
                    </div>

                    <div>
                        <h4>Let’s chat on whatsapp</h4>
                        <div>
                            <a href="tel:+1234567890" class="d-flex align-items-center gap-2">
                                <img src="../../assets/images/my profile icon/my profile icon/ri_whatsapp-fill.svg" class="w-80">

                                01125865883
                            </a>
                        </div>
                    </div>

                </div>
                <!------------------------>
            </div>

        </div>
    </section>
</template>
<style lang="scss" scoped>
a{
    transition: 0.2s ease-in-out;
    &:hover{
        transform: translateY(4px);
    }
}
#contact {
    margin-top: 54px;
    padding-top: 120px;
}

.social {
    border-top: 5px solid #6645AE;
    box-shadow: 1px 2px 7px 2px #efefef;
    padding-bottom: 45px;
    padding-right: 40px;
    padding-left: 40px;
    background: #7f56d908;
}

.user-img {
    border-radius: 50%;
    width: 179px;
    height: 182px;
    overflow: hidden;
    margin-top: -95px;
    padding-bottom: 10px;
}

img {
    width: 100%;
    height: auto;
    object-fit: cover;
}
.email-accounts{
    h4{
        padding-left: 30px;
        font-size: 20px;
        margin-bottom: 17px;
    }
    a{
        color : #42307D;
        font-weight: normal;
        font-size: 18px;
        text-decoration: none;
    }
    img{
        width: 24px;
        height: 24px;
    }
}
.designer{
    p:nth-of-type(1){
        font-family: "Dancing Script", cursive;
        font-size: 34px;
        font-weight: bold;
        color: #3D1498;
    }
    p:nth-of-type(2){
        color: #3D1498;
        font-family: "Poppins", sans-serif;
        font-size: 20px;
        font-weight: bold;
        margin-bottom: 12px;
    }
    span{
        color: #000;
        font-family: "Poppins", sans-serif;
        font-size: 18px;
    }
}
</style>
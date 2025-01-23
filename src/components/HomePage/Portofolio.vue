<template>
    <section id="portofolio">
        <div class="section__heading">
            <h2> My <span> Work Experience </span></h2>
        </div>
        <div class="container">
            <div class="row">
                <div class="col-lg-6">
                    <div class="experience__item">
                        <h3>UI UX designer </h3>
                        <div class="d-flex align-items-center gap-3">
                            <span>
                                UMed Mi
                            </span>
                            <span>
                                Sep 2020- 2023
                            </span>
                        </div>
                        <p>
                            Enhanced usability and efficiency of healthcare platforms, reducing
                            time-to-task for medical staff and improving patient satisfaction
                            through user-friendly interfaces
                        </p>
                    </div>

                    <div class="mt-40 experience__item">
                        <h3>Freelancer-Upwork </h3>
                        <div class="d-flex align-items-center gap-3">
                            <span>
                                Freelancer-Upwork
                            </span>
                            <span>
                                Sep 2018- 2020
                            </span>
                        </div>
                        <p>
                            Ý Cross-Platform Expertise: Designed intuitive interfaces for web,
                            mobile, and responsive platforms, adhering to industry best practices
                            and accessibility standards
                        </p>
                    </div>
                </div>

                <div class="col-lg-6 ">
                    <div class="exprience_line position-relative">
                       <div class="left-img">
                        <img src="../../assets/images/Frame11.png" alt="frame">
                         </div>
                        <div class="experience__item">
                        <h3>Senior UI UX designer </h3>
                        <div class="d-flex align-items-center gap-3">
                            <span>
                                Grand technology
                            </span>
                            <span>
                                Sep 23- present
                            </span>
                        </div>
                        <p>
                            Led the full design lifecycle for complex web
                            and mobile applications, from conceptualization and user research to
                            high-fidelity design and handoff
                        </p>
                    </div>

                    <div class="mt-40 experience__item">
                        <h3>Team lead </h3>
                        <div class="d-flex align-items-center gap-3">
                            <span>
                                Misk it
                            </span>
                            <span>
                                Sep 2022 - July 2023
                            </span>
                        </div>
                        <p>
                            Streamlined workflows, reducing project turnaround times and
                            improving team productivity·
                            Mentored junior designers, several of whom advanced to senior roles within the company
                        </p>
                    </div>
                    </div>
                </div>

            </div>
        </div>
    </section>
</template>
<style lang="scss" scoped>
#portofolio {
    margin-top: 80px;
    margin-bottom: 80px;
}
.section__heading {
    padding-bottom: 50px;
}
.experience__item{
    h3{
        font-family: "Poppins", sans-serif !important;
        color: #344054;
        font-size: 30px;
        font-weight: 600;
        line-height: 1.5;
        margin-bottom: 18px;
    }
    span:nth-of-type(1){
        color: #344054;
        font-size: 25px;
        font-weight: 500;
        line-height: 1.2;
    }
    span:nth-of-type(2){
        line-height: 1.2;
    }
    p{
        margin-top: 18px;
        margin-bottom: 15px;
    }
    span:nth-of-type(2),p{
        font-size: 18px;
        font-weight: normal;
        font-family: "Poppins", sans-serif !important;
        color: #98A2B3;
    }
}
.exprience_line{
    padding-left: 70px;
}
.left-img{
    position: absolute;
    left: -10px;
    top: 0;
}
@media screen and (max-width: 996px) {
.exprience_line{
    padding-left: 0px;
    padding-top: 100px;
} 
.left-img {
        position: absolute;
        top: 154px;
        transform: rotate(90deg);
        right: 0;
    }
}
</style>
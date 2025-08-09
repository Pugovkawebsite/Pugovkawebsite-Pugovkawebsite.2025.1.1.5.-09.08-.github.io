<template>
 <div class="app">
    <div class="main">
      <user-card :users="users"/>
      <div class="contact">
        <div class="contact__wrap">
          <contacts-card :contacts="contacts"/>
        </div>
        <img class="elem__gorizont" src="./img/divider.svg">
      </div>
      <div class="socials">
        <div class="socials__wrap">
          <div class="socials__text">Socials</div>
            <socials-card :socials="socials"/>
        </div>
        <img class="gray" src="./img/divider.svg"> 
      </div>
      <div class="languages">
        <div class="languages__wrap">
          <div class="languages__text__small">Languages</div>
          <languages-card :languages="languages"/>
        </div>

      </div>
      <div class="hobbies">
        <div class="hobbies__text__small">Hobbies & Interests</div>
        <hobbies-card :hobbies="hobbies"/>
      </div>
       

    </div>
    <div class="content">
      <div class="main-wrap main-wrap__height__education">
        <grafic-elem :elem="elem"/>
        <div class="education">
          <div class="title">Education</div>
          <div class="education__content-wrap">
            <education-card :universities="universities"/>
          </div>
        </div>
      </div>
      <div class="main-wrap main-wrap__height__achievements">
        <grafic-elem :elem="elem"/>
        <div class="achievements">
          <div class="title title_achievements">Achievements</div>
            <div class="achievements__content-wrap">
              <achievements-card :achievements="achievements"/>
            </div>
        </div>
      </div>
      
      
      <div class="main-wrap main-wrap__height__skills">
      <grafic-elem :elem="elem"/>
        <div class="skills">
          <div class="title">Tools/Skills</div>
            <div class="skills__content-wrap">
              <div class="skills__content-wrap-1">
                <skills-card :skills="skills"/>
              </div>
              <div class="skills__content-wrap-2">
                <tools-card :tools="tools"/>
              </div>
            </div>
            
        </div>
      </div>
      <div class="main-wrap main-wrap__height__project">
       <grafic-elem :elem="elem"/>
        <div class="projects">
          <div class="title">Latest projects</div>
          <div class="projects__content-wrap">
          <projects-card :projects="projects"/>
          </div>

          
        </div>
      </div>
      <div class="main-wrap main-wrap__height__certificates">
        <grafic-elem :elem="elem"/>
        <div class="certificates">
          <div class="title">Certificates & Awards</div>
            <div class="certificates__content-wrap">
              <certificates-card :certificates="certificates"/>
            </div>
        </div>
      </div>
    </div>
      
   
 </div>
</template>


<script>
import EducationCard from "./components/EducationCard.vue";
import CertificatesCard from "./components/CertificatesCard.vue";
import AchievementsCard from "./components/AchievementsCard.vue";
import SkillsCard from "./components/SkillsCard.vue";
import ToolsCard from "./components/ToolsCard.vue";
import ProjectsCard from "./components/ProjectsCard.vue";
import GraficElem from "./components/GraficElem.vue";
import ContactsCard from "./components/СontactsCard.vue";
import SocialsCard from "./components/SocialsCard.vue";
import LanguagesCard from "./components/LanguagesCard.vue";
import HobbiesCard from "./components/HobbiesCard.vue";
import UserCard from "./components/UserCard.vue";


export default {
  components: {
    EducationCard,
    CertificatesCard,
    AchievementsCard,
    SkillsCard,
    ToolsCard,
    ProjectsCard,
    GraficElem,
    ContactsCard, 
    SocialsCard,
    LanguagesCard,
    HobbiesCard,
    UserCard
  }, 
  data() {
    return {
      users: [
        {id: 1, name: "Anurag Yadav", img: "/img/persone.svg", title: "Chandigarh University", about: "A well-organized, creative and goaloriented graduate possessing excellent communication, problem-solving and leadership skills with a flair to explore Computer Science Engineering"}
      ],
      universities: [
        {id: 1, img: "/img/education/Chandigarh_University.svg", title: "Chandigarh University", level: "Bachelor in Computer Science Engineering", time: "2020 - 2024", completion: "- 9 CGPA"},
        {id: 2, img: "/img/education/Suditi.svg", title: "Suditi Global Academy", level: "Intermediate XI - XII (CBSE)", time: "2018-2020", completion: "- 85%"},
        {id: 3, img: "/img/education/Akanksha.svg", title: "Akanksha Global Acadmey", level: "High School IX - X (CBSE)", time: "2016-2018", completion: "- 92%"}
      ],
      certificates: [
        {company: "freeCodeCamp", name: "Responsive Web Design", time: "Dec 2021 - Feb 2022", img: "/img/certificates/free_code_camp.svg"}, 
        {company: "Google", name: "Data Strcture & Algorithms", time: "Mar 2021 - Jun 2021", img: "/img/certificates/google.svg"}
      ],
      achievements: [
        {id: 1, time: "Present", place: "Chandigarh", role: "Graphic Designer", company: "Alexa Dev Community", img: "/img/achievements/Logo_ADC.svg", descr: "Creatively Designing and Developing web UI for Chandigarh University’s Alexa Developer Community, upcoming big launch of full website."},
        {id: 2, time: "Oct 2021 - Nov 2021", place: "Online", role: "Hacktoberfest Contributor", company: "Github", img: "/img/achievements/Logo_GitHub.svg", descr: "Contributed 8 PR’s in various open source projects. Great experience and learning alot about working with Github and open-source. Connecting with developers"},
        {id: 3, time: "Jan 2021 - March 2021", place: "Online", role: "Contributor", company: "Winter of Code", img: "/img/achievements/Logo_winter.svg", descr: "Overwhelming to be a part of DSC NSEC project - DSC NSEC Algorithms for Winter of Code 2020. First introduction to Git and Github. How github is used by most of the programmers in order to manage the projects."},
        {id: 4, time: "Oct 2020 - Dec 2020", place: "Online", role: "30Days of Google Cloud", company: "Google", img: "/img/achievements/Logo_google.svg", descr: "Hands on practice on Google Cloud Platform - the tool that powers apps like Google Search, Gmail and YouTube. As part of the program had learned the concepts like computing, application development, big data & machine learning using cloud."}
      ],
      skills: [
        {id: 1, name: "Figma", function: " Web UI Design, Prototyping", img: "/img/skills/Figma.svg"},
        {id: 2, name: "Java", function: "Software Development", img: "/img/skills/Java.svg"},
        {id: 3, name: "Python", function: "Design workspace", img: "/img/skills/Python.svg"}
      ],
      tools: [
        {id: 1, name: "HTML 5", function: "Structural Design", img: "/img/skills/HTML5.svg"},
        {id: 2, name: "CSS 3", function: "Style Design", img: "/img/skills/CSS3.svg"},
        {id: 3, name: "Wordpress", function: "Web development", img: "/img/skills/Wordpress.svg"},
        {id: 4, name: "VS Code", function: "Code editor", img: "/img/skills/VS.svg"},
        {id: 5, name: "Notion", function: "Project managment", img: "/img/skills/Notion.svg"},
      ],
      projects: [
        {id: 1, name: "Alexa Dev Community Landing Page", role: "Web UI design for alexa developers comunity", img: "/img/projects/ADC.svg", link: "https//figma.com", img2: "/img/projects/figma_icon.svg"},
        {id: 1, name: "Portfolio Webpage", role: "Personal Portfolio webpage with resume and blog", img: "/img/projects/Portfolio.svg", link: "https://anuragyadav365.github.io", img2: "/img/projects/portfolio_icon.svg"},
      ],
      contacts: [
        {id: 1, name: "Email", address: "anuragyadavmnp@gmail.com", img: "/img/contacts/mail.svg"},
        {id: 2, name: "Website", address: "https://anuragyadav365.github.io/portfolio.html", img: "/img/contacts/link.svg"},
        {id: 3, name: "Phone", address: "(+91) 981 5533 309", img: "/img/contacts/phone.svg"},
        {id: 4, name: "Address", address: "Hallomajra, Chandigarh, India", img: "/img/contacts/location.svg"},
      ],
      socials: [
        {id: 1, name: "Instagram", address: "@anurag.yadav.007", img: "/img/socials/instagram.svg"},
        {id: 2, name: "Github", address: "@anuragyadav365", img: "/img/socials/github.svg"},
        {id: 3, name: "Twitter", address: "@anuragmnp", img: "/img/socials/twitter.svg"},
        {id: 4, name: "Linkedin", address: "@anuragyadav", img: "/img/socials/linkedin.svg"},
      ],
      languages: [
        {id: 1, name: "Hindi", level: "Native", img: "/img/languages/Hindi.svg"},
        {id: 2, name: "English", level: "Professional working", img: "/img/languages/English.svg"},
        {id: 3, name: "Spanish", level: "Elementary", img: "/img/languages/Flag.svg"},
      ],
      hobbies: [
        {id: 1, name: "Gaming", img: "/img/hobbies/gaming.svg"},
        {id: 2, name: "Travelling", img: "/img/hobbies/travelling.svg"},
        {id: 3, name: "Sketching/Graffitti", img: "/img/hobbies/sketching.svg"},
        {id: 4, name: "Blogging", img: "/img/hobbies/blogging.svg"}
      ]
    } 
  }
}

</script>



<style>

.content {
  padding-top: 64.54px;
  width: 843px;
  height: 1698px;
}
.main {
  width: 354px;
  height: 1698px;
  background: #fff;
  padding: 48px;
}
.education {
  padding: 0px 0px 48px 0px;
  width: 697px;
  height: 272px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.main-wrap__height__education {
  height: 272px;
}
.title {
  font-weight: 500;
  font-size: 24px;
  color: #2e2e48;
}
.education__content-wrap {
  width: 697px;
  height: 158px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.certificates {
  width: 695px;
  height: 269px;
}
.main-wrap__height__certificates {
  height: 269px;
}
.certificates__content-wrap {
  margin-top: 32px;
  margin-bottom: 48px;
}
.achievements {
  padding: 0px 0px 48px 0px;
  width: 697px;
  height: 471px;
}
.main-wrap__height__achievements {
  height: 471px;
}
.achievements__content-wrap {

}
.title_achievements {
  margin-bottom: 32px;
}
.skills {
  width: 697px;
  height: 363.76px;
}
.main-wrap__height__skills {
  height: 363.76px;
}
.skills__content-wrap {
  margin-top: 32.27px;
  width: 697px;
  height: 250px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.skills__content-wrap-1 {
  width: 697px;
  height: 129px;
  display: flex;
  justify-content: space-between;
}
.skills__content-wrap-2 {
  width: 697px;
  height: 112px;
  display: flex;
  justify-content: space-between;
}
.projects {
  width: 697px;
  height: 264.45px;
}
.main-wrap {
  width: 793.81px;  
  display: flex;
  justify-content: start;
}
.main-wrap__height__project {
  height: 264.45px;
}
.projects__content-wrap {
  margin-top: 32.27px;
  width: 697px;
  height: 150px;
  display: flex;
  justify-content: space-between;
}
.contact {
  height: 314px;
}
.contact__wrap {
  margin-top: 32.27px;
  margin-bottom: 32.27px;
  width: 266px;
  height: 250px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.socials {
  height: 322.35px;
}
.socials__wrap{
  width: 266px;
  height: 257px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-bottom: 32.27px;
  margin-top: 32.27px;
}
.socials__text {
  padding-top: 1px;
  font-weight: 400;
  font-size: 12px;
  color: #79819a;
}
.languages__wrap {
  width: 266px;
  height: 197px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin-bottom: 32.27px;
  margin-top: 32.27px;
}
.languages__text__small {
  font-weight: 400;
  font-size: 12px;
  color: #79819a;
}
.hobbies {
  width: 266px;
  height: 218px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
@media(max-width: 1199px) {
  .app {
    width: 985px;
  }
  .main {
    width: 308px;
    padding: 28px;
  }
  .content, .main-wrap {
    width: 645px;
  }
  .education, .achievements, .skills, .projects, .certificates, .projects__content-wrap, .skills__content-wrap, .education__content-wrap {
    width: 588px;
  }
  .elem {
    width: 86.81px;
  }
  .skills__content-wrap-1, .skills__content-wrap-2 {
    width: 588px;
  }
 
 
}
@media(max-width: 987px) {
  .app {
    width: 765px;
  }
  .content, .main-wrap {
    width: 565px;
  }
  .main {
    width: 200px;
    padding: 14px;
    padding-right: 4px;
  }
  .elem__gorizont {
    width: 170px;
  }
  .education, .achievements, .skills, .projects, .certificates, .projects__content-wrap, .skills__content-wrap, .education__content-wrap {
    width: 532px;
  }
  .elem {
    width: 70.81px;
  }
  .skills__content-wrap-1, .skills__content-wrap-2 {
    width: 532px;
  }
  .title {
    font-size: 22px;
    padding-left: 15px;
  }
  
}


@media(max-width: 767px) {
  .app {
    width: 570px;
    flex-direction: column;
    overflow: hidden;
  }
  .main, .content, .contact__wrap {
    width: 570px;
  }
  .education, .achievements, .skills, .projects, .certificates, .projects__content-wrap, .skills__content-wrap, .education__content-wrap {
    width: 477px;
  }
  .languages {
    width: 570px;
  }
  .elem__gorizont {
    width: 500px;
    height: 4px;
  }
  .socials__wrap {
    width: 510px;
    height: 217px;
    margin-bottom: 0px;
    flex-wrap: wrap;
    flex-direction: row;
  }
  .socials__text {
    font-size: 16px;
    height: 30px;
  }
  .socials__text {
    width: 100%;
  }
  .socials {
    height: 270.35px;
  }
  .languages__wrap {
    width: 514px;
  }
  .languages__text__small, .hobbies__text__small {
    font-size: 16px;
    width: 100%;
  }
  .languages__wrap {
    height: 127px;
    flex-direction: row;
    flex-wrap: wrap;
  }
  .language-card__descr {
    width: 115px;
  }
  .language-card {
    width: 160px;
  }
  .gray {
    width: 500px;
    height: 3px;
  }
  .hobbies {
    width: 514px;
    flex-direction: row;
    flex-wrap: wrap;
    height: 160px;
  }
  .main {
    height: 1320px;
    padding: 30px;
  }
  .elem {
    width: 66.81px;
  }
  .main-wrap {
    width: 574px;
  }
  .education, .achievements, .skills, .projects, .certificates, .projects__content-wrap, .skills__content-wrap, .education__content-wrap {
    width: 477px;
  }
  .education__content-wrap {
    flex-direction: column;
  }
  .education {
    height: 612px;
    justify-content: start;
  }
  .education__content-wrap {
    margin-top: 10px;
    height: 502px;
  }
  .content {
    height: 2188px;
  }
  .main-wrap__height__education {
    height: 552px;
  }
  .main-wrap__height__achievements {
    height: 671px;
  }
  .skills__content-wrap-1, .skills__content-wrap-2 {
    width: 507px;
  }
}
@media(max-width: 575px) {
  
  #app {
    max-width: 390px;
    overflow: hidden;
    margin: 0 auto;
  }
  .app, .main, .content, .contact__wrap {
    width: 400px;
  }
  .main {
    padding: 15px;
  }
  .elem__gorizont {
    width: 300px;
  }
  .contact__wrap {
    width: 370px;
  }
  .socials__wrap {
    width: 370px;
    height: 267px;
    margin-top: 5.27px;
  }
  .gray {
    width: 300px;
  }
  .social-card__address {
    font-size: 14px;
  }
  .languages__wrap {
    flex-direction: column;
  }
  .languages__wrap {
    height: 227px;
  }
  .languages__wrap {
    width: 300px;
  }
  .languages {
    width: 300px;
  }
  .hobbies {
    width: 300px;
  }
  .elem {
    width: 36.81px;
  }
  .education, .achievements, .skills, .projects, .certificates, .projects__content-wrap, .skills__content-wrap, .education__content-wrap {
    width: 280px;
  }
  .title {
    font-size: 20px;
  }
  .main-wrap {
    width: 320px;
  }
  .skills__content-wrap-1 {
    width: 280px;
    height: 360px;
    flex-wrap: wrap;
  }
  .skills__content-wrap {
    height: 700px;
  }
  .content {
    height: 2728px;
  }
  .skills__content-wrap-2 {
    height: 330px;
    flex-wrap: wrap;
    width: 280px;
  }
  .skills {
    height: 680.76px;
  }
  .main-wrap__height__skills {
    height: 780.76px;
  }
  .projects__content-wrap {
    flex-direction: column;
  }
  .projects__content-wrap {
    height: 350px;
    margin-bottom: 10px;
  }
  .projects {
    height: 380px;
  }
  .main-wrap__height__project {
    height: 414.45px;
  }
  .socials__text {
    padding-top: 10px;
  }
      
}
@media(max-width: 459px) {
  #app {
    max-width: 300px;
    margin: 0 auto;
  }
  .app, .main, .content  {
    width: 300px;
  }
  .elem__gorizont {
    width: 260px;
  }
  .contact__wrap, .contact-card, .contact__wrap {
    width: 270px;
  }  
  .main {
    height: 1350px;
  }
  .content {
    padding-top: 14px;
  }
  .hobbies {
    height: 100px;
  }
  .education, .achievements, .skills, .projects, .certificates, .projects__content-wrap, .skills__content-wrap, .education__content-wrap {
    width: 260px;
  }
  .skills__content-wrap-2 {
    width: 255px;
    height: 280px;
  }
  .skills__content-wrap {
      height: 610px;
    }
  .main-wrap__height__skills {
    height: 700.76px;
  }
  .title {
    font-size: 18px;
  }
  .content {
    height: 2600px;
  }
  .socials__text {
    font-size: 15px;
  }
  .achievements {
    height: 678px;
  }
  .title_achievements {
    margin-bottom: 12px;
  }
  .main-wrap__height__achievements {
    height: 677px;
  }
}
</style>

<template>
  <div class="home container-fluid">
    <div class="row" style="height:75px"></div>

    <!-- ABOUT ME -->
    <div class="row">
      <div
        class="col-xs-12 order-xs-1 col-sm-12 order-sm-1 col-md-6 order-md-2"
      >
        <img
          :src="require('@/assets/img/IMG_7090hc.jpg')"
          class="portrait mb-3"
        />
      </div>
      <div
        class="col-xs-12 order-xs-2 col-sm-12 order-sm-2 col-md-6 order-md-1"
      >
        <h1 class="text-left">Justin Mattson</h1>
        <h2 class="text-left" style="font-size:16px;">
          <a href="mailto:justin.mattson@outlook.com">
            <i class="far fa-envelope"></i> justin.mattson@outlook.com</a
          >
        </h2>
        <br />
        <h2 class="text-left" style="font-size:20px;">
          &nbsp;Experience Highlights
        </h2>
        <div class="text-left">
          <ul class="pr-3">
            <li>
              Many years experience solving problems and analyzing data,
              advancing from equipment maintenance technician to test solutions
              engineer.
            </li>
            <li>
              Global project and process management, successfully collaborating
              across cultures and language barriers.
            </li>
            <li>
              Encountered career roadblock due to a lack of software development
              experience.
            </li>
            <li>
              Completed Immersive Full Stack program at Boise Codeworks and
              loves having yet another skillset in the ever expanding toolbox!
            </li>
            <li>
              Seeking software development opportunities, involving front-end
              and/or back-end, potentially combined with data analysis and
              UI/UX.
            </li>
            <li>
              Experience testing
              <a
                href="https://www.interactiveaccessibility.com/accessibility-statistics#:~:text=57%20Million%20Americans%20have%20a%20Disability&text=Consider%20impairments%20that%20impact%20accessibility,have%20difficulty%20lifting%20or%20grasping."
                >accessibility</a
              >
              using
              <a href="https://www.w3.org/WAI/standards-guidelines/wcag/glance/"
                >WCAG 2.1</a
              >
              guidelines within multiple user environments/devices.
            </li>
          </ul>
        </div>
      </div>

      <!-- <div class="col-12">Passions:</div> -->
    </div>

    <!-- SKILLS / EDUCATION -->
    <div class="container-fluid">
      <div class="row d-flex justify-content-around">
        <div class="col-12 mt-3 mb-0">
          <H2 class="text-center text-shadow-light">Skills / Education:</H2>
          <skills v-for="skill in skills" :key="skill.title" :skill="skill" />
        </div>
        <!-- Codeworks -->
        <div
          class="card col-12 col-md-5 col-lg-3 my-3 shadow border border-secondary"
        >
          <img
            src="@/assets/img/BCW.jpg"
            class="card-img-top p-3"
            alt="Photo of Justin Mattson"
          />
          <div class="card-body pt-0">
            <h3 class="card-title">500+ Hours Coding</h3>
            <ul class="card-text text-left">
              <li>HTML5 & CSS3</li>
              <li>JavaScript ES6</li>
              <li>Web API / HTTP</li>
              <li>JS Frameworks</li>
              <li>Nodejs</li>
              <li>DotNet Core C#</li>
              <li>SQL</li>
              <li>MongoDb</li>
              <li>Agile / Scrum</li>
            </ul>
            <a
              href="https://boisecodeworks.com/"
              target="_blank"
              class="btn btn-outline-primary"
              >Codeworks</a
            >
          </div>
        </div>

        <!-- Continuing Education -->
        <div
          class="card col-12 col-md-5 col-lg-3 my-3 shadow border border-secondary"
          style="background-color:#bee8f8"
        >
          <img src class="card-img-top" alt />
          <div class="card-body">
            <h4 class="card-title">Continuing Education</h4>
            <p class="card-text text-left">
              <b>Micron Technology, Inc.</b>
              <br />
              <small>
                <i class="fas fa-long-arrow-alt-right"
                  >&nbsp;Project Management</i
                >
                <br />
                <i class="fas fa-long-arrow-alt-right">&nbsp; Data Analysis</i>
                <br />
                <i class="fas fa-long-arrow-alt-right"
                  >&nbsp; Problem Solving</i
                >
              </small>
            </p>
            <p class="card-text text-left">
              <b>Boise State University</b>
              <br />
              <small>
                <i class="fas fa-long-arrow-alt-right"
                  >&nbsp;Electrical & Computer Engineering</i
                >
                <br />
                <i class="fas fa-long-arrow-alt-right"
                  >&nbsp;Computer Science</i
                >
              </small>
            </p>
            <p class="card-text text-left">
              <b>College of Southern Idaho</b>
              <br />
              <small>
                <i class="fas fa-long-arrow-alt-right"
                  >&nbsp;Upper Division Mathematics</i
                >
              </small>
            </p>
            <p class="card-text text-left">
              <b>Flathead Valley Community College</b>
              <br />
              <small>
                <i class="fas fa-long-arrow-alt-right"
                  >&nbsp;General Education</i
                >
              </small>
            </p>
            <!-- <a href="#" class="btn btn-outline-primary">Go somewhere</a> -->
          </div>
        </div>

        <!-- Devry Phoenix -->
        <div
          class="card col-12 col-md-5 col-lg-3 my-3 shadow border border-warning bg-secondary"
        >
          <img src="@/assets/img/devry-logo.svg" class="card-img-top p-3" alt />
          <div class="card-body pt-0">
            <h5 class="card-title" style="color:black;">Electronics</h5>
            <p class="card-text" style="color:black;">
              Associate of Applied Science
            </p>
            <a
              href="https://www.devry.edu/about/campus-locations/arizona/phoenix.html"
              target="_blank"
              class="btn btn-outline-warning"
              >DeVry Phoenix</a
            >
          </div>
        </div>
      </div>
    </div>

    <!-- BWMA -->
    <div class="row bg-image" style="height:100vh">
      <div class="col-12 cursive" style="height:100vh;">
        <div class style="height:75px;"></div>
        <B>
          <p>
            The best thing about starting a Vue project from scratch is...
            <br />I can let my imagination run wild!
          </p>
        </B>
      </div>
    </div>

    <!-- PROJECTS -->
    <div class="row py-3" style="background-color:#8888;">
      <div class="col-12">
        <H2 class="text-center py-3 text-shadow-light"
          >Software Development Projects:</H2
        >
      </div>
      <applications v-for="app in applications" :key="app.name" :app="app" />
    </div>

    <!-- POSITIVITY! -->
    <div class="col-12 valign p-1 bg-happy" style="height:950px">
      <div
        class="d-flex valign text-light text-shadow-dark"
        style="font-size:72pt;"
      >
        Have a nice day!
      </div>
    </div>

    <!-- FOOTER -->
    <div class style="height:50px;"></div>
    <div
      class="col-12 text-center fixed-bottom p-0"
      style="background-color:#fffd"
    >
      <div style="font-weight:700;">
        Made with
        <img src="@/assets/logo.png" style="height: 1em" />
        by Justin Mattson
        <br />
        <a href="https://www.facebook.com/justin.mattson.9" target="_blank">
          <i
            class="fa fa-facebook-official text-dark-vue"
            aria-hidden="true"
          ></i> </a
        >&nbsp;
        <a href="https://www.linkedin.com/in/justin-mattson" target="_blank">
          <i
            class="fa fa-linkedin-square text-dark-vue"
            aria-hidden="true"
          ></i> </a
        >&nbsp;
        <a href="https://justinmattson.github.io/" target="_blank">
          <i class="fa fa-github text-dark-vue p-1" aria-hidden="true"></i> </a
        >&nbsp;
        <a href="mailto:justin.mattson@outlook.com" class="text-dark">
          <i class="fa fa-envelope-o text-dark-vue" aria-hidden="true"></i>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import Skills from "@/components/Skills.vue";
import Applications from "@/components/Applications.vue";
export default {
  name: "Home",
  data() {
    return {
      skills: [
        {
          title: "VSCode",
          link: "https://code.visualstudio.com/",
          imgUrl: "https://www.userlogos.org/files/vscode-logo.png",
        },
        {
          title: "HTML",
          link: "https://en.wikipedia.org/wiki/HTML5",
          imgUrl:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/120px-HTML5_logo_and_wordmark.svg.png",
        },
        {
          title: "CSS",
          link: "https://en.wikipedia.org/wiki/CSS",
          imgUrl:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/d/d5/CSS3_logo_and_wordmark.svg/100px-CSS3_logo_and_wordmark.svg.png",
        },
        {
          title: "JS",
          link: "https://en.wikipedia.org/wiki/JavaScript",
          imgUrl:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/b/ba/Javascript_badge.svg/2000px-Javascript_badge.svg.png",
        },
        {
          title: "Bootstrap",
          link: "https://getbootstrap.com/",
          imgUrl: "http://pluspng.com/img-png/bootstrap-png-bootstrap-512.png",
        },
        {
          title: "Font Awesome",
          link: "https://fontawesome.com/",
          imgUrl:
            "https://www.drupal.org/files/project-images/font_awesome_logo.png",
        },
        {
          title: "GetHub",
          link: "https://github.com/",
          imgUrl:
            "http://www.seeklogo.net/wp-content/uploads/2015/09/github-mark-logo-400x400.png",
        },
        {
          title: "NPM",
          link: "https://www.npmjs.com/",
          imgUrl:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/d/db/Npm-logo.svg/1200px-Npm-logo.svg.png",
        },
        {
          title: "Vue.js",
          link: "https://vuejs.org/",
          imgUrl: "https://vuejs.org/images/logo.png",
        },
        {
          title: "Node.js",
          link: "https://nodejs.org/en/",
          imgUrl:
            "https://nodejs.org/static/images/logos/nodejs-new-pantone-black.svg",
        },
        {
          title: "MongoDB",
          link: "https://www.mongodb.com/",
          imgUrl:
            "https://www.gigapros.com/portal/wp-content/uploads/2014/12/mongodb.png",
        },
        {
          title: "Postman",
          link: "https://www.postman.com/",
          imgUrl:
            "https://huddle.eurostarsoftwaretesting.com/wp-content/uploads/2018/10/pm-logo-vert.png",
        },
        {
          title: "Auth0",
          link: "https://auth0.com/",
          imgUrl: "https://avatars1.githubusercontent.com/u/2824157?v=4&s=400",
        },
        {
          title: "Heroku",
          link: "https://www.heroku.com/",
          imgUrl:
            "https://brand.heroku.com/static/media/heroku-logo-stroke.aa0b53be.svg",
        },
        {
          title: "C#",
          link: "https://docs.microsoft.com/en-us/dotnet/csharp/",
          imgUrl:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/0/0d/C_Sharp_wordmark.svg/464px-C_Sharp_wordmark.svg.png",
        },
        {
          title: "MySQL",
          link: "https://www.mysql.com/",
          imgUrl: "https://www.mysql.com/common/logos/logo-mysql-170x115.png",
        },
        {
          title: "GearHost",
          link: "http://gearhost.com/",
          imgUrl: "http://www.gearhost.com/Content/images/svgs/tach.svg",
        },
        {
          title: "Docker",
          link: "https://www.docker.com/",
          imgUrl:
            "https://www.docker.com/sites/default/files/d8/styles/role_icon/public/2019-07/Moby-logo.png?itok=sYH_JEaJ",
        },
        {
          title: "StackOverflow",
          link: "https://stackoverflow.com/",
          imgUrl:
            "https://cdn.sstatic.net/Sites/stackoverflow/company/Img/logos/so/so-icon.png?v=c78bd457575a",
        },
        {
          title: "Figma",
          link: "https://www.figma.com/",
          imgUrl: "http://cdn.embed.ly/providers/logos/figma.png",
        },
        {
          title: "LucidChart",
          link: "https://www.lucidchart.com/",
          imgUrl:
            "https://d2slcw3kip6qmk.cloudfront.net/marketing/images/LucidLogo_Website.svg",
        },
        {
          title: "Trello",
          link: "https://trello.com/",
          imgUrl:
            "https://d2k1ftgv7pobq7.cloudfront.net/meta/u/res/images/brand-assets/Logos/0099ec3754bf473d2bbf317204ab6fea/trello-logo-blue.png",
        },
        {
          title: "React",
          link: "https://reactjs.org/",
          imgUrl: "https://tactless7.github.io/cv/img/icons/react_logo_2.png",
        },
        {
          title: "Halfmoon",
          link: "https://www.gethalfmoon.com/",
          imgUrl: "https://www.gethalfmoon.com/static/halfmoon/img/hm-logo.svg",
        },
        {
          title: "Python",
          link: "https://www.python.org/",
          imgUrl:
            "https://files.realpython.com/media/python-logo.8eb72ea6927b.png",
        },
        {
          title: "Selenium",
          link: "https://www.selenium.dev/",
          imgUrl:
            "https://th.bing.com/th/id/OIP.NPQVOCjh0Pqb-yO8BgQ5HQAAAA?w=179&h=180&c=7&o=5&dpr=1.5&pid=1.7",
        },
        // {
        //   title: null,
        //   link: null,
        //   imgUrl: null,
        // },
      ],
      applications: [
        {
          githubUrl: "https://github.com/chuckmcclain/saaanr-cs",
          hostName: "Heroku",
          hostUrl: "https://saaanr.herokuapp.com/",
          img: "saaanr.jpg",
          name: "SAAA Northern Rockies",
          stack: "Vue.js | C# | MySQL",
        },
        {
          githubUrl: "https://github.com/JustinMattson/mttreasures",
          hostName: "Heroku",
          hostUrl: "https://mttreasures.herokuapp.com/",
          img: "mttreasures.png",
          name: "MT Treasure",
          stack: "Vue.js | Node.js | MongoDB",
        },
        {
          githubUrl: "https://github.com/JustinMattson/CS-final-keepr",
          hostName: "Heroku",
          hostUrl: "https://keepr252.herokuapp.com/#/",
          img: "keepr.png",
          name: "Keepr",
          stack: "Vue.js | C# | MySQL",
        },
        {
          githubUrl: "https://github.com/JustinMattson/capstone-volunteer",
          hostName: "Heroku",
          hostUrl: "https://capstone-volunteer.herokuapp.com",
          img: "volunteer.png",
          name: "Volunteer (Capstone Team: Kevin Lane, Xander Rutledge)",
          stack: "Vue.js | Node.js | MongoDB",
        },
        {
          githubUrl: "https://github.com/JustinMattson/checkpoint-buglog",
          hostName: "Heroku",
          hostUrl: "https://checkpoint-buglog.herokuapp.com",
          img: "buglog.png",
          name: "BugLog",
          stack: "Vue.js | Node.js | MongoDB",
        },
        {
          githubUrl: "https://github.com/JustinMattson/checkpoint-kanban",
          hostName: "Heroku",
          hostUrl: "https://checkpoint-kanban.herokuapp.com",
          img: "kanban.png",
          name: "Kanban (Partner Application: Kevin Lane)",
          stack: "Vue.js | Node.js | MongoDB",
        },
        {
          githubUrl: "https://github.com/JustinMattson/bloggr-checkpoint",
          hostName: "Readme",
          hostUrl: "https://justinmattson.github.io/bloggr-checkpoint",
          img: "bloggr.png",
          name: "Bloggr",
          stack: "VUE | JS | Auth0",
        },
        {
          githubUrl: "https://github.com/JustinMattson/hackathon-1",
          hostName: "Hackathon:LocalHost",
          hostUrl: null,
          img: "sceneit.png",
          name: "Scene It! (Team: Troy Fuhriman, Steven Packard, Kevin Lane)",
          stack: "JS | Node.js | MongoDB",
        },
        {
          githubUrl: "https://github.com/JustinMattson/CheckPoint4-inspire",
          hostName: "GitHub",
          hostUrl: "https://justinmattson.github.io/checkpoint4-inspire/",
          img: "inspire.png",
          name: "Inspire",
          stack: "JS | HTML | CSS",
        },
        {
          githubUrl: "https://github.com/JustinMattson/CheckPoint3-TaskMaster",
          hostName: "GitHub",
          hostUrl: "https://justinmattson.github.io/CheckPoint3-TaskMaster",
          img: "taskmaster.png",
          name: "Task Master",
          stack: "JS | HTML | CSS",
        },
        {
          githubUrl: "https://github.com/JustinMattson/CheckPoint2",
          hostName: "GitHub",
          hostUrl: "https://justinmattson.github.io/CheckPoint2",
          img: "lollipop.png",
          name: "The Lollipop Shop",
          stack: "Bootstrap | HTML | CSS",
        },
        {
          githubUrl: "https://github.com/JustinMattson/Checkpoint2-Halfmoon",
          hostName: "GitHub",
          hostUrl: "https://justinmattson.github.io/Checkpoint2-Halfmoon/",
          img: "lollipop-halfmoon.png",
          name: "The Lollipop Shop",
          stack: "Halfmoon | HTML | CSS",
        },
        {
          githubUrl: "https://github.com/JustinMattson/week-1-checkpoint",
          hostName: "GitHub",
          hostUrl: "https://justinmattson.github.io/week-1-checkpoint/",
          img: "siteclone.png",
          name: "Site Clone",
          stack: "HTML | CSS | JS",
        },
        {
          githubUrl: "https://github.com/justinmattson",
          hostName: "GitHub",
          hostUrl: "https://justinmattson.github.io/#/",
          img: "landing.png",
          name: "Landing Page",
          stack: "Vue.js",
        },
        {
          githubUrl: "https://github.com/JustinMattson/todos-react",
          hostName: "GitHub",
          hostUrl: "https://justinmattson.github.io/todos-react/",
          img: "todos-react.png",
          name: "1st React App",
          stack: "React",
        },
        // {
        //   githubUrl: null,
        //   hostName: null,
        //   hostUrl: null,
        //   img: null,
        //   name: null,
        //   stack: null,
        // },
      ],
    };
  },
  components: {
    Skills,
    Applications,
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;500;700&display=swap");
.cursive {
  font-family: "Dancing Script", cursive;
  font-size: 20pt;
}
.bg-image {
  background: url("../assets/img/bwma.jpg") no-repeat center center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  background-attachment: fixed;
}
.bg-happy {
  background: url("../assets/img/IMAG0996_wild_sunflowers.jpg") no-repeat center
    center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  background-attachment: fixed;
}
.portrait {
  min-width: 200px;
  max-height: 400px;
  border-radius: 10px;
  box-shadow: 4px 4px 5px black;
}
</style>

<template>
  <div class="row">
    <div class="col-md-6">
      <SectionRS
        v-for="(section, index) in sections.filter((x) => !x.right)"
        v-bind:section="section"
        v-bind:key="'section-left-' + index"
      />
    </div>
    <div class="col-md-6">
      <SectionRS
        v-for="(section, index) in sections.filter((x) => x.right)"
        v-bind:section="section"
        v-bind:key="'section-right-' + index"
      />
    </div>
  </div>
</template>

<script>
import SectionRS from "./section.vue";

export default {
  name: "BodyRS",
  components: { SectionRS },
  data() {
    return {
      sections: [
        {
          right: false,
          title: "EXPERIENCE",
          items: [
            {
              timeperiod: "08/2022 → CURRENT",
              title: "WEBDEV26",
              descriptions: [
                '<strong>Full Stack Developer</strong> for <u><a target="_blank" href="https://karlbook.com/">Karlbook</a></u> Developing and maintaining a comprehensive booking platform with landing page and management dashboard using Next.js, TypeScript, PostgreSQL, Google Calendar, Stripe integration and more.',
                '<strong>Full Stack Developer</strong> for <u><a target="_blank" href="https://lebateaufrancais.com/">Le Bateau Français</a></u> Developing and maintaining a comprehensive booking platform with landing page and management dashboard using Next.js, TypeScript, PostgreSQL, Google Calendar, Stripe integration and more.',
                '<strong>Full Stack Developer</strong> for <u><a target="_blank" href="https://gallery.artibar.com/fr">Artibar Gallery</a></u> Led the creation of an AI-driven platform featuring two core solutions—an online marketplace for selling and exhibiting art, and a text-to-image AI tool that enables users to generate their own artwork using custom AI models developed by our team.',
                '<strong>Full Stack Developer</strong> for <u><a target="_blank" href="https://furrytag.com/">Furrytag</a></u> Designed and developed a staff dashboard for vets, groomers, and other professionals to manage and update pets information in the AI-powered pet management app.'
              ],
            },
            {
              timeperiod: "08/2019 → 07/2022",
              title: "DATAFLEX",
              descriptions: [
                'Remote Full Stack Developer for <u><a target="_blank" href="https://qrmenu.com/">QRmenu</a></u> <strong>(Angular, AWS Lambda, NodeTs)</strong>.',
                'Remote Full Stack Developer for <u><a target="_blank" href="https://dopweb.com/">Dopweb</a></u> <strong>(Angular, AWS Lambda, NodeTs)</strong>.',
                "Managment & Development of multiple Shopify stores <strong>AlpineJs , Shopify APIs, NodeJs, BOLD API...</strong>.",
                "Making AMP Responsive Templates for a website builder platform.",
                "APIs integration for a website builder platform <strong>(Google Analytic, Search Console, Lighthouse, Google adsense, Stripe, Rank Tracker ...)</strong>.",
              ],
            },
            {
              timeperiod: "2017 → 08/2019",
              title: "SOMAGEC",
              descriptions: [
                "Creation of Intranet Web Applications with <strong>Core.NET</strong> and <strong>Angular</strong>.",
              ],
            },
            {
              timeperiod: 2016,
              title: "Ministry Of Finance",
              descriptions: [
                "Conception and Development of a Management Application.",
                "Creation of <strong>ASP.NET</strong> Web Application Using MVC and Entity Framework.",
              ],
            },
          ],
        },
        // {
        //     right: true,
        //     title: 'PROJECTS',
        //     items: [
        //         {
        //             timeperiod: '2020',
        //             title: '7imyah.com',
        //             descriptions: [
        //                 'Setup and Deploy Website in a <strong>Docker</strong> environment.',
        //                 'Creation of an Interactive Dashboards in <strong>Angular</strong>.',
        //                 'Creation of the web interface with <strong>AMP</strong> technology, <u><a href="http://7imyah.com/">7imyah</a></u>',
        //                 'Creation of the web API with <strong>Node Js</strong>.',
        //                 'Project conception and development using <strong>MEAN</strong> stack.',
        //             ]
        //         }
        //     ]
        // },
        {
          right: false,
          title: "CERTIFICATIONS",
          items: [
            {
              timeperiod: 2016,
              title: "Microsoft® Specialist",
              descriptions: [
                "Microsoft® Specialist: Programming in HTML5 with JavaScript and CSS3.",
              ],
            },
            {
              timeperiod: 2016,
              title: "Microsoft® Specialist",
              descriptions: ["Microsoft® Specialist: Programming in C#."],
            },
          ],
        },
        {
          right: true,
          title: "SKILLS",
          items: [
            {
              title: "Teamwork and autonomy",
              descriptions: ["Git, Slack, Jira, Trello, Asana ..."],
            },
            {
              title: "Technologies",
              descriptions: [
                "AWS services, TypeScript, JavaScript, C#",
                "Redux, Context API",
                "Sentry, CloudWatch, Hotjar, Microsoft Clarity, Google analytics ...",
                "AMP, REST, GraphQL ...",
              ],
            },
            {
              title: "Frameworks",
              descriptions: ["NextJs, Angular, VueJs, AlpineJs, .NET Core, Tailwind, Bootstrap..."],
            },
            {
              title: "Database",
              descriptions: ["PostgreSQL, SQL Server, MongoDB, DynamoDB"],
            },
            {
              title: "DevOps and CI",
              descriptions: ["Docker, AWS CodePipeline, CircleCI, Travis CI"],
            },
            {
              title: "Servers",
              descriptions: ["Windows Server, AWS"],
            },
          ],
        },
        {
          right: true,
          title: "EXPERTISE",
          items: [
            {
              title: "Test Driven Development",
            },
            {
              title: "Rest API Development",
            },
            {
              title: "APIs Integration",
            },
            {
              title: "Shopify Store Development",
            },
            {
              title: "Database Management",
            },
          ],
        },
        {
          right: true,
          title: "STUDIES",
          items: [
            {
              timeperiod: 2022,
              title: "Information Systems Engineering",
              descriptions: [
                "Database administrator.",
                "IS Project Manager.",
                "IS study and development consultant.",
              ],
            },
            {
              timeperiod: 2020,
              title: "Computer System Engineering",
              descriptions: [
                "Mastery of statistical and data analysis methods.",
                "Participate in data engineering project for decision making.",
              ],
            },
            {
              timeperiod: 2016,
              title: "Specialized Technician Diploma",
              descriptions: [
                "Specialized Technician Diploma in Software Development.",
              ],
            },
            {
              timeperiod: 2014,
              title: "Scientific Baccalaureate",
              descriptions: ["High-school Diploma in Maths"],
            },
          ],
        },
      ],
    };
  },
};
</script>

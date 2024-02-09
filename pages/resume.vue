<template>
  <section class="bg-grey-light flex h-full min-h-screen w-full flex-col content-center justify-center text-left font-serif">
    <div class="shadow-material container mx-auto mb-12 mt-24 bg-white p-12 md:w-2/3 print:mt-0 print:w-full print:shadow-none">
      <div id="resume" class="resume-inner w-full">
        <div class="flex items-center">
          <div class="headings flex-grow">
            <h1 class="title text-5xl font-normal text-black no-underline print:text-4xl">Dr. Phillip Hartin</h1>
            <h2 class="name text-grey-dark mt-1 text-xl font-normal tracking-wide text-black">Software Engineer</h2>
          </div>
        </div>

        <!-- Qualifications -->
        <section class="mt-12">
          <div class="title border-b border-grey-light pb-4 text-4xl print:text-2xl">Qualifications</div>
          <div class="list">
            <div class="item mt-10 print:mt-6" v-for="(qualification, index) in qualifications" :key="index">
              <div class="flex items-center">
                <h2 class="title text-2xl font-normal print:text-xl">
                  {{ qualification.title }}
                </h2>
                <div class="flex-grow text-grey-darker text-right font-mono text-sm font-normal print:text-xs">
                  {{ qualification.year }}
                </div>
              </div>
              <div class="text-grey-darker mt-2 text-xl tracking-wide print:mt-1 print:text-base">
                {{ qualification.field }}
              </div>
              <div class="text-grey-dark mt-3 font-serif tracking-wide print:mt-1 print:text-sm">
                {{ qualification.institution }}
              </div>
            </div>
          </div>
        </section>

        <!-- Experience -->
        <section class="mt-12">
          <div class="title border-b border-grey-light pb-4 text-4xl print:text-2xl">Experience</div>
          <div class="list">
            <div class="item mt-10 print:mt-6" v-for="(role, index) in experience" :key="index">
              <div class="flex items-center">
                <h2 class="title text-2xl font-normal print:text-xl">
                  {{ role.title }}
                </h2>
                <div class="flex-grow text-grey-darker text-right font-mono text-sm font-normal print:text-xs">
                  {{ role.dates }}
                </div>
              </div>
              <div class="text-grey-darker mt-2 text-xl tracking-wide print:text-base">
                {{ role.organisation }}
                <span class="text-grey-dark text-lg tracking-wide print:text-base">| {{ role.location }}</span>
              </div>
              <div v-if="role.description" class="text-grey-darkest mt-4 w-2/3 text-base leading-tight tracking-normal print:mt-2 print:text-sm">
                {{ role.description }}
              </div>
            </div>
          </div>
        </section>

        <!-- Projects -->
        <section class="mt-12">
          <div class="title border-b border-grey-light pb-4 text-4xl print:text-2xl">Projects</div>
          <div class="list">
            <div class="item mt-10 print:mt-6" v-for="(project, index) in projects" :key="index">
              <div class="flex items-center">
                <h2 class="title text-2xl font-normal print:text-xl">
                  {{ project.title }}
                </h2>
                <div class="flex-grow text-grey-darker text-right font-mono text-sm font-normal print:text-xs">
                  {{ project.year }}
                </div>
              </div>
              <div class="text-grey-darker mt-2 text-xl tracking-wide print:text-base">
                {{ project.role }}
                <span v-if="project.personal == false" class="text-grey-dark text-lg tracking-wide print:text-sm">| via {{ project.organisation }}</span>
              </div>
              <div class="text-grey-darkest mt-4 w-2/3 leading-tight tracking-normal print:mt-2 print:text-sm">
                {{ project.key_features }}
              </div>
            </div>
          </div>
        </section>

        <!-- Skills -->
        <section class="mt-12">
          <div class="title border-b border-grey-light pb-4 text-4xl print:text-3xl">Skills</div>
          <div class="list">
            <div class="item text-grey-darkest mt-8 text-lg print:mt-6" v-for="(skill, index) in skills" :key="index">
              <span class="text-grey-darker text-sm uppercase tracking-wide print:text-xs">{{ skill.title }} |</span>
              {{ skill.items }}
            </div>
          </div>
        </section>

        <!-- Awards -->
        <section class="mt-12">
          <div class="title border-b border-grey-light pb-4 text-4xl print:text-3xl">Awards</div>
          <div class="list">
            <div class="item mt-6 print:mt-4" v-for="(award, index) in awards" :key="index">
              <div class="flex items-center">
                <h2 class="title text-xl font-normal print:text-lg">
                  {{ award.title }}
                </h2>
                <div class="flex-grow text-grey-darker text-right font-mono text-sm font-normal print:text-xs">
                  {{ award.year }}
                </div>
              </div>
              <div class="text-grey-darker mt-3 font-serif tracking-wide print:mt-1 print:text-sm">
                {{ award.body }}
              </div>
            </div>
          </div>
        </section>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">

    const qualifications =  ref([
          {
            title: "Doctor of Philosophy (PhD)",
            field: "Computer Science",
            year: "2016",
            awards: ["Best Thesis Award", "UCAMI Best Paper Award"],
            institution: "Ulster University"
          },
          {
            title: "Bachelor Degree with First Class Honours (BSc Hons)",
            field: "Computer Science",
            year: "2012",
            awards: [
              "The British Computing Society Medal and Prize",
              "Most Outstanding Student in the Final Honours Year",
              "The I+ Healthcare & Technology Prize"
            ],
            institution: "Ulster University"
          }
        ])
        const experience = ref([
          {
            title: "Lead Developer",
            organisation: "Ply Creative",
            dates: "Jun 2017 - Present",
            description:
              "Leading the architecture, development and operations of commercial web and mobile applications.",
            location: "Brisbane, Australia"
          },
          {
            title: "Senior Developer",
            organisation: "Ply Creative",
            dates: "Jan 2017 - Jun 2017",
            description:
              "Responsible for the development of user centeric web applications, with a focus on API design and front-end implementation.",
            location: "Brisbane, Australia"
          },
          {
            title: "Software Engineer",
            organisation: "Self-Employed",
            dates: "Oct 2015 - Jan 2017",
            description:
              "Full stack development; solutions ranging from CMS/eCommerce development to mobile app development and supporting infrastructure. A specialist focus on software solutions for academic research.",
            location: "Coffs Harbour, Australia"
          },
          {
            title: "Lecturer (Part-Time)",
            organisation: "Ulster University",
            dates: "2014",
            description: "",
            location: "Belfast, United Kingdom"
          },
          {
            title: "Software Engineer & Research Assistant",
            organisation: "Ulster University",
            dates: "2012 - 2015",
            description: "",
            location: "Belfast, United Kingdom"
          },
          {
            title: "Global Markets Trade Floor Infrastructure Analyst",
            organisation: "Citigroup",
            dates: "2010 - 2011",
            description: "",
            location: "Belfast, United Kingdom"
          }
        ])

        const projects = ref([
          {
            title: "Mental Health and Wellness app",
            personal: false,
            organisation: "Ply Creative",
            year: 2018,
            role: "Lead Developer",
            key_features: "iOS/Android/PWA, Push Notifications"
          },
          {
            title: "Healthy Taps app",
            personal: true,
            organisation: "Ulster University",
            year: 2018,
            role: "Solo Developer",
            key_features:
              "iOS/Android/PWA, Behavioural Tracking, RCT, Distributed Architecture"
          },
          {
            title: "VC Funding, Investment and Recruitment Platform",
            personal: false,
            organisation: "Ply Creative",
            year: 2017,
            role: "Lead Developer",
            key_features:
              "Web Platform, Data Engineering, User Analytics, Payment Gateways, Digital Asset Management, Live Chat"
          },
          {
            title: "Financial Planning SaaS",
            personal: false,
            organisation: "Ply Creative",
            year: 2018,
            role: "Lead Developer",
            key_features: "SPA, Financial Modelling with Xero Integration"
          },
          {
            title: "Australia's First Online Ad Marketplace",
            personal: false,
            organisation: "Ply Creative",
            year: 2017,
            role: "Lead Developer",
            key_features:
              "PWA, Marketplace, Facilitating Escrow Payments, Inventory Management"
          },
          {
            title: "Gray Matters app",
            personal: true,
            organisation: "Ulster University",
            year: 2015,
            role: "Solo Developer",
            key_features:
              "Native iOS and Android, Behavioural Tracking and Manipulation, Clinical RCT"
          }
        ])
        const skills = ref([
          {
            title: "Key Skills",
            items:
              "PhD in Machine Learning applications and healthcare, Data Modelling, Software Design"
          },

          {
            title: "Platforms and Tools",
            items:
              "AWS, Firebase, Google Cloud Platform, Weka, Matlab, SPSS+SAS, Forge, Plesk and Docker"
          },
          {
            title: "Frameworks and Languages",
            items:
              "Laravel, Ionic, Angular, Vue, Nuxt, iOS, Android, Firebase, Python, SciPy/NumPy"
          },
          {
            title: "DevOps",
            items:
              "CI/CD Pipeline Development, Automation, Buddy, Travis, PHPUnit, Behat and Laravel Dusk"
          },
          {
            title: "Interpersonal",
            items:
              "Clear communicator, approachable and dependable, highly analytical yet decisive"
          }
        ])

        const awards = ref([
          {
            title: "Best Thesis Award",
            body: "Computer Science Research Institute | Ulster University",
            year: 2017
          },
          {
            title: "AGDA Design Awards - Winner - Digital Design",
            body: "Australian Graphic Design Association",
            year: 2016
          },
          {
            title: "AGDA Design Awards - Finalist - Design for Good",
            body: "Australian Graphic Design Association",
            year: 2016
          },
          {
            title: "UCAMI Best Paper Award",
            body:
              "Ubiquitous Computing and Ambient Intelligence Annual Conference",
            year: 2014
          },
          {
            title: "Most Outstanding Student in the Final Honours Year",
            body: "British Computing Society",
            year: 2012
          },
          {
            title: "The British Computing Society Medal and Prize",
            body: "British Computing Society",
            year: 2012
          },
          {
            title: "The I+ (i-piu, Italy) Healthcare & Technology Prize",
            body: "Ulster University",
            year: 2012
          }
        ])
</script>

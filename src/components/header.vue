<template>
  <div>
    <div id="resume" class="row">
      <div class="col-md-4" id="title">
        <!-- <img src="/src/assets/img/avatar.jpg" layout="responsive" alt="avatar" height="248" width="200" id="avatar"> -->
        <div>
          <img
            id="avatar"
            class="next-particle"
            data-init-position="random"
            data-init-direction="left"
            data-fade-position="left"
            data-fade-direction="left"
            data-particle-gap="1"
            data-width="200"
            data-height="248"
            data-max-width="200"
            data-max-height="248"
            data-mouse-force="80"
            data-gravity="0.06"
            data-noise="20"
            alt="avatar"
            src="/src/assets/img/avatar.jpg"
          />
        </div>
        <h1 class="text-monospace">{{ name.first + " " + name.last }}</h1>
        <p class="text-muted" id="position">
          <span>{{ name.position }}</span>
        </p>
      </div>
      <div class="col-md-8">
        <div class="item-contact">
          <div
            v-for="(item, index) in contact"
            class="text-muted contac link"
            v-bind:class="item.type"
            v-bind:key="index"
          >
            <template v-if="item.link">
              <a :href="item.link">{{ item.value }}</a>
            </template>
            <template v-else>
              <span>{{ item.value }}</span>
            </template>
          </div>
        </div>
      </div>
    </div>
    <div class="row justify-content-center">
      <div class="col-md-6 col-centered">
        <div class="text-muted" id="about">
          {{ name.about }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
function getDateDiff() {
  return 6;
}
export default {
  methods: {
    getDateDiff() {
      return new Date().getUTCFullYear() - 2017;
    },
  },
  name: "HeaderRS",
  data() {
    return {
      name: {
        first: "Hicham",
        middle: "",
        last: "Rabai",
        about: `I'm an experienced full-stack developer who constantly seeks out innovative solutions to everyday problems. I have been working for ${this.getDateDiff()} years, I worked on projects concerning mobile app development and web development and for the moment, I am working as a full-stack developer in a private company.`,
        position: "FULL STACK DEVELOPER",
      },
      contact: [
        { type: "adress", value: "Rabat , Morocco" },
        {
          type: "mail",
          value: "hicham.rabai@outlook.fr",
          link: "mailto:hicham.rabai@outlook.fr",
        },
        {
          type: "github",
          value: "Github.com/hicham4i",
          link: "http://github.com/hicham4i",
        },
      ],
    };
  },
  mounted() {
    let particleScript = document.createElement("script");
    particleScript.setAttribute(
      "src",
      "https://nextparticle.nextco.de/nextparticle.min.js"
    );
    document.head.appendChild(particleScript);
  },
};
</script>

<style scoped>
#resume {
  padding-top: 20px;
}

#avatar {
  /* display: inline-block; */
  /* content: " "; */
  /* background-size: 250px; */
  height: 248px;
  width: 200px;
}
#avatar:hover {
  opacity: 0.25;
}
#title {
  text-align: center;
  line-height: 80%;
}

#position {
  text-align: center;
  text-transform: uppercase;
  position: relative;
}
#position:before {
  border-top: 1px solid #dfdfdf;
  content: "";
  margin: 0 auto;
  position: absolute;
  top: 50%;
  left: 0;
  right: 0;
  bottom: 0;
  width: 90%;
  z-index: -1;
}
#position span {
  background: #fff;
  padding: 0 15px;
}

#about {
  text-align: center;
  padding: 20px 30px 0 30px;
}

.col-centered {
  float: none;
  margin: 0 auto;
}

.text-muted {
  color: #6c757d !important;
  font-size: 13px;
}

.text-muted a,
.text-muted a:hover {
  color: inherit;
}

@media screen and (min-width: 750px) {
  .item-contact {
    padding: 15px 140px;
    text-align: right;
  }

  .item-contact div:after {
    display: inline-block;
    content: " ";
    background-size: 15px;
    height: 15px;
    width: 15px;
    margin-bottom: -3px;
    margin-left: 8px;
  }

  .item-contact .adress:after {
    background-image: url("./../assets/img/adress.svg");
  }
  .item-contact .github:after {
    background-image: url("./../assets/img/github.svg");
  }
  .item-contact .mail:after {
    background-image: url("./../assets/img/mail.svg");
  }
}

@media screen and (max-width: 750px) {
  .item-contact {
    text-align: left;
    padding: 15px 15px;
  }

  .item-contact div:before {
    display: inline-block;
    content: " ";
    background-size: 15px;
    height: 15px;
    width: 15px;
    margin-bottom: -3px;
    margin-right: 8px;
  }

  .item-contact .adress:before {
    background-image: url("./../assets/img/adress.svg");
  }
  .item-contact .github:before {
    background-image: url("./../assets/img/github.svg");
  }
  .item-contact .mail:before {
    background-image: url("./../assets/img/mail.svg");
  }
}
.link {
  padding: 10px 0 0;
}
</style>

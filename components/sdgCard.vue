<template>
  <div
    class="
      our-team
      w-60
      text-center
      relative
      overflow-hidden
    "
  >
    <img :src="imageUrl" alt="profile" class="object-cover" loading="lazy" />
    <div class="team-content">
      <h3 class="title text-lg font-700">
        {{ name }}
      </h3>
      <span class="post block text-md opacity-0 mb-1"> {{ title }} </span>
      <span class="post block text-md opacity-0 mb-4"> {{ company }} </span>
      <ul class="icon">
        <li class="inline-block">
          <a
            aria-label="linkedin"
            target="_blank"
            :href="socialMediaLink"
            class="
              iconify
              border-solid border
              block
              h-8
              text-base
              leading-9
              text-center
              w-8
              rounded-full
              hover:bg-hex-006192 hover:border-hex-006192
            "
            rel="noreferrer"
          >
            <span
              class="iconify m-auto text-xl mt-1"
              data-icon="uim:linkedin-alt"
            ></span>
          </a>
        </li>
        <li class="inline-block">
          <a
            target="_blank"
            aria-label="github"
            :href="githubLink"
            class="
              iconify
              border-solid border
              block
              h-8
              text-base
              leading-9
              text-center
              w-8
              rounded-full
              hover:bg-gray-900 hover:border-gray-900
            "
            rel="noreferrer"
          >
            <span
              class="iconify m-auto text-xl mt-1"
              :data-icon="icon"
            ></span>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    name: {
      type: String,
      default: 'Name'
    },
    title: {
      type: String,
      default: 'Title'
    },
    company: {
      type: String,
      default: ''
    },
    socialMediaLink: {
      type: String,
      default: '#'
    },
    githubLink: {
      type: String,
      default: '#'
    },
    icon: {
      type: String,
      default: 'uim:github-alt'
    },
    imageUrl: {
      type: String,
      default: 'xd',
      required: true
    }
  },
  data () {
    return {}
  }
}
</script>

<style>
.our-team {
  padding: 20px 20px;
  border-radius: 50%;
}
.our-team img {
  transform: scale(1);
  transition: all 1s ease 0s;
}
.our-team:hover img {
  transform: scale(1.2);
}
.our-team .team-content {
  width: 100%;
  height: 100%;
  background: #06508b;
  position: absolute;
  padding-top: 35%;
  color: #fff;
  opacity: 0;
  top: 0;
  left: 0;
  transition: all 0.5s ease-out 0s;
}
.our-team:hover .team-content {
  opacity: 0.8;
}
.our-team .title {
  transform: rotate(-90deg);
  transition: all 0.3s ease-in-out 0.2s;
}
.our-team:hover .title {
  opacity: 1;
  transform: scale(1);
  transition-delay: 0.1s;
}
.our-team .post {
  transform: scale(1.2);
  transition: all 0.3s ease-in-out 0.2s;
}
.our-team:hover .post {
  opacity: 1;
  transform: scale(1);
}

.our-team .icon li a {
  transition: all 0.3s ease 0s;
}
</style>

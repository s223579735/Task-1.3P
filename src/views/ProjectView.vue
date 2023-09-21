<template>
    <div class="projects">
        <div style="margin: auto; width: 50%; margin-bottom: 5px;">
            <h1 class="heading" style="font-size: 24px; margin-bottom: 5px;">Projects I've Done</h1>
            <!-- <p style="font-size: 12px; margin-top: 0; color: rgb(156,163,175);">Lorem ipsum dolor sit amet, consectetur
                adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p> -->
        </div>
        <div style="margin-top: 0px">
            <div style="margin: auto; width: 50%;" v-for="(project, index) in Projects" v-bind:key="index">
                <p class="project-title">{{ project.title }}</p>
                <p class="project-description">{{ project.description }}</p>
            </div>
        </div>
    </div>
</template>

<script>

import ProjectData from '../assets/projects.js'

export default {
    name: 'ProjectView',
    computed: {
        Projects() {
            return ProjectData;
        }
    }
}
</script>

<style>
.projects {
    width: 100%;
    overflow: hidden;
}

.project-title {
    margin-bottom: 0;
    font-size: 20px
}

.project-description {
    margin-top: 0;
    margin-bottom: 40px;
    font-size: 12px
}

@media only screen and (max-device-width: 400px) {

    .project-title {
        font-size: 14px;
    }

    .project-description {
        font-size: 12px;
        margin-bottom: 15vh;
    }
}
</style>
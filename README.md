## PROJECT SUMMARY

### PROJECT INFORMATION

- Project title: Metro Bike Sharing
- Group name: Eureka
- Team members: 
  * Yiran Li - liyiran@usc.edu
  * Xiner Ning - xinernin@usc.edu
  * Yueqin Yang - yueqinya@usc.edu


The original repository can be found in [Here](https://github.com/liyiran/metroBike). We have totally **127** commits. Please check the original repository if you want.
### Work distribution
As a team, we emphosize the teamwork and have team meeting everyweek. During each meeting, we split the chart task into sub tasks and each one takes one sub task. In general, we split the work evenly.


### PROJECT ARTIFACTS

- [Demonstration URL](<http://www-scf.usc.edu/~liyiran/final/>)
- [Presentation PDF](<https://github.com/INF554Fall18/project-eureka/blob/master/final%20presentation/final.pdf>) and [transcript](<https://github.com/INF554Fall18/project-eureka/blob/master/final%20presentation/PRESENTATION_TRANSCRIPT.md>)
- [Article](<https://github.com/INF554Fall18/project-eureka/blob/master/final_paper.pdf>) and [Overleaf URL](<https://www.overleaf.com/read/rsvmqbvvnsgh>)
- [YouTube video](https://youtu.be/hElPSr1pnJY)

### Requirements
- d3 maps : dotmap
- responsive d3 charts: all charts
- interactive d3 charts: all charts
- d3 animated transitions: bar charts, pie chart, waterfall chart
- d3 layouts: line chart, pie chart

### Set-up
For using Vue.js in our project
- Step 1: 
- This command will install vue-cli globally. 
```
npm install -g vue-cli
```
- Step 2:
- The below command pulls a **webpack** template, prompts for some information and generate a project in directory/folder **final**.
```
vue init webpack-simple final
```
- Step 3:
- Change directory to our project folder
```
cd final
```
- Step 4:
- Install all the dependencies required by the template as listed in package.json file. This step may take a minute or two to get all the dependencies.
```
npm install
```
- Step 5:
- This command will start your local http server, open the browser and your default hosted web page will be shown.
```
npm run serve
```

For using bootstrap in our project
```
$ npm install bootstrap@3
```

### Deployment
Use ```vue-cli-service build``` to generate a compiled version of our webside. Then upload the webpage to the aludra server.

### Codebase
We use the Vue as our website's frame. 
For all our code, you can [Click Here](<https://github.com/INF554Fall18/project-eureka/tree/master/final>).
Here is the code in App.vue, which is the entry point of the whole application.
```html
<template>
    <div id="app" class="container-fluid">
        <div id="section1" class="container-fluid">
            <div class="container" style="margin-top: 2%;">
                <div class="row">
                    <div class="col-lg-10 mx-auto">
                        <p>Metro bike usage research</p>
                        <p align="center">Yiran Li</p>
                        <p align="center">Yueqin Yang</p>
                        <p align="center">Xiner Ning</p>
                    </div>
                </div>
            </div>
        </div>
        <nav class="sticky-top navbar navbar-expand-lg navbar-light bg-dark">
            <div class="d-flex flex-column flex-md-row justify-content-between">
                <a class="navbar-brand">
                    <img src="./assets/logo.png" height="30">
                </a>
                <router-link class="nav-item nav-link"  to="/">Index</router-link>
                <router-link class="nav-item nav-link"  to="/general">General</router-link>
                <router-link class="nav-item nav-link"  to="/region">Region</router-link>
            </div>
        </nav>
        <div>
            <router-view></router-view>
        </div>
        <VueElevator :word="word" :duration="duration" :mainAudio="mainAudio" :endAudio="endAudio"></VueElevator>
    </div>
</template>

<script>
    import {VueElevator} from 'vue-elevator'
    export default {
        name: 'app',
        data() {
            return {
                word: "",
                duration: 4000,
                mainAudio: "",
                endAudio: "",
            }
        },
        components: {
            VueElevator
        },
    }
</script>
<style lang="scss">
    @import '../node_modules/bootstrap/scss/bootstrap.scss';
</style>
<style>
    @import '../node_modules/mapbox-gl/dist/mapbox-gl.css';

    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        color: #2c3e50;
    }

    #section1 {
        padding-top: 150px;
        padding-bottom: 100px;
        color: #ffffff;;
        height: 700px;
        background-image: url("./assets/one-tap-account.jpg");
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center center;
        background-attachment: fixed;
        font-weight: 700;
        font-size: 67px;
    }

    #app {
        background-image: url(./assets/background.png)
    }
</style>

```

## Authors
- Yiran Li
- Yueqin Yang 
- Xiner Ning

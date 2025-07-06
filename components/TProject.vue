<script setup>
const props = defineProps({
    project: {
        type: Object,
        required: true,
    },
});
const { project } = props;
</script>

<template>
    <div v-if="project.lang == 'JS'" class="js">
        <table>
            <tbody>
                <tr>
                    <td>
                        <img src="../assets/images/logos--javascript.png" alt="JavaScript" title="JavaScript" class="logo" />
                    </td>
                    <td>
                        <nuxt-link :to="project.url"  class="title">{{ project.name }}</nuxt-link>
                        <br />
                        <span>{{ project.desc }}</span>
                        <br /><br />
                        <nuxt-link :to="`/WhatWhat/${project.details}`" class="see">See</nuxt-link>
                    </td>
                </tr>
                <tr>
                    <td>
                    </td>
                    <td>
                        <span class="type">Type :</span>&nbsp;{{ project.type }}
                        <br />
                        <span class="license">License :</span>&nbsp;{{ project.license }}
                        <br />
                        <span class="category">Category :</span>&nbsp;{{ project.people }}
                        <br />&nbsp;
                    </td>
                </tr>
            </tbody>            
        </table>
    </div>
    <div v-if="project.lang == 'Java'" class="java">
        <table>
            <tbody>
                <tr>
                    <td>
                        <img src="../assets/images/logos--java.png" alt="Java" title="Java" class="logo" style="position: relative; left: 8px;" />
                    </td>
                    <td>
                        <nuxt-link :to="project.url" class="title" style="position: relative; left: 14px;">{{ project.name }}</nuxt-link>
                        <br />
                        <span style="position: relative; left: 14px;">{{ project.desc }}</span>
                        <br /><br />
                        <nuxt-link :to="`/WhatWhat/${project.details}`" class="see" style="position: relative; left: 14px;">See</nuxt-link>
                    </td>
                </tr>
                
                <tr>
                    <td>
                    </td>
                    <td>
                        <span class="type" style="position: relative; left: 14px;">Type :</span>&nbsp;<span style="position: relative; left: 14px;">{{ project.type }}</span>
                        <br />
                        <span class="license" style="position: relative; left: 14px;">License :</span>&nbsp;<span style="position: relative; left: 14px;">{{ project.license }}</span>
                        <br />
                        <span class="category" style="position: relative; left: 14px;">Category :</span>&nbsp;<span style="position: relative; left: 14px;">{{ project.people }}</span>
                        <br />&nbsp;
                    </td>
                </tr>
            </tbody>            
        </table>
    </div>
    <div v-if="project.lang == 'C#'" class="cs">
        <table>
            <tbody>
                <tr>
                    <td>
                        <img src="../assets/images/logos--c-sharp.png" alt="C#" title="C#" class="logo" />
                    </td>
                    <td>
                        <nuxt-link :to="project.url"  class="title">{{ project.name }}</nuxt-link>
                        <br />
                        <span>{{ project.desc }}</span>
                        <br /><br />
                        <nuxt-link :to="`/WhatWhat/${project.details}`" class="see">See</nuxt-link>
                    </td>
                </tr>
                
                <tr>
                    <td>
                    </td>
                    <td>
                        <span class="type">Type :</span>&nbsp;{{ project.type }}
                        <br />
                        <span class="license">License :</span>&nbsp;{{ project.license }}
                        <br />
                        <span class="category">Category :</span>&nbsp;{{ project.people }}
                        <br />&nbsp;
                    </td>
                </tr>
            </tbody>            
        </table>
    </div>
    <div v-if="project.lang == 'Lua'" class="lua">
        <table>
            <tbody>
                <tr>
                    <td>
                        <img src="../assets/images/logos--lua.png" alt="Lua" title="Lua" class="logo" />
                    </td>
                    <td>
                        <nuxt-link :to="project.url"  class="title">{{ project.name }}</nuxt-link>
                        <br />
                        <span>{{ project.desc }}</span>
                        <br /><br />
                        <nuxt-link :to="`/WhatWhat/${project.details}`" class="see">See</nuxt-link>
                    </td>
                </tr>

                <tr>
                    <td>
                    </td>
                    <td>
                        <span class="type">Type :</span>&nbsp;{{ project.type }}
                        <br />
                        <span class="license">License :</span>&nbsp;{{ project.license }}
                        <br />
                        <span class="category">Category :</span>&nbsp;{{ project.people }}
                        <br />&nbsp;
                    </td>
                </tr>
            </tbody>            
        </table>
    </div>
</template>

<style scoped>
div {
    font-family: Open Sans, sans-serif;
    width: 99.7%;
}
a:hover {
    color: crimson;
    text-decoration: none;
}

a:link, a:visited {
    color: currentColor;
    text-decoration: none;
}
.java {
    border-color: brown;
    border-radius: 1rem;
    border-width: 0.1rem;
    border-style: dashed;
    margin-bottom: 0.5rem;
    background-color: rgba(165, 42, 42, 0.15);
}
.lua {
    border-color: blue;
    border-radius: 1rem;
    border-width: 0.1rem;
    border-style: dashed;
    margin-bottom: 0.5rem;
    background-color: rgba(0, 0, 255, 0.15);
}
.cs {
    border-color: green;
    border-radius: 1rem;
    border-width: 0.1rem;
    border-style: dashed;
    margin-bottom: 0.5rem;
    background-color: rgba(0, 128, 0, 0.15);
}
.js {
    border-color: gold;
    border-radius: 1rem;
    border-width: 0.1rem;
    border-style: dashed;
    margin-bottom: 0.5rem;
    background-color: rgba(255, 217, 0, 0.15);
}
.logo {
    padding: 1rem;;
}
.title {
    font-size: larger;
    font-weight: bold;
}
.see {
    font-size: small;
}
.type {
    font-style: italic;
}
.license {
    font-style: italic;
}
.category {
    font-style: italic;
}
.details {
    text-decoration: underline;
    font-weight: bold;
}
</style>
<template>
  <div class="hello">
    <vue-tabs type="pills">
      <v-tab v-for="tab in tabs" :key="tab">
        <div slot="title">
          {{tab}}
        </div>
        <div class="tabContents">
          <User v-for="index in statistics[tab.replace(/\s/g, '')]" :key="index"/>
          <NonUser v-for="i in 1000 - statistics[tab.replace(/\s/g, '')]" :key="i * 50"/>
          <p>
            {{ statistics[tab.replace(/\s/g, '')] }} in 1000 people.
          </p>
        </div>
      </v-tab>
      <v-tab>
        <div slot="title">
          Combined
        </div>
        <Combined :statistics="[statistics]"/>
      </v-tab>
    </vue-tabs>
  </div>
</template>

<script>
import {VueTabs, VTab} from 'vue-nav-tabs'
import 'vue-nav-tabs/themes/vue-tabs.css'
import User from '@/components/User.vue'
import NonUser from '@/components/NonUser.vue'
import Combined from '@/components/Combined.vue'

var data = {
  tabs: ['Disabled', 'Blind', 'Colourblind', 'Illiterate', 'Dyslexic', 'Dyscalculia', 'Learning Disability', 'Disabling Hearing Loss', 'ADHD'],
  statistics: { 
    Disabled: 150,
    Blind: 5, 
    Colourblind: 40, 
    Illiterate: 150, 
    Dyslexic: 100, 
    Dyscalculia: 50, 
    LearningDisability: 20, 
    DisablingHearingLoss: 50, 
    ADHD: 30
  }
}

export default {
  name: 'HelloWorld',
  data: function () {
    return data
  },
  props: {

  },
  components: {
    VueTabs,
    VTab,
    User,
    NonUser,
    Combined
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
  display: flex;
  justify-content: center;
  align-content: center;
  padding: 10px;
}

.tabContents {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  align-content: center;
  padding: 20px;
  width: 750px;
  justify-content: center;
}

.tab-container {
  align-self: center;
  margin: 0;
  display: flex;
  justify-content: center;
}
</style>

<template>
  <div class="combined">
    <div v-for="user in statistics[0]['Blind']" :key="user" class="blind">
        <img src="@/assets/user1.png" alt="Non-disabled User" height="15px" width="15px">
    </div>
    <div v-for="user in statistics[0]['Colourblind']" :key="user" class="colourblind">
        <img src="@/assets/user2.png" alt="Non-disabled User" height="15px" width="15px">
    </div>
    <div v-for="user in statistics[0]['Illiterate']" :key="user" class="illiterate">
        <img src="@/assets/user3.png" alt="Non-disabled User" height="15px" width="15px">
    </div>
    <div v-for="user in statistics[0]['Dyslexic']" :key="user" class="dyslexic">
        <img src="@/assets/user4.png" alt="Non-disabled User" height="15px" width="15px">
    </div>
    <div v-for="user in statistics[0]['Dyscalculia']" :key="user" class="dyscalculia">
        <img src="@/assets/user5.png" alt="Non-disabled User" height="15px" width="15px">
    </div>
    <div v-for="user in statistics[0]['LearningDisability']" :key="user" class="learningdisability">
        <img src="@/assets/user6.png" alt="Non-disabled User" height="15px" width="15px">
    </div>
    <div v-for="user in statistics[0]['DisablingHearingLoss']" :key="user" class="disablinghearingloss">
        <img src="@/assets/user7.png" alt="Non-disabled User" height="15px" width="15px">
    </div>
    <div v-for="user in statistics[0]['ADHD']" :key="user" class="adhd">
        <img src="@/assets/user8.png" alt="Non-disabled User" height="15px" width="15px">
    </div>
    <div v-for="user in 555" :key="user" class="non-disabled">
        <img src="@/assets/user-1.png" alt="Non-disabled User" height="15px" width="15px">
    </div>

    <div class="key">
        <div>
            <img src="@/assets/user1.png" alt="Non-disabled User" height="15px" width="15px"> : Blind
        </div>
        <div>
            <img src="@/assets/user2.png" alt="Non-disabled User" height="15px" width="15px"> : Colourblind
        </div>
        <div>
            <img src="@/assets/user3.png" alt="Non-disabled User" height="15px" width="15px"> : Illiterate
        </div>
        <div>
            <img src="@/assets/user4.png" alt="Non-disabled User" height="15px" width="15px"> : Dyslexic
        </div>
        <div>
            <img src="@/assets/user5.png" alt="Non-disabled User" height="15px" width="15px"> : Dyscalculia
        </div>
        <div>
            <img src="@/assets/user6.png" alt="Non-disabled User" height="15px" width="15px"> : Learning Disability
        </div>
        <div>
            <img src="@/assets/user7.png" alt="Non-disabled User" height="15px" width="15px"> : ADHD
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Combined',
  props: ['statistics']
}
</script>

<style scoped>
.combined {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    width: 750px;
    padding: 20px;
    align-content: center;
    justify-content: center;
}
.key {
    padding: 30px;
    display: flex;
    flex-direction: column;
    text-align: left;
}
</style>

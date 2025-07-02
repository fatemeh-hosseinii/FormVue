<template>
    <form @submit.prevent="submitform" class=" bg-blue-900 flex flex-col justify-center items-center">     
        <p class="text-[34px] text-amber-50">Hiring Form</p>
        <PersonalityInfo/>
        <ExperienceJob/>
        <ExperienceEducation/>
        <BaseButton class="mt-10 rounded-xl"/>

    </form>
</template>
<script>
import PersonalityInfo from './PersonalityInfo/PersonalityInfo.vue';
import BaseButton from "./Modules/BaseButton.vue"
import ExperienceJob from './ExperienceJob/ExperienceJob.vue';
import ExperienceEducation from './ExperienceEducation/ExperienceEducation.vue';
export default{
components:{
    PersonalityInfo,
    ExperienceJob,
    BaseButton,
    ExperienceEducation,
    

}

}

</script>
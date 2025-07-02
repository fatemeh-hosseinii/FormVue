<template>
  <div class="flex flex-col  mt-10 w-[50%]  ">
    <p class="text-2xl text-amber-50">  Experience Education:</p>
    <div class="grid grid-cols-9 gap-5 mt-5 ">
        <div class="col-span-4">
            <BaseInput
            
            label="Grade"
            class="col-span-3"
            placeholder="Enter your Grade"
        />
        </div>
      

    
      <div class="flex flex-col col-span-4">
        <BaseInput
          label="date of education"
          type="number"
          placeholder="Enter your date  "
          
        />
        <p class="mt-2" >{{ Commpany}}</p>

      </div>
     
    </div>

  </div>
</template>

<script>
import BaseInput from '../Modules/BaseInput.vue';
export default {
  components: {
    BaseInput
  },
  data() {
    return {
     Grade:"",
     GradeDate :""
    };
  },
 
};
</script>

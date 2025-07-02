<template>
  <div class="flex flex-col  mt-10 w-[50%]  ">
    <p class="text-2xl text-amber-50">  Experience Job:</p>
    <div class="grid grid-cols-9 gap-5 mt-5 ">
      <BaseInput
        v-model="NameJob"
        label="NameJob"
        class="col-span-3"
        placeholder="Enter your Job"
      />

    
      <div class="flex flex-col col-span-3">
        <BaseInput
          v-model="Commpany"
          label="Commpany"
          type="text"
          placeholder="Enter your password "
          
        />
        <p v-if="Commpany.length>0" class="mt-2" >slm</p>

      </div>
      <BaseInput
        v-model="Date"
        label="Date"
        type="number"
        class="col-span-2"
      />
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
      NameJob: "",
      Commpany: "",
      Date: "",
    };
  },
 
};
</script>

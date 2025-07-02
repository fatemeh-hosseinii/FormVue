<template>
  <div class="flex flex-col w-[50%]">
    <p class="text-2xl text-amber-50">Identity:</p>

    <div class="grid grid-cols-6 gap-5 mt-5 ">
      <!-- Firstname -->
      <div class="flex flex-col col-span-2">
        <BaseInput
          v-model="firstname"
          label="Firstname"
          placeholder="Enter your firstname"
        />
        <p class="text-[red]">{{firstname }}</p>
       
      </div>

      <!-- Lastname -->
      <div class="flex flex-col col-span-2">
        <BaseInput
          v-model="lastname"
          label="Lastname"
          placeholder="Enter your lastname"
        />
        
      </div>

      <!-- Username -->
      <div class="flex flex-col col-span-2">
        <BaseInput
          v-model="username"
          label="Username"
          placeholder="نام کاربری خود را وارد کنید"
        />
        <p>{{ username }}</p>
      </div>

      <!-- Password -->
      <div class="flex flex-col col-span-2">
        <BaseInput
          v-model="password"
          label="Password"
          type="password"
          placeholder="Enter your password"
        />
      </div>

      <!-- BirthDay -->
      <div class="flex flex-col col-span-2">
        <BaseInput
          v-model="birthDay"
          label="BirthDay"
          type="date"
        />
      </div>
    </div>

    <!-- Submit Button -->
    <!--
    <button
      @click="submitForm"
      class="mt-5 px-4 py-2 bg-blue-600 text-white rounded hover:bg-blue-700 w-fit"
    >
      Submit
    </button>
    -->
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
      firstname: "",
      lastname: "",
      username: "",
      password: "",
      birthDay: "",
      errors: {}
    };
  },
  watch: {
    firstname(newVal) {
      console.log("firstname:", newVal);
    }
  }
};
</script>

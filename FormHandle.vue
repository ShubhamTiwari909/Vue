<template>
  <div>
    <form @submit="resetForm">
      <div class="text-slate-200 bg-slate-900 p-6">
        <label for="" class="mx-6 my-8 text-xl font-mono">Name</label>
        <input
          class="text-slate-900"
          type="text"
          id="name"
          v-model.trim.lazy="formValue.Name"
        />
      </div>
      <div class="text-slate-200 bg-slate-900 p-6">
        <label for="" class="mx-6 my-8 text-xl font-mono">Email</label>
        <input
          class="text-slate-900"
          type="text"
          id="email"
          v-model.trim.lazy="formValue.Email"
        />
      </div>
      <div class="text-slate-200 bg-slate-900 p-6">
        <label for="" class="mx-6 my-8 text-xl font-mono">Post</label>
        <input
          class="text-slate-900"
          type="text"
          id="post"
          v-model.trim.lazy="formValue.Post"
        />
      </div>
      <div class="text-slate-200 bg-slate-900 p-6">
        <label for="" class="mx-6 my-8 text-xl font-mono">Job Location</label>
        <select
          id="location"
          class="text-slate-800"
          multiple
          v-model.trim.lazy="formValue.JobLocation"
        >
          <option value="">--</option>
          <option value="Chennai">Chennai</option>
          <option value="Bengaluru">Bengaluru</option>
          <option value="Hydrabad">Hydrabad</option>
          <option value="Delhi">Delhi</option>
        </select>
      </div>
       <div class="text-slate-200 bg-slate-900 p-6">
        <label for="" class="mx-6 my-8 text-xl font-mono">Skills</label>
        HTML :<input
          class="mx-5"
          type="checkbox"
          id="skill"
          v-model.trim.lazy="formValue.Skills"
          value="HTML"
        />
        CSS:
        <input
          class="mx-5"
          type="checkbox"
          id="skill"
          v-model.trim.lazy="formValue.Skills"
          value="CSS"
        />
         JAVASCRIPT :<input
          class="mx-5"
          type="checkbox"
          id="skill"
          v-model.trim.lazy="formValue.Skills"
          value="JAVASCRIPT"
        />
        TAILWIND:
        <input
          class="mx-5"
          type="checkbox"
          id="skill"
          v-model.trim.lazy="formValue.Skills"
          value="TAILWIND"
        />
      </div>
      <div class="text-slate-200 bg-slate-900 p-6">
        <label for="" class="mx-6 my-8 text-xl font-mono">Gender</label>
        Male :<input
          class="mx-5"
          type="radio"
          id="gender"
          v-model.trim.lazy="formValue.Gender"
          value="male"
        />
        Female:
        <input
          class="mx-5"
          type="radio"
          id="gender"
          v-model.trim.lazy="formValue.Gender"
          value="female"
        />
      </div>
      <div class="text-slate-200 bg-slate-900 p-6">
        <label class="mx-6 my-8 text-xl font-mono" for="">Age</label>
        <input
          class="text-slate-900"
          type="number"
          id="age"
          v-model.number="formValue.Age"
        />
      </div>
      <div class="text-slate-200 bg-slate-900 p-6">
        <label for="" class="mx-6 my-8 text-xl font-mono">About You</label>
        <textarea
          class="text-slate-900 text-semibold"
          id="summary"
          v-model.trim.lazy="formValue.AboutYou"
        ></textarea>
      </div>
      <button
        class="bg-slate-800 text-slate-200 px-5 py-3 rounded-md"
        type="submit"
      >
        Submit
      </button>
    </form>
    <div>
      {{ JSON.stringify(formValue, null, 2) }}
    </div>
  </div>

  <!-- .trim,.trim.lazy,.number are directives -->
</template>

<script>
export default {
  name: "FormHandle",
  data() {
    return {
      formValue: {
        Name: "",
        Email: "",
        Post: "",
        JobLocation: [],
        Skills : [],
        Gender: "",
        AboutYou: "",
        Age: "",
      },
    };
  },
  methods: {
    resetForm() {
      console.log(this.formValue);
    },
  },
};
</script>

<style></style>

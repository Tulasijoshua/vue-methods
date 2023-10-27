<template>
  <div >
    <div>
      <pre>
        {{ JSON.stringify(formValues, null, 2) }}
      </pre>
    </div>
    <div>
      <div>
        <label>Name</label>
        <input type="text" id="name" v-model="formValues.name">
      </div>
      <div>
        <label for="summary">Profile summary</label>
        <textarea id="summary" v-model="formValues.summary"></textarea>
      </div>
      <div for="country">Country</div>
      <select id="country" v-model="formValues.country">
        <option value="">Select country</option>
        <option value="Ghana">Ghana</option>
        <option value="Ghana">Germany</option>
        <option value="USA">USA</option>
        <option value="England">England</option>
      </select>
    </div>
    <div>
      <label for="jobLocation">Job Location</label>
      <select id="jobLocation" multiple v-model="formValues.jobLocation">
        <option value="">Select Location</option>
        <option value="Ghana">Ghana</option>
        <option value="USA">USA</option>
        <option value="Remote">Remote</option>
      </select>
    </div>
    <div>
      <input id="remote" type="checkbox" v-model="formValues.remote" true-value="yes" false-value="no" />
      <label>Open to Remote work?</label>
    </div>
    <div>
      <h3>Skill set</h3>
      <input type="checkbox" id="html" value="html" v-model="formValues.skillSet" />
      <label for="html">HTML</label>
      <input type="checkbox" id="css" value="css" v-model="formValues.skillSet" />
      <label for="css">CSS</label>
      <input type="checkbox" id="javascript" value="javascript" v-model="formValues.skillSet" />
      <label for="javascript">JavaScript</label>
    </div>
    <div>
      <h3>Year of Experience</h3>
      <input type="radio" id="0-2" value="0-2" v-model="formValues.yearsOfExperience">
      <label for="0-2">0 - 2</label>
      <input type="radio" id="3-5" value="3-5" v-model="formValues.yearsOfExperience">
      <label for="3-5">3 - 5</label>
      <input type="radio" id="6-9" value="6-9" v-model="formValues.yearsOfExperience">
      <label for="0-2">6 - 9</label>
      <input type="radio" id="10+" value="10+" v-model="formValues.yearsOfExperience">
      <label for="10+">10+</label>
    </div>
    <div>
      <label for="age"></label>
      <input type="number" id="age" v-model="formValues.age" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formValues: {
        name: '',
        summary: '',
        country: '',
        jobLocation: [],
        remote: 'no',
        skillSet: [],
        yearsOfExperience: '',
        age: null,
      }
    }
  }
}
</script>

<style>
  .marTop {
    margin-top: 5rem;
  }
</style>. 
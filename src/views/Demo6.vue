<template>
  <div id="demo6">
      <h1>Form</h1>
      <!--<form v-on:submit.prevent="submit">-->
      <form v-on:submit="submit">
      <div>
          <label for="first_name">Firstname:</label>
          <input type="text" name="first_name" v-model.trim="applicant.first_name">
          </div>
          <div>
          <label for="last_name">Lastname:</label>
          <input type="text" name="last_name" v-model="applicant.last_name">
          </div>
          <div>
          <label for="sex">Male</label>
          <input type="radio" name="sex" value='male' v-model="applicant.sex">
          <label for="sex">Female</label>
          <input type="radio" name="sex" value='female' v-model="applicant.sex">
          </div>
            <div>
                <label for="age">Age:</label>
                <input type="number" v-model.number="applicant.age">
            </div>

           <div>
              <select name="courses" v-model="applicant.course">
                  <option value="react">React</option>
                  <option value="angular">Angular</option>
                  <option value="vuejs">Vue</option>
              </select>
          </div>
          <button type="button" @click.exact="clear" @click.alt="useDefault">Clear</button>
          <button type="submit">Submit</button>
      </form>
      <div>#spy {{JSON.stringify(applicant)}}</div>
  </div>
</template>

<script>
export default {
    name: 'demo6',
    data () {
        return {
            applicant: {
                first_name: '',
                last_name: '',
                sex: 'male',
                course: 'vue',
                age: 0
            }
        }
    },
    methods: {
        submit (event) {
            event.preventDefault()
            alert(JSON.stringify(this.applicant))
        },
        clear () {
            this.applicant = {
                first_name: '',
                last_name: '',
                sex: 'female',
                course: 'react',
                 age: 0
            }
        },
         useDefault () {
            this.applicant = {
                first_name: 'NoName',
                last_name: 'NoName',
                sex: 'male',
                course: 'vue',
                age: 20
            }
        }
    }
}
</script>

<style>

</style>

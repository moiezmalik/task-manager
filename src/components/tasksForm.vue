<template>
  <form id="form" @submit="onSubmit">
    <div class="row mt-3">
      <div class="col-sm-2">
        <label for="title" class="control-label">Title</label>
      </div>
      <div class="col-sm-10">
        <input type="text" v-model="title" id="title" class="form-control" />
      </div>
    </div>
    <div class="row mt-3">
      <div class="col-sm-2">
        <label for="description" class="control-label">Description</label>
      </div>
      <div class="col-sm-10">
        <input type="text" v-model="description" id="description" class="form-control" />
      </div>
      <div class="row mt-3">
        <div class="col-sm-2">
            <label for="reminder" class="control-label">Reminder</label>
        </div>
        <div class="col-sm-10">
          <input type="checkbox" v-model="reminder" id="reminder" class="form-box" />
      </div>
      </div>
    </div>
    <div class="row">
      <div class="col-sm-10 offset-sm-2">
        <div class="d-grid gap-2 mt-3">
          <input
            type="submit"
            class="btn btn-primary btn-large"
            value="Submit"
          />
        </div>
      </div>
    </div>
  </form>
</template>

<script>
export default {
  name: "TaskForm",
  data(){
    return {
      id: 0,
      title: '',
      description: '',
      reminder: false
    }
  },
  methods:{
    onSubmit(e){
      e.preventDefault()
      this.id++;
      const formData = {
        id: this.id,
        title: this.title,
        description: this.description,
        reminder: this.reminder
      }
      this.$emit('form-data', formData);

      this.title = '',
      this.description = '',
      this.reminder = false
    }
  },
  props: {
      tasks: Array
  }
};
</script>

<style scoped>
.btn-primary{
    background: #42b983;
    border: #42b983;
}
.btn-primary:hover{
    background: green;
    border: green;
}
</style>
<template>
  <form id="form" action="submit">
    <div class="row mt-3">
      <div class="col-sm-2">
        <label for="title" class="control-label">Title</label>
      </div>
      <div class="col-sm-10">
        <input type="text" id="title" class="form-control" />
      </div>
    </div>
    <div class="row mt-3">
      <div class="col-sm-2">
        <label for="description" class="control-label">Description</label>
      </div>
      <div class="col-sm-10">
        <input type="text" id="description" class="form-control" />
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
<template>
  <div class="project">
      <div class="actions">
          <h3 @click="showDetails = !showDetails">{{ project.title }}</h3>
          <div class="icons">
              <span class="material-icons-outlined"> <i class="fas fa-pen"> </i> </span>
              <span class="material-icons-outlined"> <i class="fas fa-trash"> </i> </span>
              <span class="material-icons-outlined"> <i class="fas fa-check"> </i> </span>
          </div>
      </div>
      <div v-if="showDetails" class="details">
          <p>{{ project.details }}</p>
      </div>
  </div>
</template>

<script>
export default {
    props: ['project'],
    //this is to toggle hiding of info
    data() {
        return {
            showDetails: false
        }
    }
}
</script>

<style>
.project {
    margin: 20px auto;
    background: white;
    padding: 10px 20px;
    border-radius: 4px;
    box-shadow: 1px 2px 3px rgba(0, 0, 0, 0.05);
    border-left: 4px solid #e90074;
}
h3 {
    cursor: pointer;
}
.actions {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.material-icons-outlined {
    font-size: 24px;
    margin-left: 10px;
    color: #ddd;
    cursor: pointer;
}
.material-icons-outlined:hover{
    color: #777;
}

</style>
<template>
  <div class="my-5">
    <div class="">
      <div >
        <div
          class="card-header d-flex justify-content-between align-item-center"
        >
          <h2 class="mb-0"><span><i class="mdi mdi-certificate"></i></span> CREATE CATEGORY FORM</h2>
<router-link class="text-light btn btn-icon btn-primary text-center " style="width:180px; padding:12px" :to="{path:'/categories'}">
       <span> <i class="mdi mdi-border-all"></i> </span> ALL CATEGORY
      </router-link>
        </div>

        <div class="card">
          <div class="card-body">
            <form @submit.prevent="add_category" class="forms-sample">
              <div class="form-group">
                <label for="exampleInputName1"
                  >Create New Category Name <span class="text-danger">*</span>
                </label>
                <input
                v-model="form.name"
                name="fname"
                  type="text"
                  class="form-control"
                  id="exampleInputName1"
                  placeholder="Name"
                />
              </div>




              <button type="submit" class="btn btn-gradient-primary mr-2">
               <span> <i class="mdi mdi-checkbox-marked"></i></span> CREATE NEW CATEGORY
              </button>
            </form>
          </div>
        </div>
      </div>
      <!--end of create category -->


    </div>
  </div>
</template>

<script>
import Form from 'vform'
import axios from 'axios';
export default {
  data: () => ({
    form: new Form({
      name: '',
    })
  }),
  methods:{
    add_category(){
      this.form.post('category/store').then(response =>{
        console.log(response.data)
        this.$router.push('/categories');
      })

    }
  }
};
</script>

<style>
</style>










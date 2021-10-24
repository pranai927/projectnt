<template>
  <div class="container">
   <div class="row">
    <form>
      <div class="form-group">
        <label for="firstname" class="form-label">First Name:</label>
        <input type="text" lass="form-control" id="firstname" v-model="firstname" />
      </div>
      <div class="form-group">
        <label for="lastname" class="form-label">Last Name:</label>
        <input type="text" class="form-control" id="lastname" v-model="lastname"/>
      </div>
      <div class="form-group">
        <label for="DOB" class="form-label">DOB:</label>
        <input type="text" class="form-control" id="DOB" v-model="DOB" />
      </div>
      <div class="radiobutton">
        <label class="sr-only">Gender:</label>
        <label><input type="checkbox" /> Male</label>
        <label><input type="checkbox" /> Female</label>
      </div>
      <div class="form-group">
        <label class="sr-only">City:</label>
        <select class="custom-select mr-sm-2" id="inlineFormCustomSelect">
          <option selected>Choose...</option>
          <option value="1">Mumbai</option>
          <option value="2">Pune</option>
          <option value="3">Banglore</option>
        </select>
      </div>
      <div class="form-group">
        <label class="sr-only">Description:</label>
        <textarea
          class="form-control"
          id="exampleFormControlTextarea4"
          rows="3"
          v-model="Description"
        ></textarea>
      </div>
      <div class="form-group">
        <label class="sr-only">Address:</label>
        <textarea
          class="form-control"
          id="exampleFormControlTextarea4"
          rows="3"
          v-model="address"
        ></textarea>
      </div>
      <button type="submit" class="btn btn-dark">Submit</button>
    </form>
  
 
   
  </div>
 </div>
</template>

<script>
export default {
  name: "FormComponent",
  props: {
    msg: String,
  },
 data() {
  return {
    
  };
}
};
</script>

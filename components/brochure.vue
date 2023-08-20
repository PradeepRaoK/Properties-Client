<template>
  <div class="brochure" id="contact" :style="{backgroundColor:$vuetify.theme.themes.myTheme.colors.tertiary}">
    <v-text style="font-size: 32px; font-weight: 700;">Interested in the property?</v-text>
    <v-text style="font-size: 16px; font-weight: 400;">Download the brochure using the link below</v-text>
    <v-btn @click="showModal = true" prepend-icon="$vuetify" rounded="xl" size="x-large" class="download-btn"> Download Brochure</v-btn>
    
    <v-dialog v-model="showModal" max-width="600">
      <v-card>
        <v-card-title class="modal-title">
          Fill in your details
        </v-card-title>
        <v-card-text>
          <v-form ref="form">
            <div class="modal-row">
              <v-text-field v-model="name" label="Name"></v-text-field>
              <v-text-field v-model="number" label="Number"></v-text-field>
            </div>
            <v-text-field v-model="email" label="Email"></v-text-field>
          </v-form>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn @click="submitForm" color="tertiary2">Submit</v-btn>
          <v-btn @click="showModal = false" color="tertiary2">Cancel</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showModal: false,
      name: '',
      number: '',
      email: ''
    }
  },
  methods: {
    submitForm() {
      this.$refs.form.validate();
      // submit form data
      this.showModal = false;
    }
  }
}
</script>

<style>
.brochure {
  height: 40%;
  text-align: center;
  color: #FFFFFF;
  padding: 100px;
  display: flex;
  flex-direction: column;
  gap: 40px;
}
.download-btn {
  margin: auto;
  margin-top: 30px;
}
@media (max-width: 430px) {
  .download-btn {
    font-size: 16px;
    width: 310px;
  }
  .brochure{
    padding: 40px;
  }
}
.modal-row {
  display: flex;
  flex-direction: row;
  gap: 20px;
}
.modal-title {
  text-align: center;
}
</style>

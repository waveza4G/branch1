// <q-form ref="myForm">

setup () {
  const myForm = ref(null)

  function validate () {
    myForm.value.validate().then(success => {
      if (success) {
        // yay, models are correct
      }
      else {
        // oh no, user has filled in
        // at least one invalid value
      }
    })
  }

  // to reset validations:
  function reset () {
    myForm.value.resetValidation()
  }

  return {
    myForm,
    // ...
  }
}
<script setup>
defineOptions({
  name: 'App'
});
</script>

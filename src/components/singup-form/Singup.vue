<template src="./Singup.html"></template>

<script>

  import {mapState} from 'vuex';

  export default {
    data() {
      return {
        name: '',
        email: '',
        position: '',
        expertise: '',
        reason: '',
        response: '',
      };
    },
    name: "Singup",
    computed: {
    },
    methods: {
      validateBeforeSubmit() {
        this.$validator.validateAll().then((result) => {
          if (result) {
            this.getFormValues();
            return;
          }
          this.responseStatus(result);
        });
      },
      getFormValues() {
        this.$http.post('http://httpbin.org/post/', {
          name: this.name,
          email: this.email,
          position: this.position,
          expertise: this.expertise,
          reason: this.reason,
        })
          .then((response) => {
            this.responseStatus(response.body.status);
          }, (error) => {});
      },
      responseStatus(value) {
        if (value) {
          this.response = 'success';
        } else {
          this.response = 'error';
        }
        setTimeout(() => {
          this.response = '';
        }, 3000);
      },
    },
    mounted() {
    },
    components: {
    },
  }
</script>

<style src="./Singup.scss" lang="scss"></style>

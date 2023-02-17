<script>
import emailjs from 'emailjs-com';
import useValidate from '@vuelidate/core'
import {required, email} from '@vuelidate/validators'
import {reactive, computed} from 'vue'

export default{
    data(){
        const state = reactive({
            email: '',
            name: '',
            subject: '',
            message: '',
        })
        
        const rules = computed(() => {
            return {
                email: { required, email },
                name: { required },
                subject: { required },
                message: { required },
            }
        })
        
        const v$ = useValidate(rules, state)

        return{
            state,
            v$,
            submitStatus: null
        }
    },
    methods: {
        submitForm() {
            this.v$.$touch()
            if (this.v$.$error) {
                this.submitStatus = 'ERROR'
            } else {
                this.submitStatus = 'PENDING'
                emailjs.sendForm('service_xgu0af9', 'template_92jwz3n', this.$refs.form, 'r5dMtbjK3ir0VDD2v')
                .then(() => {
                    this.submitStatus = 'OK'
                }, () => {
                    this.submitStatus = 'FAILED'
                });
            }
        }
    },
   
}
</script>
<template>
    <div class="main-cont-c">
        <div class="container root">
            <h2>CONTACTANOS</h2>
            <form ref="form">
                <p>
                    <input 
                    type="text" 
                    :class="v$.name.$error ? 'input-err' : 'input'" 
                    name="from_name" 
                    v-model="state.name" 
                    placeholder="Nombre" 
                    autocomplete="off"
                    @blur="this.v$.$validate()">

                    <span v-if="v$.name.$error"> {{ v$.name.$errors[0].$message }}*</span>
                </p>
                <p>
                    <input 
                    type="email" 
                    name="user_email"
                    :class="v$.email.$error ? 'input-err' : 'input'" 
                    placeholder="Correo" 
                    @keydown.space.prevent 
                    v-model="state.email"
                    autocomplete="off"
                    @blur="this.v$.$validate()">

                    <span v-if="v$.email.$error"> {{ v$.email.$errors[0].$message }}*</span>
                </p>
                <p>
                    <input 
                    type="text" 
                    :class="v$.subject.$error ? 'input-err' : 'input'" 
                    name="subject" 
                    v-model="state.subject" 
                    placeholder="Asunto" 
                    @blur="this.v$.$validate()">

                    <span v-if="v$.subject.$error"> {{ v$.subject.$errors[0].$message }}*</span>
                </p>
                <p>
                    <input 
                    type="text" 
                    :class="v$.message.$error ? 'input-err' : 'input'" 
                    name="message" 
                    v-model="state.message" 
                    placeholder="Mensaje" 
                    @blur="this.v$.$validate()">

                    <span v-if="v$.message.$error"> {{ v$.message.$errors[0].$message }}*</span>
                </p>

                <button @click.prevent="submitForm" class="orange-btn"  :disabled="submitStatus === 'PENDING'">ENVIAR</button>
                <p class="typo__p" v-if="submitStatus === 'OK'" style="color: green;">Gracias por contactarnos</p>
                <p class="typo__p" v-if="submitStatus === 'ERROR'">Por favor complete el formulario correctamente</p>
                <p class="typo__p" v-if="submitStatus === 'PENDING'">Enviando...</p>
                <p class="typo__p" v-if="submitStatus === 'FAILED'" style="color: red;">Algo falló</p>
            </form>
        </div>
    </div>
</template>

<style lang="css" scoped>
.orange-btn{
    color: #ffffff;
    background-color: #F26800 ;
    border: none;
    padding: 10px 20px 10px 20px;
    margin-top: 10px;
    margin-bottom: 20px;
    font-weight: bold;
}
span{
    color: red;
}
.main-cont-c{
    background-color: #1f1e29;
    display: grid;
    place-items: center;
    padding-top: 100px;
    padding-bottom: 100px;
}
.root {
  background-color: #ffffff;
  box-shadow: silver;
  padding: 30px;
  text-align: center;
  width: 50%;
}
.input {
  outline: none;
  border: none;
  border-radius: 20px;
  border: 2px solid rgba(128, 128, 128, 0.11);
  font-size: 1em;
  padding: 5px 0 5px 10px;
  margin: 10px 0 5px 0;
  width: 100%;
}
.input-err{
  outline: none;
  border: none;
  border-radius: 20px;
  border: 2px solid rgb(255, 0, 0);
  font-size: 1em;
  padding: 5px 0 5px 10px;
  margin: 10px 0 5px 0;
  width: 100%;
}

@media screen and (max-width: 1000px){
    .root {
    background-color: #ffffff;
    box-shadow: silver;
    padding: 30px;
    text-align: center;
    width: 70%;
    }
}

@media screen and (max-width: 700px){
    .root {
    background-color: #ffffff;
    box-shadow: silver;
    padding: 30px;
    text-align: center;
    width: 90%;
    }
}

@media screen and (max-width: 700px){
    .root {
    background-color: #ffffff;
    box-shadow: silver;
    padding: 30px;
    text-align: center;
    width: 80%;
    }
}
</style>
<!-- <script>
import emailjs from 'emailjs-com';
// import {ref} from 'vue';
// import useFormValidation from '../modules/useFormValidation'
// import useSubmitButtonState from '../modules/UseSubmitButtonState'

export default {
  data() {
    return {
      successMessage: false,
      failedMessage: false
    };
  },
  // setup(){
  //   let fName = ref("");
  //   let fEmail = ref("");
  //   let fSubject = ref("");
  //   let fMessage = ref("");
  //   const { validateNameField, validateEmailField, validateSubjectField, validateMessageField, errors } = useFormValidation();

  //   const validateInput = () => {
  //     validateNameField("name", fName.value);
  //     validateEmailField("email", fEmail.value);
  //     validateSubjectField("subject", fSubject.value);
  //     validateMessageField("message", fMessage.value);
  //   };

  //   const { isSignupButtonDisabled } = useSubmitButtonState(errors);

  //   return{
  //     fName,
  //     fEmail,
  //     fSubject,
  //     fMessage,
  //     errors,
  //     validateInput,
  //     isSignupButtonDisabled
  //   };

  // },
  methods: {
    sendEmail() {
      emailjs.sendForm('service_xgu0af9', 'template_92jwz3n', this.$refs.form, 'r5dMtbjK3ir0VDD2v')
        .then(() => {
            this.successMessage = true;
        }, () => {
            this.failedMessage = true;
        });
    },
    closeSuccessMessage() {
      this.successMessage = false;
    },
    closeFailedMessage(){
      this.failedMessage = false;
    }
  }

  
}

</script>
<template>
    <div style="padding-top: 10px; height:; background-color: #29291e;">
      
        <div id="contact-form" class="contact-form">
            <h1 class="contact-form_title">{{ $t("contact.title") }}</h1>
            <div class="separator"></div>
            <form class="form" ref="form" >
                <input  name="from_name" v-bind:placeholder="$t('contact.ph-name')" type="text" autocomplete="off" v-model.trim="fName" @keyup="validateInput" @blur="validateInput">
                <div class="pointing" v-if="errors.name">
                  {{ errors.name }}
                </div>
                <input  name="user_email" v-bind:placeholder="$t('contact.ph-email')" type="email" autocomplete="off" v-model="fEmail"  @keydown.space.prevent @keyup="validateInput" @blur="validateInput">
                <div class="pointing " v-if="errors.email">
                  {{ errors.email }}
                </div>
                <input  name="subject" v-bind:placeholder="$t('contact.ph-subject')" type="text" autocomplete="off" v-model="fSubject" @keyup="validateInput" @blur="validateInput">
                <div class="pointing " v-if="errors.subject">
                  {{ errors.subject }}
                </div>
                <textarea  name="message" rows="4" v-bind:placeholder="$t('contact.ph-message')" v-model="fMessage" @keyup="validateInput" @blur="validateInput"></textarea>
                <div class="pointing" v-if="errors.message">
                  {{ errors.message }}
                </div>
            <button class="button" @click.prevent="sendEmail" :class="isSignupButtonDisabled ? 'unavailable-btn' : 'available-btn' " :disabled="isSignupButtonDisabled" @keyup="validateInput" @blur="validateInput">{{$t("contact.send-btn")}}</button>
            </form>
        </div>

        <transition name="message">
          <div v-if="successMessage" class="message-container">
            <div class="message">
              <h2 style="color: green;">{{ $t("contact.transition-s.header") }}</h2>
              <img src="../img/success.png">
              <p>{{ $t("contact.transition-s.t") }}</p>
              <button @click="closeSuccessMessage">{{ $t("contact.transition-s.btn") }}</button>
            </div>
          </div>
        </transition>
        
        <transition name="message">
          <div v-if="failedMessage" class="message-container">
            <div class="message">
              <h2 style="color: red;">{{ $t("contact.transition-f.header") }}</h2>
              <img src="../img/failed.png">
              <p>{{ $t("contact.transition-f.t") }}</p>
              <button @click="closeFailedMessage">{{ $t("contact.transition-f.btn") }}</button>
            </div>
          </div>
        </transition>

    </div>
</template>
<style scoped>
.message-container {
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0,0,0,0.8);
  z-index: 1000;
}

.message {
  background-color: #fff;
  padding: 20px;
  border: 3px solid #F26800;
  border-radius: 10px;
  box-shadow: 0px 0px 3px #888;
  color: #000;
  text-align: center;
  width: 500px;
  max-width: 95%;
  margin: 0 auto;
}

.message h2 {
  font-size: 24px;
  margin-bottom: 20px;
  font-weight: bold;
}

.message p {
  font-size: 18px;
  margin-bottom: 30px;
  margin-top: 20px;
}
.message button {
  padding: 10px 20px;
  background-color: #29291e;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 18px;
}

.contact-form {
  color: white;
  text-align: center;
	margin:auto;
	width: 70%;
    padding: 30px 0 30px 0;
}

.contact-form .separator {
	border-bottom: solid 1px #ccc;
	margin-bottom: 15px;
}

.contact-form .form {
	display: flex;
	flex-direction: column;
	font-size: 16px;
}

.contact-form_title {
	font-size: 28px;
  margin-top: 20px;
}

.contact-form input[type="email"],
.contact-form input[type="text"],
.contact-form textarea {
  padding: 12px 20px;
  margin: 8px 0;
  box-sizing: border-box;
  border: none;
  border-bottom: 1px solid rgb(190, 190, 190);
  outline: none;
  background-color: rgb(238, 238, 238);
}

::placeholder {
  color: rgb(70, 70, 70);
  opacity: 1; /* Firefox */
}

:-ms-input-placeholder { /* Internet Explorer 10-11 */
 color: rgb(70, 70, 70);
}

::-ms-input-placeholder { /* Microsoft Edge */
 color: rgb(70, 70, 70);
}

.contact-form textarea {
	resize: none;
}

.contact-form .button {
  margin-top: 10px;
	border: none;
	color: white;
	cursor: pointer;
	padding: 10px 50px;
	text-align: center;
	text-transform: uppercase;
}

.unavailable-btn{
  background-color: gray;
}

.available-btn{
  background: #F26800;
}
.available-btn:hover{
  transform: scale(1.01);
}
.pointing{
  text-align: center;
  color: red;
  text-transform: uppercase;
  width: fit-content;
  padding: 0 10px 0 10px;
}

</style> -->
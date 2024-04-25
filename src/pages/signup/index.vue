<!-- eslint-disable vue/multi-word-component-names -->
<template lang="">
    <div class="container mt-4">
        <main>
 
            <div class="row g-5">
            
            <div class="col-md-7 col-lg-8">
                <form class="needs-validation" novalidate>
                <div class="row g-3">
                    <div class="col-12">
                        <label for="name" class="form-label">Name</label>
                        <input type="text" class="form-control" id="name" v-model="form.name">
                       
                    </div>
                    <div class="col-12">
                        <label for="email" class="form-label">Email</label>
                        <input type="email" class="form-control" id="email" placeholder="you@example.com" v-model="form.email">
                        <div class="invalid-feedback">
                            Please enter a valid email address for shipping updates.
                        </div>
                    </div>
                    <div class="col-12">
                        <label for="password" class="form-label">PASSWORD</label>
                        <input type="password" class="form-control" id="password" placeholder="********" v-model="form.password">
                      
                    </div>
                    <div class="col-12">
                        <label for="password" class="form-label">Confirm PASSWORD</label>
                        <input type="password" class="form-control" id="password" placeholder="********" v-model="form.passwordConfirm">
                      
                    </div>
                </div>

                <hr class="my-4">

                <a class="w-100 btn btn-primary btn-lg" @click="onSubmit">Login</a>
                </form>
            </div>
            </div>
        </main>
    </div>
</template>
<script>
import axios from 'axios';

export default{
    setup(){
        return {
            form : {
                email : '',
                password: '',
                passwordConfirm: '',
                name:''
            }
        }
    },
    methods : {
         async onSubmit() {
            
            try{
                const response = await axios.post("http://localhost:3000/auth/signup", {
                    email: this.form.email,
                    password: this.form.password,
                    name: this.form.name
                });
                console.log(response);
            }catch(err){
                console.log(err);
            }
        }
    }
}
</script>
<style lang="">
    
</style>
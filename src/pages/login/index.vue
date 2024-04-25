<!-- eslint-disable vue/multi-word-component-names -->
<template lang="">
    <div class="container mt-4">
        <main>
 
            <div class="row g-5">
            
            <div class="col-md-7 col-lg-8">
                <form class="needs-validation" novalidate>
                <div class="row g-3">
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
                </div>

                <hr class="my-4">

                <button class="w-100 btn btn-primary btn-lg" type="submit">Login</button>
                </form>
            </div>
            </div>
        </main>
    </div>
</template>
<script>
export default{
    setup(){
        return {
            form : {
                email : '',
                password: ''
            }
        }
    },
    methods : {
        onSubmit() {

        }
    }
}
</script>
<style lang="">
    
</style>
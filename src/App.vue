<template>
    <div class="container">
        <form v-if="!submitted">
            <div class="row">
                <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                    <!-- Part 1 5 Points-->
                    <!-- Create a Signup Form where you retrieve the following Information -->
                    <!-- Full Name (First Name + Last Name) -->
                    <!-- Mail -->
                    <!--<div class="form-group">-->
                        <!--<label for="email">Mail</label>-->
                        <!--<input-->
                                <!--type="text"-->
                                <!--id="email"-->
                                <!--class="form-control"-->
                                <!--:value="userData.email"-->
                                <!--@input="userData.email = $event.target.value">-->
                    <!--</div>-->

                    <!-- Password -->
                    <!--<div class="form-group">-->
                        <!--<label for="password">Password</label>-->
                        <!--<input-->
                                <!--type="password"-->
                                <!--id="password"-->
                                <!--class="form-control"-->
                                <!--v-model.lazy.trim.number="userData.password">-->
                        <!--<p>{{ userData.password }}</p> </div>-->
                    <!-- Store Data? Yes/No -->

                    <!-- Part 2 5 Points -->
                    <!-- Only display the Form if it has NOT been submitted -->
                    <!-- Display the Data Summary ONCE the Form HAS been submitted -->

                    <!-- Part 3 5 Points -->
                    <!-- Edit the Example from above and create a custom "Full Name" Control -->
                    <!-- which still holds the First Name and Last Name Input Field -->

                    <div class="form-group">
                        <label >First Name</label>
                        <input type="text" class="form-control" v-model="firstName">
                    </div>
                    <div class="form-group" >
                        <label >Last Name</label>
                        <input type="text" class="form-control" v-model="lastName">
                    </div>

                    <div class="form-group">
                        <label >Mail</label>
                        <input type="text" class="form-control" v-model="email">
                    </div>

                    <div class="form-group">
                        <label >Password</label>
                        <input type="password" class="form-control" v-model="password">
                    </div>

                    <div class="form-group">
                        <label >
                            <input type="radio" value="Yes" class="form-control" v-model="storeData">
                        </label>
                    </div>
                    <div class="form-group">
                        <label >
                            <input type="radio" value="No" class="form-control" v-model="storeData">
                        </label>
                    </div>
                    <button type="submit"
                            class="btn btn-primary"
                            @click.prevent="submitted = true">Submit</button>
                </div>
            </div>
        </form>
        <hr>
        <div class="row" v-if="submitted">
            <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                <div class="panel panel-default">
                    <div class="panel-heading">
                        <h4>Your Data</h4>
                    </div>
                    <div class="panel-body">
                        <p>Full Name: {{firstName}}{{lastName}}</p>
                        <p>Mail: {{ email }}</p>
                        <p>Password: {{ password }}</p>
                        <p>Store in Database?: {{storeData}} </p>


                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    // import Switch from './Switch.vue';
    export default {
        data() {
            return {
                firstName: 'jess',
                lastName: 'nord',
                email: '',
                password: '',
                storeData: 'Yes',
                submitted: false
                }

            }
    }

</script>

<style>
</style>

<template>
     <body>
     <div class="container">


      <div class="row">
          <form>
            <div class="row">

                <div class="col s12 m6 offset-m3">
                      <div class="card center-align mg">

                          <div class="card-content">
                              <h3>Welcome!</h3>
                              <div class="input-field">
                                  <input id="email" type="text" class="validate">
                                  <label for="email">Email</label>
                              </div>
                              <div class="input-field" >
                                  <input id="password" type="password" class="validate">
                                  <label for="password">Password</label>

                              </div>
                                new? <a href="/register">register</a>
                              <div>

                              </div>
                              <button class="btn pulse blue lighten-1 waves-light" type="submit" v-on:click="login()" name="action">Login
                                  <i class="material-icons right">send</i>
                              </button>
                          </div>


                        </div>
                      </div>
                </div>


          </form>

      </div>
     </div>
     </body>
</template>

<script>
    export default {
        name: 'Login',
        data() {
            return {
                input: {
                    username: "",
                    password: ""
                }
            }
        },
        methods: {
            login() {
          
                if(this.input.username != "" && this.input.password != "") {
                    if(this.input.username == this.$parent.mockAccount.username && this.input.password == this.$parent.mockAccount.password) {
                        // this.$emit("authenticated", true);
                        // this.$router.replace({ name: "secure" });
                        alert("Hello! I am an alert box!!");

                    } else {
                        // console.log("The username and / or password is incorrect");
                    }
                } else {
                    // console.log("A username and password must be present");
                }
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
     <style scoped>
     h3 {
       margin: 40px 0 0;
     }
     ul {
       list-style-type: none;
       padding: 0;
     }
     li {
       display: inline-block;
       margin: 0 10px;
     }
     a {
       color: #34ADFF;
     }
</style>

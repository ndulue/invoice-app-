<template>
    <div>
        <div class="tab-pane fade show active" id="pills-login" role="tabpanel" aria-labelledby="pills-login-tab">
            <div class="row">
                <div class="col-md-12">
                    <form action="" @submit.prevent="login">
                        <div class="form-group">
                            <label for="Email"></label>
                            <input type="email" name="email" id="email" class="form-control" v-model="model.email" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="Password"></label>
                            <input type="password" name="password" id="password" class="form-control" v-model="model.password" required>
                        </div>

                        <div class="form-group">
                            <button class="btn btn-primary">Login</button>
                            {{ loading }}
                            {{ status }}
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>
</template>
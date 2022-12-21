<template>
    <v-card class="elevation-12">
        <v-toolbar dark color="teal">
            <v-toolbar-title>登入</v-toolbar-title>
        </v-toolbar>
        <v-row>
            <v-col cols="6" xs="6">
                <v-card-text>
                    <v-card-subtitle v-if="isWrong" dense class="red--text">
                        * 帳號密碼錯誤
                    </v-card-subtitle>
                    <v-form v-model="validate">
                        <v-text-field
                            prepend-icon="mid-account-circle"
                            name="login"
                            label="帳號"
                            type="text"
                            hint="請使用示範帳號登入"
                            :rules="Rules"
                            v-model="account"
                        ></v-text-field>
                        <v-text-field
                            id="password"
                            prepend-icon="mid-lock"
                            name="password"
                            label="密碼"
                            type="password"
                            hint="請使用示範帳號登入"
                            :rules="Rules"
                            v-model="password"
                        ></v-text-field>
                    </v-form>
                </v-card-text>
                <v-card-actions>
                    <v-spacer></v-spacer>
                    <v-btn 
                        color="teal"
                        @click="test()"
                        :disabled="!validate"
                    >Login</v-btn>
                </v-card-actions>
            </v-col>
            <v-col cols="6" class="mt-2" justify="center" xs="6">
                <h3>示範帳號1</h3>
                <p>帳號：劉大東</p>
                <p>密碼：root</p>
                <h3>示範帳號2</h3>
                <p>帳號：王阿花</p>
                <p>密碼：root</p>
            </v-col>
        </v-row>
    </v-card>
 </template>
 
 <script>
 export default {
    name: 'Login',
    props: {
       source: String,
    },
    data() {
    return {
        validate: false,
        Rules: [
        v => !!v || '必填欄位',
        ],
        account: "",
        password: "",
        isWrong: false,
    }
  },
  methods: {
    test(){
        this.isWrong = false
        if (this.account === "劉大東") {
            if (this.password === "root") {
                this.$router.push("/personal_report1")
            }
            else {
                this.isWrong = true
            }
        }
        else if (this.account === "王阿花") {
            if (this.password === "root") {
                this.$router.push("/personal_report2")
            }
            else {
                this.isWrong = true
            }
        }
        else {
            this.isWrong = true
        }
    }
  }
 };
 </script>
 
 <style></style>
 
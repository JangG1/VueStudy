<template>
<div class="login">
    <div class="inputForm">
       <router-link v-bind:to="'/'"> <img src="@/assets/logo.jpg" alt="logo"></router-link>
        <input class="inputID" type="text" v-model="username" placeholder="아이디 입력"><br>
        <input class="inputPWD" type="password" v-model="password" placeholder="비밀번호 입력"><br>
        <input class="inputBtn" type="button" value="login" @click="login"><br>
        <!-- <input type="button" value="회원가입" v-on:click="signUp()"> -->
        <div class="etc">
            <div class="checkBoxDiv"><input type="checkbox" id="a"> <label for="a">자동로그인</label></div>
            <div class="findBoxDiv">| 아이디찾기 | 비밀번호찾기</div>
        </div>
        <div class="signUpBtn">
            <router-link class="signUpLink" v-bind:to="'/signUp'">회원가입</router-link>
        </div>
        <!-- <LoginPage /> -->
    </div>
</div>
</template>

<script>
// @ is an alias to /src
// import LoginPage from '@/components/LoginPage.vue'

export default {
    data() {
        return {
            username: '',
            password: '',
            msg: '',
        }
    },
    methods: {
        login() {
            try {
                if (this.$store.getters.getUserInfo.username === this.username) {
                    if (this.$store.getters.getUserInfo.password === this.password) {
                        alert(this.username + "님 환영합니다");
                        this.$router.push("/");
                    } else if ("" === this.password) {
                        alert("비밀번호를 입력하세요.");
                    } else {
                        alert("비밀번호가 맞지 않습니다.");
                        this.password="";
                    }
                } else if ("" === this.username)
                    alert("아이디를 입력하세요.")
                else
                    alert("아이디가 맞지 않습니다.")

            } catch (err) {
                this.msg = "error";
            }
        }
    }

}
</script>

<style scoped>
.login {
    height: 1200px;
    text-align: center;
    /* border: 1px solid black; */
    margin: 0 auto;
    padding: 0;

}

.login>div {
    position: relative;
    display: block;
    left: 50%;
    top: 25%;
    transform: translate(-50%, -50%);
    text-align: center;
    /* border: 1px solid black; */
    width: 400px;
    height: 200px;
    padding: 0;
    margin: 0;
}

.inputID,
.inputPWD,
.inputBtn {
    border: 0.5px 1px black solid;
    width: 386px;
    height: 40px;
    margin: 0;
    padding: 5px;
    font-size: 15px;
}

.inputBtn {
    background-color: #0051ba;
    border-radius: 4px;
    border: none;
    color: white;
    text-decoration: none;
    padding: 0px 5px;
    width: 400px;
    font-size: 20px;
}

.etc {
    display: flex;
    border: black 1px solid;
    height: 40px;
}

.etc>* {
    margin: 10px 0px;
}

.findBoxDiv {
    margin-right: 5px;
    margin-left: auto;
}

.signUpBtn {
    height: 40px;
    /* border: black 1px solid; */
    margin-top: 10px;
}

.signUpLink {
    background-color: #0051ba;
    border-radius: 4px;
    border: none;
    font-size: 20px;
    color: white;
    text-decoration: none;
    padding: 5px 10px;
}

/* .signUpLink:link .signUpLink:hover .signUpLink:visited {

    color: white;
} */
</style>

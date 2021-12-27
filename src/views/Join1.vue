<template>
<div >
    <div style="text-align:center;">
        <router-link v-bind:to="'/'"> <img src="@/assets/logo.jpg" alt="logo"></router-link>
        <h1>회원가입</h1>
        <hr>
    </div>
    <form class="container" name="login_member" action="#" method="post" >
        <div>
            <h3>
                아이디
            <input type="text" name="class" class="id">
            <button class="classBtn" > 중복확인 </button>
               </h3>
        </div>
        <div>
            <h3>
                닉네임
            <input type="text" name="nick" class="nick">
            <button class="nickBtn"> 중복확인 </button>
             </h3>
        </div>
        <div>
            <h3>
                비밀번호
            <input type="password" name="password" class="password">
              </h3>
        </div>
        <div>
            <h3>
                비밀번호확인
            <input type="password" name="re_password" class="re_password">
              </h3>
        </div>
        <div>
            <h3>
                이름
            <input type="text" name="username" class="username">
              </h3>
        </div>
        <div>
            <h3>
                전화번호
            <input type="text" name="mobile" class="mobile" placeholder="-없이 숫자만" maxlength="11">
              </h3>
        </div>

        <div>
            <h3>
                주소
            <input type="text" name="total_add" class="total_add">
            <button class="addBtn">주소검색</button>
              </h3>
        </div>
        <div>
            <h3>
                상세주소
            <input type="text" name="detail_add" class="detail_add">
              </h3>
        </div>
    </form>
    <hr>
    <div class="footer">
        <div class="CheckBox">
            <label class="Agree">약관동의</label><br>
            <input type="checkbox" name="cb1" class="agree">귀하의 쇼핑몰에 회원으로 가입합니다(필수)<br>
            <input type="checkbox" name="cb2" class="agree">개인정보 수집 이용동의(필수)<br>
            <input type="checkbox" name="cb3" class="agree">마케팅 활용 및 광고성 정보 수신 동의 (선택)
        </div>
        <div class="joinBtnArea">
            <button class="joinBtn">가입하기</button>
        </div>
    </div>
</div>
</template>

<script>


export default {
    data() {
        return {}
    },
    methods: {
        range(start, end) {
            let list = []
            for (let i = start; i <= end; i++)
                list.push(i);
            return list;
        }
    },
    
}
</script>

<style scoped>
h1{
    font-size: 32px;
}
h2{
    font-size: 22px;
}
h3{
    font-size: 18px;

}
p, label, span{
    font-size: 16px;
}
.container {
    background-color: #fafafa;
    padding: 100px;
}

.container>div {
    width: 40%;
    margin-right: auto;
    margin-left: 200px;
    padding: 10px;
}

.container>div>h3 {
    width: 300%;
    margin: 12px 0;
}

/* .container>div>input {
    display: inline-block;
    height: 25px;
    margin-right: 10px;
    width: 300px;
    text-align: center;
    border-radius: 4px;
    border: 1px solid;
    
} */

.CheckBox {
    text-align: center;
    padding: 10px 0;
}
.footer{
    background-color: #fafafa;
}
.joinBtn{
background-color: #4a85d1;
margin-top: 30px;
}
.joinBtnArea {
    text-align: center;
    padding-bottom: 30px;
}

.classBtn,
.nickBtn,
.addBtn {
    background-color: #4a85d1;
    border-radius: 4px;
    border: none;
    color: white;
    padding: 5px 10px;
    margin-left: 25px;
}
.id, .nick, .password, .re_password, 
.username, .mobile, .total_add, .detail_add{
    text-align: center;
    height: 25px;
    border-radius: 4px;
    border: 1px solid;
    width: 290px;
}
.id{
    margin-left: 54px;
}
.nick{
    margin-left: 54px;
    }
.password{
    margin-left: 36px;
}

.username{
    margin-left: 73px;
}
.mobile{
    margin-left: 37px;
}
.total_add{
    margin-left: 73px;
}
.detail_add{
    margin-left: 36px;
}

</style>

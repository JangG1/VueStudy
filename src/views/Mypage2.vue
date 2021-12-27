<template>
<div>
    <!--top-->
  <div class="top" style="text-align:center">
           <router-link v-bind:to="'/'"> <img src="@/assets/logo.jpg" alt="logo"></router-link>
        <h1>마이페이지</h1>
    </div>
    <!--left-->
    <div class="container">
        <div class="left">
         <div class="List">
                   <router-link v-bind:to="'/mypage1'">나의쇼핑내역</router-link>
            </div>
            <div class="check">
                <li>주문/배송 조회</li>
                <li>취소/환불 조회</li>
            </div>
              <div class="List">
                  <router-link v-bind:to="'/mypage2'">회원정보 열람</router-link>
            </div>
            <div class="check">
                <li>회원정보 수정</li>
            </div>
            <router-link v-bind:to="'/'"> <button class="logoutbtn">로그아웃</button></router-link>
        </div>
        <!--right-->
        <div class="right">
            <div class="pList1">
                <h2>회원 정보 열람</h2>
            </div>
            <div class="content">
                <h3>
                    닉네임
                <input type="text" class="mdText" id="m1">
                <button class="mdBtn"> 수정하기 </button>
                </h3>
            </div>
            <div class="content">
                <h3>
                    비밀번호
                <input type="text" class="mdText" id="m2">
                <button class="mdBtn"> 수정하기 </button>
                </h3>
                <br>
            </div>
            <div class="content">
                <h3>
                    연락처
                <input type="text" class="mdText" id="m3">
                <button class="mdBtn"> 수정하기 </button>
                </h3>
            </div>
            <div class="content">
                <h3>
                    주소
                
                <input type="text" class="mdText" id="m4">
                <button class="mdBtn"> 주소조회 </button>
                </h3>
            </div>
            <div class="content">
                <h3>
                    <label>상세주소</label>
                
                <input type="text" class="mdText" id="m5">
                <button class="mdBtn"> 수정하기 </button>
                </h3>
            </div>
            <div class="content">
                <router-link v-bind:to="'/'"> <button class="quit">회원탈퇴</button></router-link>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {}
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
.top {
    margin-left: 70px;
}
.container {
    display: flex;
}

.left {
    display: inline-block;
    border: 1px solid rgb(197, 195, 195);
    background-color: #fafafa;
    border-radius: 4px;
}

.left>div {
   border-bottom: 1px solid rgb(197, 195, 195);
}


.right {
    display: inline-block;
    width: 85%;
    border: 1px solid rgb(197, 195, 195);
    margin-left: 50px;
    background-color: #fafafa;
    border-radius: 4px;
}

.right>div {
   border-bottom: 1px solid rgb(197, 195, 195);
}

.List {
    text-align: center;
    padding-top:10px;
    padding-bottom:10px;
}

.check {
    text-align: center;
    padding: 0px 10px;
}

.check li {
    width: 150px;
    padding: 0;
    margin: 10px 0px;
}

.pList1 {
    text-align: center;
       border-bottom: 1px solid black;
}


.content {
    padding: 10px;
}
.content>h3 {
 margin-left: 150px;
}


.mdText {
    width: 300px;
    margin-left: 30px;
    border-radius: 4px;
    border: 1px solid;

}

.mdBtn {
    background-color: #0051ba;
    border-radius: 4px;
    border: none;
    color: white;
    padding: 5px 10px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 13px;
    cursor: pointer;
    margin-left: 20px;
}

.logoutbtn{
    margin-top: 300px;
    margin-left: 35px;
}

.quit{
   background-color: #00ba54;
   margin-left: 360px;
}

#m1{
  margin-left: 47px;
}
#m2{
    margin-left: px;
}
#m3{
    margin-left: 47px;
}
#m4{
    margin-left: 65px;
}
#m5{
    margin-left: 45px;
}
</style>

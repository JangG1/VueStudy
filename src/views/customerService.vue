<template>
<div>
    <div class="customerService">
        <div class="csTop">
            <div class="csSearch">
                <input type="text" id="search" placeholder="자주 묻는 질문 검색" />
                <button type="button" onclick="location.href = 'success.html'">
                    검색
                </button>
            </div>
            <div class="cs1to1Q">
                <span style="margin: 0 20px; font-size: 200%;">1234-5678</span>
                <router-link v-bind:to="'/otoQ'">
                    <button>
                        1대1 문의하기
                    </button>
                </router-link>
            </div>
        </div>
        <hr />
        <div class="csFAQ">
            <div>
                <h2 style="text-align: left">자주 묻는 질문</h2>
            </div>
            <div>
                <table class="tableMain">
                    <tr>
                        <th>번호</th>
                        <th style="border-left: 1px black solid">제목</th>
                    </tr>
                    <tr v-for="FAQ in FAQs" :key="FAQ.number">
                        <td style="width: 10%">
                            <span v-html="FAQ.number"></span>
                        </td>
                        <td class="question">
                            <span  v-html="FAQ.question"></span>
                        </td>
                    </tr>
                </table>
            </div>
        </div>
        <hr />
        <div class="csNotice">
            <div>
                <h2 style="text-align: left">공지 사항</h2>
            </div>
            <div>
                <table class="tableMain">
                    <tr>
                        <th>번호</th>
                        <th style="border-left: 1px black solid">제목</th>
                    </tr>
                    <tr v-for="notice in notices" :key="notice.number">
                        <td style="width: 10%">
                            <span v-html="notice.number"></span>
                        </td>
                        <td class="notice">
                            <a href=""></a>
                            <span  v-html="notice.notice"></span>
                        </td>
                    </tr>
                </table>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    data() {
        return {
            FAQs: [{
                    number: "1",
                    question: "<a href='#''>[구매] 세금계산서를 발급받고 싶어요.</a>",
                },
                {
                    number: "2",
                    question: "<a href='#'>[구매] 취소/반품했는데, 언제 환불되나요.</a>",
                },
                {
                    number: "3",
                    question: "<a href='#'>[구매] 고객센터 이용 시간은 어떻게되나요.(1:1 상담을 원합니다.)</a>",
                },
                {
                    number: "4",
                    question: "<a href='#'>[배송] 주문한 상품은 언제 배송되나요?</a>",
                },
                {
                    number: "5",
                    question: "<a href='#'>[구매] 간편회원도 쿠폰을 사용할 수 있나요?</a>",
                },
            ],
            notices: [{
                    number: "1",
                    notice: "<a href='#'>[공지] 구매이용약관 개정 공지 (2022년 1월 3일 시행)</a>",
                },
                {
                    number: "2",
                    notice: "<a href='#'>[공지] 정기점검으로 인한 서비스 일시중지 - 12월 14일(금)</a>",
                },
                {
                    number: "3",
                    notice: "<a href='#'>환경부 공고, '요소수 판매에 관한 조정명령' (12/8~ )</a>",
                },
                {
                    number: "4",
                    notice: "<a href='#'>[공지] 정기점검으로 인한 서비스 일시중지 - 11월 17일(금)",
                },
                {
                    number: "5",
                    notice: "<a href='#'>[공지] 정기점검으로 인한 서비스 일시중지 - 10월 26일(금)</a>",
                },
            ],
        };
    },
};
</script>

<style scoped>
.customerService {
    text-align: center;
    border: 1px black solid;
    width: 100%;
}

.csTop {
    height: 100px;
    display: flex;
    align-items: center;
    margin: 10px 10px;
}

.csSearch {
    width: 65%;
    padding: 0 0;
    margin: 10px 10px;
}

#search {
    font-size: 170%;
}

.cs1to1Q {
    width: 35%;
    padding: 0 0;
    margin-left: auto;
}

button {
    background-color: #0051ba;
    border-radius: 4px;
    border: none;
    color: white;
    text-decoration: none;
    padding: 0px 5px;
    width: auto;
    height: 40px;
    font-size: 25px;
    margin: 5px 2px;
}

.csFAQ,
.csNotice {
    padding: 0 10px 10px 10px;
    margin: 20px 20px;
}

.tableMain {
    width: 100%;
    border: 1px black solid;
    border-collapse: collapse;
    padding: 10px 10px;
}

th,
td {
    border-bottom: 2px black solid;
    padding: 5px 5px;
}

.question,
.notice {
    border-left: 1px black solid;
    text-align: left;
    padding: 7px 20px;
}
</style>

<template>
  <body>
    <div class="AddEventView">
        <div class="header">

            <!-- 뒤로 가기 버튼 -->
            <div class="closeButton">
                <a href="javascript:history.back()" class="title"><img src="../assets/close.svg" alt="닫기"/></a>
            </div>
            
            <!-- 페이지 제목-->
            <p class="pageTitle">출석관리</p>
        </div>
    </div>
  </body>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import "~/scss/main.scss";

body{
    font: 15px;
    margin: 0;

    .AddEventView{

        .header{

            .closeButton{

            }
        }
    }
}

</style>
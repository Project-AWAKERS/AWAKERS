<template>
    <body>
      <header>
          <!-- 페이지 제목-->
          <p class="pageTitle">기존일정 수정하기</p>
  
          <!-- 닫기 버튼 -->
          <div class="backButton">
              <a href="javascript:history.back()" class="title"><img src="../assets/close.svg" alt="닫기"/></a>
          </div>        
  
      </header>
  
      <section>
  
          <!-- 일정명 입력란 -->
          <div class="eventName">
              <div id="name">일정명</div>
              <input type="text" name="eventName" class="inputEventName">
          </div>
          
          <!-- 날짜 입력란 -->
          <div class="eventDate">
              <div id="name">날짜</div>
              <input type="date" name="eventDate" class="inputEventDate">
          </div>
  
          <!-- 유형 선택 버튼 -->
          <div class="eventType">
  
              <!-- 필터링 버튼 1 (전체, 예배별, 행사별, 봉사별)-->
              <div id="name">구분</div>
              <div class="filterButton">
                  <div class="selectTypeButton">
                      <button class="selectType">예배</button>
                      <button class="selectType">행사</button>
                      <button class="selectType">봉사</button>
                  </div>
              </div>
          </div>
  
      </section>
  
      <footer>
          <!-- 로그인 버튼 -->
          <button type="button" @click="addEvent">추가하기</button>
      </footer>
    </body>
  </template>
  
  <script>
  export default {
      data(){
        return {
  
        }
      },
      methods: {
        //새로운 행사 추가 매서드
        addEvent(){
              const newEvent = {
                  id: this.events.length + 1,
                  name: `Event ${this.events.length + 1}`,
                  date: `1월 7일`,     //행사 날짜는 실제 날짜로 대체하기
                  attendees: Math.floor(Math.random() * 100) + 1,     //참석자 수는 랜덤
                  type: `예배`
              };
              this.events.push(newEvent);
          },
      }
  }
  </script>
  
  <style lang="scss" scoped>
  @import "~/scss/main.scss";
  
  body{
      font: 15px;
      width: 330px;
      height: 700px;
      margin-top: 30px;
  
      header{
          width: 330px;
          height: 20px;
          display: flex;
          
          .pageTitle{
              font-size: 18px;
              font-weight: bold;
              color: rgb(139, 138, 138);
          }
  
          .backButton{
              margin-top: -4px;
              margin-left: auto;
              cursor: pointer;
          }
      }
  
      section{
          margin-top: 24px;
  
          #name{
              font-size: 12px;
              font-weight: bold;
              color: gray;
          }
  
          .eventName{
              margin-top: 24px;
  
              .inputEventName{
                  margin-top: 10px;
                  width: 310px;
                  height: 25px;
                  border-radius: 10px;
              }
          }
  
          .eventDate{
              margin-top: 24px;
  
              .inputEventDate{
                  margin-top: 10px;
                  width: 310px;
                  height: 35px;
                  border-radius: 10px;
                  color: black;
              }
          }
  
          .eventType{
              margin-top: 24px;
  
              .selectTypeButton{
                  margin-top: 10px;
                  display: flex;
                  gap: 7px;
                  width: 200px;
                  height: 30px;
  
                  .selectType{
                      width: 50px;
                      height: 30px;
                      border : none;
                      border-radius : 10px;
                      color: rgb(91, 88, 88);
                      cursor: pointer;
                      //background-color: rgb(204, 198, 198);
                  }
  
                  .selectType:hover{
                      color: white;
                      background-color: rgb(88, 87, 87);
                  }
              }
          }
      }
  
      footer{
          position: absolute;
          bottom: 20px;
      
          button{
              font-size: 15px;
              font-weight: bold;
              width: 330px;
              padding: 15px;
              background-color: #606761;
              color: white;
              border: none;
              border-radius: 8px;
              cursor: pointer;
              bottom: 0;
          }
  
          button:hover{
              background-color: #171a17;
          }
      }
  }
  
  </style>
<template>
    <body>
        <div class="black-bg" v-if="modalOpen == true">
            <div class="white-bg">
                <!-- 제목 -->
                <div class="modalHeader">
                    <div>출석 관리</div>

                    <!-- 닫기 버튼 -->
                    <div class="closeBtn">
                        <img src="../assets/close.svg" @click="modalOpen = false" alt="닫기"/>
                    </div>
                </div>
                
                <footer>
                    <!-- 수정 버튼 -->
                    <button type="button"  onclick="location.href='#/EditEventPage'" >수정하기</button>
                </footer>
            </div>
        </div>

        <div class="AttendanceDashboardView">
            <div class="header">
                
                <!-- 뒤로 가기 버튼 -->
                <div class="backButton">
                    <a href="javascript:history.back()" class="title"><img src="../assets/chevron-left.svg" alt="뒤로가기"/></a>
                </div>
                
                <!-- 페이지 제목-->
                <p class="pageTitle">출석 대시보드</p>
            </div>
            <div class="container">
                <div class="menu">
                    <div class="filterMenu">
                        
                        <!-- 페이지 소제목-->
                        <div class="title">AWAKE 예배</div>  
                        <div class="subtitle">1월 7일</div>                         

                        <!--토스트 팝업 메뉴 버튼 -->
                        <div class="toast">
                            <button type="button" class="toastButton">
                                <img src="../assets/options-horizontal.svg" onclick="location.href='#/AddEventPage'" alt="Add Event" class="addButton">
                            </button>
                        </div>
                    </div>
                </div>
                
            </div>
        </div>
    </body>
</template>

<script>

export default {
    data(){
        return {
            events: [
                {
                    name: 'AWAKE 예배',
                    date: '1월 7일',
                    attendees: 55,
                    type: '예배',
                },
            ],
            modalOpen: false,
        }
    },
    methods: {
        
    },
};
</script>

<style lang="scss" scoped>
@import "~/scss/main.scss";

body{
    font: 15px;
    margin: 0;

    .black-bg{
        box-sizing: border-box;
        width: 100%;
        height: 100%;
        background: rgba(0,0,0,0.5);
        position: fixed;
        top: 0;
        left: 0;
        text-align: center;
        justify-content: center;
        display: flex;
        

        .white-bg{
            width: 350px;
            height: 150px;
            background: white;
            border-radius: 20px;
            padding: 20px;
            margin: 0 auto;
            bottom: 0;
            position: absolute;


            .modalHeader{
                display: flex;
                height: 30px;
                font-size: 17px;
                font-weight: bold;
                color: rgb(123, 121, 121);
                

                .closeBtn{
                    width: 24px;
                    height: 10px;
                    margin-left: auto;
                    cursor: pointer;
                }

                
            }
        }  
    
        button{
            font-size: 15px;
            font-weight: bold;
            width: 330px;
            height: 45px;
            padding: 15px;
            margin-top: 10px;
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


    .AttendanceDashboardView{
        width: 330px;
        height: 700px;
        margin: 0 auto;

        .header{
            width: 330px;
            height: 80px;
            text-align: center;
            font-size: 15px;
            margin-top: 20px;
            display: flex;
            
            .backButton{
                float: left;
                cursor: pointer;
            }
            .pageTitle{
                margin: 5px 10px 5px -15px;
                height: 100%;
                width: 100%;
                font-size: 15px;
                color: gray;
            }
        }

        .container{
            height: 800px;
            width: 330px;
            //background: #ccc;

            .menu{
                font-size: 17px;
                width: 330px;
                height: 50px;
                //background: #d3d5f3;
                float: left;
                display: flex;

                .filterMenu{
                    font-size: 18px;
                    width: 330px;
                    height: 24px;
                    display: flex;
                
                    .title{
                        color: rgb(118, 114, 114);
                        margin-top: 3px;
                        font-weight: 800;
                        width: 150px;
                        height: 24px;
                    }

                    .subtitle{
                        width: 290px;
                        height: 50px;
                        padding: 10px;
                        margin-top: 17px;
                        margin-left: -160px;
                        background: transparent;
                        color : rgb(199, 193, 193);
                        font-size: 10px;
                        float: left;
                    }

                    .toast{
                        display: flex;
                        margin-left: auto;
                    
                        .toastButton{
                            border: none;
                            background-color: transparent;
                            cursor: pointer;
                            height: 45px;

                        .addButton{
                            cursor: pointer;
                        }
                    }
                }
            }
        }

        .filterButton{
            width: 330px;
            height: 100px;

            .selectTypeButton{
                display: flex;
                gap: 7px;
                border-radius: 5px;
                width: 200px;
                height: 30px;

                .selectType{
                    width: 50px;
                    height: 30px;
                    border : none;
                    border-radius : 4px;
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

        .filterButton2{
            float: right;
            margin-top: -45px;
            margin-right: 10px;

            #order{
                color: black;
                width: 62px; 
                height: 20px; 
                border-style: none;
                cursor: pointer;
            }
        }
        
        .contentsContainer{
            .contents{
                width: 330px;
                height: 700px;
                //background: #fffa99;
                float: left;

                    .contentsBox{
                        width: 290px;
                        height: 50px;
                        background-color: rgb(223, 219, 219);
                        border-radius: 10px;
                        padding: 16px;
                        cursor: pointer;

                        .contentsTitle{
                            font-size: 17px;
                            font-weight: bold;
                            color: rgb(98, 97, 97);
                        }

                        .contentsDate{
                            font-size: 10px;
                            margin-top: 5px;
                            color: rgb(132, 129, 129);
                        }

                        .etc{
                            margin-top: 10px;
                            display: flex;
                            gap: 6px;

                            .attendance{
                                color: rgb(125, 124, 124);
                                font-weight: bold;
                                font-size: 13px;
                            }

                            .type{
                                color: gray;
                                background-color: white;
                                clear: both;
                                float: left;
                                width: 25px;
                                height: 16px;
                                border-radius: 6px;
                                font-weight: 650;
                                font-size: 10.8px;
                                display: flex;
                                flex-direction: column;
                                justify-content: center;
                                align-items: center;
                            }
                        }

                        .editEvents{
                            margin-top: -40px;
                            float: right;
                            cursor: pointer;
                        }

                        .scrollContainer{
                            height: 300px;
                            overflow-y: scroll;
                        }
                    }
                }
            }  
        }
    }
}


</style>
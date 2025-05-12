<template>
    <div class="container-content">
        <div v-if="menu" class="overlay"></div>
        <div class="header" >
            <div class="header-top" :class="{'active': offsetY >= 100}">
                <div class="header-logo">
                    <div class="icon"></div>
                </div>
                <div class="header-nav" v-if="!mobile">
                    <button class="nav-item" @click="moveSection(0)">About</button>
                    <button class="nav-item" @click="moveSection(1)">Vision</button>
                    <button class="nav-item" @click="moveSection(2)">Features</button>
                    <button class="nav-item" @click="moveSection(3)">Values</button>
                    <button class="nav-item" @click="moveSection(4)">FAQ</button>
                </div>
                <button class="download-btn">앱 다운로드</button>
                <div class="menu-icon" v-if="mobile" @click="showMenu">
                    <div class="bar"></div>
                    <div class="bar"></div>
                    <div class="bar"></div>
                </div>
            </div>
            <div class="header-bottom" v-if="menu " >
                <button class="nav-item menu" :class="{'active' : activeIndex==0}" @click="moveSection(0)">About</button>
                <button class="nav-item menu" :class="{'active' : activeIndex==1}" @click="moveSection(1)">Vision</button>
                <button class="nav-item menu" :class="{'active' : activeIndex==2}" @click="moveSection(2)">Features</button>
                <button class="nav-item menu" :class="{'active' : activeIndex==3}" @click="moveSection(3)">Values</button>
                <button class="nav-item menu" :class="{'active' : activeIndex==4}" @click="moveSection(4)">FAQ</button>
            </div>
        </div>


        <div class="pt100" id="section-0">
            <div class="main-box">
                <div class="box-main-title">
                    대중교통, <br>
                    더 빠르고 똑똑하게
                </div>
                <div class="box-sub-title">
                    매일의 이동이 더 간편하고 가벼워집니다.
                </div>
                <div class="download-box">앱 다운로드 하기
                    <button class="download-btn">
                        <div class="icon"></div>
                    </button>
                </div>
                <div class="bus"></div>
            </div>

            <div class="mt192">
                <div class="message main">버스터와 함께 즐거운 출근길</div>
                <div class="message sub mt14">바쁜 아침, 더 빠른 길을 찾느라 헤매지 마세요.</div>
                <div class="message sub mt4">버스터는 매일의 출근길을 더 똑똑하고 편리하게 만듭니다.</div>
            </div>

            <div class="box-intro-groups">
                <div class="rocket">
                    <div class="main-message">언제, 어디서든 빠르게</div>
                    <div class="sub-message">
                        출발지부터 목적지까지 이동할때
                        버스, 지하철, 도보를 활용한 경로를 안내하고,
                        실시간으로 현재 위치를 확인합니다.
                    </div>
                </div>
                <div class="people">
                    <div class="main-message">바쁜 출근시간, 효율적으로</div>
                    <div class="sub-message">
                        알림 스케줄 설정으로
                        대중교통 도착시간을 알림 받아
                        목적지까지 늦지 않게 도착할 수 있어요.
                    </div>
                </div>
                <div class="setting">
                    <div class="main-message">알뜰한 리워드 적립</div>
                    <div class="sub-message">
                        보상형 광고를 시청하거나,
                        승하차 정보를 입력하여 리워드를
                        적립하고 기프티콘으로 교환해요.
                    </div>
                </div>
            </div>
        </div>

        <div id="section-1" class="section">
            <div class="vision-section">
                <div class="vision-logo">Buster Vision</div>
                <div class="vision-title">
                    <div class="message main ta-s">
                        혁신으로 <br> 만들어가는 지속 가능한 미래
                    </div>
                    <div class="message sub ta-s">
                        버스터는 환경과 사회를 고려한 스마트한 선택으로,
                        더 나은 내일을 위한 변화를 이끌어갑니다.
                    </div>
                </div>

                <div class="vision-info-groups">
                    <div class="person">
                        <div class="image"></div>
                        <div class="main-title">
                            복잡함은 피하는
                            똑똑한 이동
                        </div>
                        <div class="sub-title">
                            혼잡도 분석을 통해 도로와 정류장의 붐빔을
                            분산합니다. 개인의 선택이 도시 전체의 흐름을
                            바꾸는 데 기여합니다.
                        </div>
                    </div>
                    <div class="column">
                        <div class="happy">
                            <div class="main-title">누구에게나 행복한 선택</div>
                            <div class="sub-title">
                                누구나 사용할 수 있는 기술은 더 많은 사람을 위한 것이어야 한다고 믿습니다.
                            </div>
                        </div>
                        <div class="carbon">
                            <div class="main-title">더 적은 탄소, 더 나은 선택</div>
                            <div class="sub-title">효율적인 이동 경로는 탄소 배출을 줄이는 실천이 됩니다. 버스터는 매일의 이동을 더 친환경적으로 만들어줍니다.</div>
                            <div class="image"></div>
                        </div>

                    </div>

                    <div class="column">
                        <div class="subway">
                            <div class="image"></div>
                            <div class="main-title">함께 만드는 교통 생태계</div>
                            <div class="sub-title">사용자의 참여로 수집된 정보를 통해 서비스 품질을 높입니다. 우리는 함께 더 나은 교통 생태계를 만들어갑니다.</div>
                        </div>

                        <div class="technology">
                            <div class="main-title">기술로 이어지는 공동체</div>
                            <div class="sub-title">버스터는 기술을 통해 도시의 연결을 돕고, 사람과 사람을 더 가깝게 만듭니다.</div>
                        </div>

                    </div>

                </div>
            </div>

            <div class="vision-message mt192" v-if="!mobile">
                버스터는 실시간 도착
                정보부터 혼잡도, 환승 경로까지
            </div>
            <div class="vision-message" v-if="!mobile">
                한 번에 보여주는 대중교통 안내
                서비스입니다.
            </div>
        </div>

        <div id="section-2" class="section pt192">
            <div class="message main">
                똑똑한 이동,
            </div>
            <div class="message main">
                똑똑한 이동,버스터가 바꾸는 일상
            </div>
            <div class="message sub mt18">
                우리는 단순한 길찾기를 넘어, 이동의 모든 순간을 연결합니다
            </div>
            <div class="message sub mt4">
                실시간 혼잡도 기반 경로 안내, 간편한 통합 결제, 일정에 맞춘 알림, 그리고 쓸수록 보상이 쌓이는 리워드까지
            </div>
            <div class="message sub mt8">
                버스터는 더 빠르고 여유로운 이동을 통해 도시 생활을 바꿔갑니다.
            </div>

            <div class="introduce-group">
                <div class="phone1">
                    <div class="image"></div>
                    <div class="main-title">혼잡도 기반 경로 안내</div>
                    <div class="tag-groups">
                        <div class="tag-box">Mobility</div>
                        <div class="tag-box">혼잡도</div>
                        <div class="tag-box">실시간 분석</div>
                    </div>
                </div>
                <div class="phone2">
                    <div class="image"></div>
                    <div class="main-title">통합 교통 결제 시스템</div>
                    <div class="tag-groups">
                        <div class="tag-box">Smart Pay</div>
                        <div class="tag-box">통합결제</div>
                        <div class="tag-box">간편함</div>
                    </div>
                </div>
                <div class="phone3">
                    <div class="image"></div>
                    <div class="main-title">출퇴근 스케줄 알림</div>
                    <div class="tag-groups">
                        <div class="tag-box">Time Alert</div>
                        <div class="tag-box">스케줄링</div>
                        <div class="tag-box">정시성</div>
                    </div>
                </div>
                <div class="phone4">
                    <div class="image"></div>
                    <div class="main-title">리워드 시스템</div>
                    <div class="tag-groups">
                        <div class="tag-box">Reward</div>
                        <div class="tag-box">기프티콘</div>
                        <div class="tag-box">친환경 인센티브</div>
                    </div>
                </div>
            </div>
        </div>

        <div id="section-3" class="section">
            <div class="radius-box">Values</div>
            <div class="message main mt16">
                스마트한 이동, 버스터와 함께
            </div>
            <div class="message sub mt14">
                바쁜 아침, 더 빠른 길을 찾느라 헤매지 마세요.
            </div>
            <div class="message sub mt4">버스터는 매일의 출근길을 더 똑똑하고 편리하게
                만듭니다.
            </div>

            <div class="value-cards-groups">
                <div class="carbon">
                    복잡한 길보다, 나은 선택을
                </div>
                <div class="experience">
                    여러 개의 앱 대신, 하나의
                    경험을
                </div>
                <div class="time">시간을 지키는 믿음직한
                    일상을
                </div>
            </div>
        </div>

        <div id="section-4" class="section pt103">
            <div class="message main">
                자주 묻는 질문
            </div>
            <div class="message sub mt18">
                버스터에 대해 자주 물어보는 질문들을 정리했어요.
            </div>
            <div class="message sub">
                궁금한 점이 더 있다면 언제든지 문의해주세요!
            </div>

            <div class="question-group">

                <div class="question-1">
                    <div class="main-title">혼잡도 정보는 어떻게 수집되나요?</div>
                    <div class="sub-title">
                        사용자들이 실시간으로 입력하는 정보와 공공
                        데이터를 함께 분석해 정확한 혼잡도를 제공합니다.
                    </div>
                </div>

                <div class="question-2">
                    <div class="main-title">정류장 정보는 얼마나 정확한가요?</div>
                    <div class="sub-title">
                        매일 업데이트되는 실시간 교통 데이터를
                        기반으로 제공되어 높은 정확도를 유지합니다.
                    </div>
                </div>

                <div class="question-3">
                    <div class="main-title">결제는 어떻게 하나요?</div>
                    <div class="sub-title">
                        버스터 내 통합 결제 시스템을 통해
                        다양한 교통수단을 한 번에 결제할 수 있습니다.
                    </div>
                </div>

                <div class="question-1">
                    <div class="main-title">스케줄 알림은 어떤 기능인가요?</div>
                    <div class="sub-title">
                        도착 시간을 미리 입력해두면, 교통 상황을
                        반영하여 최적 시간에 알림을 보내줍니다.
                    </div>
                </div>

                <div class="question-2">
                    <div class="main-title">개인화된 추천도 가능한가요?</div>
                    <div class="sub-title">
                        사용자의 이용 패턴을 분석해,
                        자주 이용하는 경로를 자동 추천해드립니다.
                    </div>
                </div>

                <div class="question-3">
                    <div class="main-title">위치 정보는 어떻게 활용되나요?</div>
                    <div class="sub-title">
                        정확한 경로 안내를 위해 사용자의 위치 정보가 활용
                        되지만, 모든 정보는 익명 처리되어 안전하게 보호돼요.
                    </div>
                </div>

            </div>
        </div>

    </div>
    <Footer :move-section="moveSection"></Footer>
</template>

<script>
import Footer from "@/footer.vue"
export default {
    name: "Intro",
    components: {
        Footer,
    },
    data() {
        return {
            activeIndex: 0,
            prevSceneHeight: 0,
            currentSceneOffsetY: 0,
            offsetY: 0,
            scrollInfo: [
                {
                    container: '',
                    heightNum: 1.5,
                    height: 0,
                },
                {
                    container: '',
                    heightNum: 1.5,
                    height: 0,
                },
                {
                    container: '',
                    heightNum: 1.8,
                    height: 0,
                },
                {
                    container: '',
                    heightNum: 0.5,
                    height: 0,
                },
                {
                    container: '',
                    heightNum: 0.8,
                    height: 0,
                },
            ],
            viewOffsetY: 0,

            mobile: false,

            menu : false,
        };
    },
    created() {
    },

    mounted() {
        this.setLayout();
        window.addEventListener("scroll", this.handleScroll);
        window.addEventListener("resize", this.setLayout);
        this.handleScroll();
    },
    unmounted() {
        window.removeEventListener("scroll", this.handleScroll);
    },
    methods: {
        setLayout() {
            this.mobile = window.innerWidth < 1152;

            if (window.innerWidth < 600) {
                // 모바일
                this.scrollInfo = [
                    { container: '', heightNum: 2.4, height: 0 },
                    { container: '', heightNum: 1.8, height: 0 },
                    { container: '', heightNum: 2.9, height: 0 },
                    { container: '', heightNum: 1, height: 0 },
                    { container: '', heightNum: 1.5, height: 0 },
                ];
            } else if (window.innerWidth < 1024) {
                // 태블릿
                this.scrollInfo = [
                    { container: '', heightNum: 2.2, height: 0 },
                    { container: '', heightNum: 2, height: 0 },
                    { container: '', heightNum: 1.7, height: 0 },
                    { container: '', heightNum: 0.8, height: 0 },
                    { container: '', heightNum: 0.9, height: 0 },
                ];
            } else {
                // 데스크탑
                this.scrollInfo = [
                    { container: '', heightNum: 1.5, height: 0 },
                    { container: '', heightNum: 1.8, height: 0 },
                    { container: '', heightNum: 2, height: 0 },
                    { container: '', heightNum: 1, height: 0 },
                    { container: '', heightNum: 1, height: 0 },
                ];
            }

            for (let i = 0; i < this.scrollInfo.length; i++) {
                this.scrollInfo[i].height = 830 * this.scrollInfo[i].heightNum;
                this.scrollInfo[i].container = document.getElementById(`section-${i}`);
                this.scrollInfo[i].container.style.height = this.scrollInfo[i].height + 'px';
            }
            this.handleScroll();
        },
        activateVisibleElements(selector) {
            document.querySelectorAll(selector).forEach((el) => {
                const rect = el.getBoundingClientRect();
                const isVisible = rect.top < window.innerHeight * 0.8 && rect.bottom > 0;
                el.classList.toggle('active', isVisible);
            });
        },

        handleScroll() {
            this.offsetY = window.scrollY;

            const section2 = document.getElementById('section-2');
            if (section2) {
                const rect = section2.getBoundingClientRect();
                const isVisible = rect.top < window.innerHeight * 0.75 && rect.bottom > 0;
                document.body.style.backgroundColor = isVisible ? '#fff' : '#F5F4F6';
            }



            this.activateVisibleElements('.message');
            this.activateVisibleElements('.vision-section');
            this.activateVisibleElements('.vision-message');
            this.activateVisibleElements('.people');
            this.activateVisibleElements('.rocket');
            this.activateVisibleElements('.setting');
            this.activateVisibleElements('.phone1, .phone2, .phone3, .phone4');
            this.activateVisibleElements('.person');
            this.activateVisibleElements('.carbon');
            this.activateVisibleElements('.happy');
            this.activateVisibleElements('.subway');
            this.activateVisibleElements('.technology');
            this.activateVisibleElements('.experience');
            this.activateVisibleElements('.time');
            this.activateVisibleElements('.question-1, .question-2, .question-3');
            this.activateVisibleElements('.radius-box');
            this.showSection();
        },

        moveSection(index) {
            let scrollY = 0;
            for (let i = 0; i < index; i++) {
                scrollY += this.scrollInfo[i].height;
            }

            window.scrollTo({
                top: scrollY,
                behavior: 'smooth'
            });
        },

        showMenu(){
            if(this.menu){
                this.menu = false;
                return;
            }
            this.menu = true;
        },

        showSection(){
            const sections = document.querySelectorAll('[id^="section-"]');
            const viewportHeight = window.innerHeight;

            for (let i = 0; i < sections.length; i++) {
                const rect = sections[i].getBoundingClientRect();
                const isVisible = rect.top < viewportHeight / 2 && rect.bottom > viewportHeight / 2;

                if (isVisible) {
                    if (this.activeIndex !== i) {
                        this.activeIndex = i;
                        console.log('activeIndex:', this.activeIndex);
                    }
                    break;
                }
            }
        }
    },
};
</script>
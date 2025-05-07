# be14-4th-Ideality-MyLocalDiary

| 이혜영 | 정민선 | 한석현 | 정동한 | 권민수 | 장시원 |
|--------|--------|--------|--------|--------|--------|
| <div align="center"><img src="https://github.com/user-attachments/assets/f589b013-0193-4775-a908-76305427112c" width="150"><br>ISTP</div> | <div align="center"><img src="https://github.com/user-attachments/assets/2a9c8c91-0afa-4fa0-b10c-f4ad94bd9a09" width="150"><br>INFJ</div> | <div align="center"><img src="https://github.com/user-attachments/assets/c17d7bc2-4a71-4323-8fb4-7fb38f518daa" width="150"><br>ENFP</div> | <div align="center"><img src="https://github.com/user-attachments/assets/05d7d9de-3c77-4243-a553-fcfb24abc6e9" width="150"><br>ISTP</div> | <div align="center"><img src="https://github.com/user-attachments/assets/b695d9dc-9885-4731-9c6a-6dde1add62f9" width="150"><br>ISTP</div> | <div align="center"><img src="https://item.kakaocdn.net/do/eda86b27d953e0a1bc89848fff989e65f604e7b0e6900f9ac53a43965300eb9a" width="150"><br>INTJ</div> |

<br>


## 📚 목차


#### [📌 프로젝트 개요](#-프로젝트-개요)  <br>
#### [🧠 기획 의도](#-기획-의도)  <br>
#### [🚀 서비스 주요 기능](#-서비스-주요-기능)  <br>
#### [🛠 기술 스택](#-기술-스택)  <br>
#### [🌐 외부 API 및 주요 구현 기술](#-외부-api-및-주요-구현-기술)  <br>
#### [🕹️ 시스템 아키텍쳐](#-시스템-아키텍쳐)  <br>
#### [🔄 CI / CD](#-CI-/-CD) <br>
#### [🧾 jenkins script](#-jenkins-script)  <br>
#### [🧱 DDD](#-ddd)  <br>
- [🧩 도메인 도출](#-도메인-도출)  <br>
- [📦 bounded context](#-bounded-context)  <br>
- [🔗 연관 관계](#-연관-관계)  <br>
- [🗂 erd](#-erd)  <br>
#### [📝 팀원별 회고 모음](#-팀원별-회고-모음)  <br>



<br><br>

## 📌 프로젝트 개요


![image](https://github.com/user-attachments/assets/fd4c18b1-b4ac-48fd-be56-e764dd593bae)
### My Local Diary 란? 

My Local Diary는 **지도 기반의 소셜 네트워크 서비스(SNS)** 입니다. <br>

사용자는 자신의 일상이나 여행 기록을 글, 사진, 음악 등으로 게시하고, 이를 지도 위의 마커(Marker) 형태로 표시할 수 있습니다. 또한, 다른 사용자의 게시글 역시 지도 상에서 확인 가능하여, 누가 언제 어디에 어떤 경험을 했는지 공간적으로 탐색할 수 있습니다.
이 서비스를 통해 사용자는 단순한 타임라인이 아닌, ‘**지도 위에 나의 일상**’을 시각적으로 기록하고 공유할 수 있으며, 이를 바탕으로 **로컬 중심의 새로운 소셜** 연결을 경험하게 됩니다.


<br><br>

## 🧠 기획 의도
```
지도 위의 나를 기록하고, 공간에서 연결되다
```
### **1. 일상의 소소한 순간을 공간과 함께 기록**
많은 사람들이 사진이나 글로 자신의 일상을 기록하지만, 그 경험이 어디에서 이루어졌는지는 쉽게 잊히곤 합니다.
우리는 장소 기반의 기록을 통해 사용자들이 추억을 보다 생생하게 저장하고 회상할 수 있는 방법을 고민하게 되었습니다.

### **2. 지도 기반 콘텐츠 활용에 대한 관심 증가**
SNS를 중심으로 맛집이나 여행지를 지도에 정리해 공유하는 문화는 이미 널리 확산되어 왔습니다.
사용자들은 구글 맵에 직접 장소를 저장하거나, 별도의 웹 서비스를 활용해 자신만의 장소 기반 콘텐츠를 큐레이션하고 있습니다.
이는 단순한 콘텐츠 소비를 넘어, 장소 중심의 기록과 공유에 대한 수요가 지속적으로 증가하고 있음을 보여줍니다.
My Local Diary는 이러한 흐름을 반영해, 누구나 개인화된 로컬 지도를 만들고 소셜하게 공유할 수 있는 플랫폼을 제공합니다.

### **3. 장소 중심의 새로운 소셜 네트워크**
기존 SNS는 타임라인 중심으로 정보가 쏟아져, 콘텐츠의 맥락과 공간적 의미가 흐려지기 쉽습니다.
우리는 ‘**어디서**’라는 장소의 관점을 중심에 둔 소셜 구조를 통해, 로컬 커뮤니티 간의 연결을 유도하고자 했습니다.

### **4. 지도라는 UI/UX의 직관성과 감성적 몰입**
지도는 시각적으로 풍부한 정보 전달뿐 아니라 공간적 몰입감과 감성적 경험을 제공합니다.
단순한 텍스트나 이미지보다 더 직관적인 방식으로, 사용자가 ‘지도 위의 내 삶’을 시각적으로 경험할 수 있다는 점에서 이 구조는 매우 매력적이었습니다.


<br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/e76adee3-0066-477f-9029-2ba2f3efd738" width="800"/>
</p>


## 🚀 서비스 주요 기능
<details>
<summary>📍 장소 등록 및 마커 기반 게시글 작성</summary>

- 사용자는 글을 작성할 때 반드시 장소를 선택하거나 검색해 지정해야 합니다.
- 등록된 장소는 지도 위에 마커 형태로 표시되며, 마커에는 해당 게시글의 썸네일 이미지가 함께 노출됩니다.
- 마커 클릭 시, 간단한 미리보기(사진/제목)와 함께 모달로 상세 게시글을 확인할 수 있습니다.
- 지도 기능은 네이버 Maps API로 구현되었으며, geocoder와 Search API를 통해 장소 검색과 주소 → 좌표 변환 기능도 지원합니다.

</details>

<details>
<summary>🗺️ 지도 홈 (메인 피드)</summary>

- 로그인 시 진입하는 메인 화면은 전체 지도 기반의 게시글 피드입니다.
- 지도에는 나와 타인의 게시글이 각각 마커 + 썸네일 형태로 표시되며,
- 내 게시글은 구별된 색상이나 아이콘으로 시각적으로 강조됩니다.
- 팔로잉 유저 목록이 사이드바에 표시되고, 유저별 마커 표시 여부를 토글할 수 있습니다.
- 마커에 마우스를 올리면 회오리 효과(싱크홀 모티브)가 발생합니다.

</details>

<details>
<summary>🧑‍🎤 마이페이지 (프로필) 기능</summary>

- 닉네임, 프로필 이미지, 자기소개, 프로필 음악 등을 설정할 수 있습니다.
- 진입 시 배경 음악이 자동 재생되며, 레트로 감성을 연출합니다.
- 미니 맵을 통해 내 게시글 위치가 시각적으로 요약됩니다.

</details>

<details>
<summary>🤝 팔로우 및 실시간 알림 시스템</summary>

- 공개 계정은 클릭 시 즉시 팔로우, 비공개 계정은 요청-수락 절차 필요
- 팔로우 및 새 게시글 업로드 시 실시간 알림 발송
- SSE(Server-Sent Events) 기반으로 실시간 통신 구현

</details>

<details>
<summary>🏅 스탬프 & 뱃지 시스템</summary>

- 게시글 작성 시 조건 충족에 따라 스탬프 자동 획득
- 동일 카테고리 스탬프 5개 수집 시 뱃지 해금
- 뱃지 클릭 시 고양이 소리 이스터에그가 재생되는 재미 요소 포함

</details>




<br>
  
## 🛠 기술 스택

### 🧩 Backend
![Spring](https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)
![Spring Data JPA](https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=for-the-badge)
![Hibernate](https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=hibernate&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=JSON%20web%20tokens&logoColor=white)
![Gradle](https://img.shields.io/badge/Gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

### 🎨 Frontend
![Vue.js](https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Vuetify](https://img.shields.io/badge/Vuetify-1867C0?style=for-the-badge)
![Vue Router](https://img.shields.io/badge/Vue_Router-4FC08D?style=for-the-badge)
![Pinia](https://img.shields.io/badge/Pinia-FADA5E?style=for-the-badge&logo=pinia&logoColor=black)
![Axios](https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge)

### 🗄 Database / Infra
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=for-the-badge&logo=mariadb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
![Amazon S3](https://img.shields.io/badge/Amazon_S3-569A31?style=for-the-badge&logo=amazonaws&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)

### 🧰 Tools
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Discord](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)


## 🌐 외부 API 및 주요 구현 기술
| 구분 | 기술 / API | 설명 |
|------|------------|------|
| 지도 렌더링 | Naver Maps API | 마커 기반 지도 시각화 |
| 장소 검색 | Naver Search API | 키워드로 장소 검색 |
| 주소 변환 | Naver geocoder 서브모듈 | 도로명 주소 → 좌표 (Geocoding) |
| 실시간 알림 | SSE (Server-Sent Events) | 팔로우/게시글 알림 푸시 |
| 인증 | JWT | 사용자 로그인/회원가입 인증 관리 |
| 배포 환경 | Docker + Kubernetes + AWS | 컨테이너 기반 인프라 관리 |
| 정적 파일 | Amazon S3 | 이미지, 오디오 파일 업로드/호스팅 |


<br>

## 🕹️ 시스템 아키텍쳐
<img src="https://github.com/2TEAM-Ideality/be14-4th-Ideality-MyLocalDiary/blob/main/resources/SystemArchitecture.png" />

## 🔄 CI / CD
<img src="https://github.com/2TEAM-Ideality/be14-4th-Ideality-MyLocalDiary/blob/main/resources/front-pipe.png" />
<img src="https://github.com/2TEAM-Ideality/be14-4th-Ideality-MyLocalDiary/blob/main/resources/back-pipe.png" />
<img src="https://github.com/2TEAM-Ideality/be14-4th-Ideality-MyLocalDiary/blob/main/resources/argocd.png" />

## 🧾 Jenkins Script
<details>
<summary>front-pipe</summary>

``` groovy
stages {
        stage('Create .env') {
            steps {
                withCredentials([
                    string(credentialsId: 'VITE_NAVER_MAP_CLIENT_ID', variable: 'VITE_NAVER_MAP_CLIENT_ID'),
                    string(credentialsId: 'VITE_NAVER_SEARCH_CLIENT_ID', variable: 'VITE_NAVER_SEARCH_CLIENT_ID'),
                    string(credentialsId: 'VITE_NAVER_SEARCH_CLIENT_SECRET', variable: 'VITE_NAVER_SEARCH_CLIENT_SECRET'),
                ]) {
                    script {
                        writeFile file: "${ENV_FILE}", text: """
                            VITE_NAVER_MAP_CLIENT_ID=${VITE_NAVER_MAP_CLIENT_ID}
                            VITE_NAVER_SEARCH_CLIENT_ID=${VITE_NAVER_SEARCH_CLIENT_ID}
                            VITE_NAVER_SEARCH_CLIENT_SECRET=${VITE_NAVER_SEARCH_CLIENT_SECRET}
                        """.stripIndent().trim()
                    }
                }
            }
        }
        stage('Preparation') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'docker --version'
                    } else {
                        bat 'docker --version'
                    }
                }
            }
        }
        stage('Source Build') {
            steps {
                git branch: 'main', url: "${env.GITHUB_URL}"
                script {
                    if (isUnix()) {
                        sh "cd my-local-diary && npm install"
                        sh "cd my-local-diary && npm run build"
                    } else {
                        bat "cd my-local-diary && npm install"
                        bat "cd my-local-diary && npm run build"
                    }
                }
            }
        }
        stage('Container Build and Push') {
            steps {
                script {
                    withCredentials([usernamePassword(credentialsId: 'DOCKERHUB_PASSWORD', usernameVariable: 'DOCKER_USER', passwordVariable: 'DOCKER_PASS')]) {
                        if (isUnix()) {
                            sh "docker build -t ${DOCKER_USER}/my_local_diary_front:${currentBuild.number} ./my-local-diary"
                            sh "docker build -t ${DOCKER_USER}/my_local_diary_front:latest ./my-local-diary"
                            sh "docker login -u ${DOCKER_USER} -p ${DOCKER_PASS}"
                            sh "docker push ${DOCKER_USER}/my_local_diary_front:${currentBuild.number}"
                            sh "docker push ${DOCKER_USER}/my_local_diary_front:latest"
                        } else {
                            bat "docker build -t ${DOCKER_USER}/my_local_diary_front:${currentBuild.number} ./my-local-diary"
                            bat "docker build -t ${DOCKER_USER}/my_local_diary_front:latest ./my-local-diary"
                            bat "docker login -u %DOCKER_USER% -p %DOCKER_PASS%"
                            bat "docker push ${DOCKER_USER}/my_local_diary_front:${currentBuild.number}"
                            bat "docker push ${DOCKER_USER}/my_local_diary_front:latest"
                        }
                    }
                }
            }
        }
        stage('K8S Manifest Update') {
            steps {
                git credentialsId: 'github',
                    url: "${env.MANIFESTS_GITHUB_URL}",
                    branch: 'main'
                
                script { 
                    withCredentials([usernamePassword(credentialsId: 'github', usernameVariable: 'GIT_USER', passwordVariable: 'GIT_PASS')]) {
                        def githubUrl = env.MANIFESTS_GITHUB_URL.replace('https://', '')
                        if (isUnix()) {
                            sh "sed -i '' 's/my_local_diary_front:.*\$/my_local_diary_front:${currentBuild.number}/g' k8s/frontend-deploy.yml"
                            sh "git add k8s/frontend-deploy.yml"
                            sh "git config --global user.name '${env.GIT_USERNAME}'"
                            sh "git config --global user.email '${env.GIT_EMAIL}'"
                            sh "git commit -m '[UPDATE] ${currentBuild.number} image versioning'"
                            sh "git push https://${GIT_USER}:${GIT_PASS}@${githubUrl} main"
                        } else {
                            bat "powershell -Command \"(Get-Content k8s/frontend-deploy.yml) -replace 'my_local_diary_front:.*', 'my_local_diary_front:${currentBuild.number}' | Set-Content k8s/frontend-deploy.yml\""
                            bat "git add k8s/frontend-deploy.yml"
                            bat "git config --global user.name '${env.GIT_USERNAME}'"
                            bat "git config --global user.email '${env.GIT_EMAIL}'"
                            bat "git commit -m \"[UPDATE] ${currentBuild.number} image versioning\""
                            bat "git push https://%GIT_USER%:%GIT_PASS%@${githubUrl} main"
                        }
                    }
                }
            }
        }
    }
```
</details>

<details>
<summary>back-pipe</summary>

``` groovy
stages {
        stage('Create secret.properties') {
            steps {
                withCredentials([
                    string(credentialsId: 'DB_USERNAME', variable: 'DB_USERNAME'),
                    string(credentialsId: 'DB_PASSWORD', variable: 'DB_PASSWORD'),
                    string(credentialsId: 'S3_ACCESS_KEY', variable: 'S3_ACCESS_KEY'),
                    string(credentialsId: 'S3_SECRET_ACCESS_KEY', variable: 'S3_SECRET_ACCESS_KEY'),
                    string(credentialsId: 'KAKAO_REST_API_KEY', variable: 'REST_API_KEY'),
                    string(credentialsId: 'server_secret_key', variable: 'secret_key'),
                    string(credentialsId: 'EMAIL_USERNAME', variable: 'EMAIL_USERNAME'),
                    string(credentialsId: 'EMAIL_PASSWORD', variable: 'EMAIL_PASSWORD'),
                    string(credentialsId: 'VITE_NAVER_SEARCH_CLIENT_ID', variable: 'NAVER_SEARCH_CLIENT_ID'),
                    string(credentialsId: 'VITE_NAVER_SEARCH_CLIENT_SECRET', variable: 'NAVER_SEARCH_CLIENT_SECRET')
                ]) {
                    script {
                        writeFile file: "${ENV_FILE}", text: """
                            DB_USERNAME=${DB_USERNAME}
                            DB_PASSWORD=${DB_PASSWORD}
                            S3_ACCESS_KEY=${S3_ACCESS_KEY}
                            S3_SECRET_ACCESS_KEY=${S3_SECRET_ACCESS_KEY}
                            REST_API_KEY=${REST_API_KEY}
                            secret_key=${secret_key}
                            EMAIL_USERNAME=${EMAIL_USERNAME}
                            EMAIL_PASSWORD=${EMAIL_PASSWORD}
                            NAVER_SEARCH_CLIENT_ID=${NAVER_SEARCH_CLIENT_ID}
                            NAVER_SEARCH_CLIENT_SECRET=${NAVER_SEARCH_CLIENT_SECRET}
                        """.stripIndent().trim()
                    }
                }
            }
        }
        stage('Preparation') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'docker --version'
                    } else {
                        bat 'docker --version'
                    }
                }
            }
        }
        stage('Source Build') {
            steps {
                git branch: 'main', url: "${env.GITHUB_URL}"
                script {
                    if (isUnix()) {
                        sh "chmod +x ./gradlew"
                        sh "./gradlew clean build"
                    } else {
                        bat "gradlew.bat clean build"
                    }
                }
            }
        }
        stage('Container Build and Push') {
            steps {
                script {
                    withCredentials([usernamePassword(credentialsId: 'DOCKERHUB_PASSWORD', usernameVariable: 'DOCKER_USER', passwordVariable: 'DOCKER_PASS')]) {
                        if (isUnix()) {
                            sh "docker build -t ${DOCKER_USER}/my_local_diary_back:${currentBuild.number} ."
                            sh "docker build -t ${DOCKER_USER}/my_local_diary_back:latest ."
                            sh "docker login -u ${DOCKER_USER} -p ${DOCKER_PASS}"
                            sh "docker push ${DOCKER_USER}/my_local_diary_back:${currentBuild.number}"
                            sh "docker push ${DOCKER_USER}/my_local_diary_back:latest"
                        } else {
                            bat "docker build -t ${DOCKER_USER}/my_local_diary_back:${currentBuild.number} ."
                            bat "docker build -t ${DOCKER_USER}/my_local_diary_back:latest ."
                            bat "docker login -u %DOCKER_USER% -p %DOCKER_PASS%"
                            bat "docker push ${DOCKER_USER}/my_local_diary_back:${currentBuild.number}"
                            bat "docker push ${DOCKER_USER}/my_local_diary_back:latest"
                        }
                    }
                }
            }
        }
        stage('K8S Manifest Update') {
            steps {
                git credentialsId: 'github',
                    url: "${env.MANIFESTS_GITHUB_URL}",
                    branch: 'main'
                
                script { 
                    withCredentials([usernamePassword(credentialsId: 'github', usernameVariable: 'GIT_USER', passwordVariable: 'GIT_PASS')]) {
                        def githubUrl = env.MANIFESTS_GITHUB_URL.replace('https://', '')
                        if (isUnix()) {
                            sh "sed -i '' 's/my_local_diary_back:.*\$/my_local_diary_back:${currentBuild.number}/g' k8s/backend-deploy.yml"
                            sh "git add k8s/backend-deploy.yml"
                            sh "git config --global user.name '${env.GIT_USERNAME}'"
                            sh "git config --global user.email '${env.GIT_EMAIL}'"
                            sh "git commit -m '[UPDATE] ${currentBuild.number} image versioning'"
                            sh "git push https://${GIT_USER}:${GIT_PASS}@${githubUrl} main"
                        } else {
                            bat "powershell -Command \"(Get-Content k8s/backend-deploy.yml) -replace 'my_local_diary_back:.*', 'my_local_diary_back:${currentBuild.number}' | Set-Content k8s/backend-deploy.yml\""
                            bat "git add k8s/backend-deploy.yml"
                            bat "git config --global user.name '${env.GIT_USERNAME}'"
                            bat "git config --global user.email '${env.GIT_EMAIL}'"
                            bat "git commit -m \"[UPDATE] ${currentBuild.number} image versioning\""
                            bat "git push https://%GIT_USER%:%GIT_PASS%@${githubUrl} main"
                        }
                    }
                }
            }
        }
    }
```
</details>

## 🧱 DDD
### 🧩 도메인 도출
<img width="1117" alt="스크린샷 2025-05-02 오후 6 05 44" src="https://github.com/user-attachments/assets/eb487671-fb52-4800-b4be-19dc89b54e18" />

### 📦 Bounded Context
<img width="1099" alt="스크린샷 2025-05-02 오후 6 07 28" src="https://github.com/user-attachments/assets/c228d2e9-618d-46dc-bb68-1ed582a2c548" />


### 🔗 연관 관계
<img width="1289" alt="스크린샷 2025-05-02 오후 6 07 55" src="https://github.com/user-attachments/assets/a707ea82-fa65-4532-9187-48b31f56022a" />


## 🗂 ERD
<img width="931" alt="스크린샷 2025-05-02 오후 6 00 18" src="https://github.com/user-attachments/assets/95a3671f-72d7-4c9d-8951-249729eaaf19" />


## 📝 팀원별 회고 모음

### 🙋‍♀️ 팀원 이혜영 - @Hailyee

- **이번 프로젝트에서 맡은 역할**
 - 1. 프론트엔드 구현 
    - figma로 ui/ux설계
    - 공통컴포넌트 - userprofile.vue, sidebar.vue ( 사용자 정보를 불러와야하는 컴포넌트인 경우에는 pinia를 도입하여 상태관리 )
    - 랜딩페이지, 스탬프 페이지 등

 - 2. 백엔드 구현 ( 검색을 통한 사용자 조회, 팔로우 및 알람 저장/생성/삭제 기능 , 팔로워/팔로잉 수 및 목록 조회 등 )
    - 팔로우 시 sse를 이용한 알람 실시간 통신
    - 백엔드와 프론트엔드 연결 시 전반적인 cors처리 설정(WebSecurityConfig.java)




- **잘한 점**
  - Pinia를 활용한 전역 상태 관리 : 기본적으로 userStore.js에서 항상 token을 저장해서 userStore.token으로 불러와 백엔드에 요청을 보낼 때 header에 담아 보내면 인증을 할 수 있었다. 
  - 또한 팔로우 알람을 구현할 떄도, pinia를 활용하여 notificationStore.js에서 따로 알림관련 정보를 관리하니 더 수월하게 짤 수 있었다. 
  - 서버로부터 실시간 이벤트를 받아오기 위한 eventSource 객체를 활용했다. 지정한 URL로 연결을 열어서, 서버가 보내는 이벤트 스트림을 수신하고 close()를 호출하면 네트워크 연결을 안전하게 종료할 수 있었다. 이 때 eventSource는 기본적으로 HTTP 요청 헤더를 마음대로 수정할 수 없다는 제한이 있어서, URL 쿼리스트링(?token=${token}) 방식으로 토큰을 보냈다. (예: http://localhost:8080/api/follow/stream?token=abcd1234)




- **아쉬운 점**

  - 역할분담이 애매하더라도 계획적으로 기능 명세서 등을 세웠다면 좀 더 체계적으로 돌아갔을텐데, 그러한 부분을 내가 주도하지 않아서 조금 아쉬웠다. 

  - 우리 팀은 배포를 한 명이 담당하여 해당 팀원이 배포에 어려움을 겪을 때 뭔가 도와줄 수 있는 방법이 없어 보여서 미안했다. 

  - 마감기간이 다가올수록 pr을 대충 확인했다.

  - 또한 로그인, 인증 과정에 대한 이해도가 낮았다.


- **배운 점**

  - 전반적으로 프론트, 백 연결 방법 그리고 새롭게 배운 기술로는 pinia, sse 로 도전해본 경험이 의미 있었다.



- **다음 프로젝트에 적용하고 싶은 점**

  - 내가 좀 더 계획적인 사람이 되어서, 다음 최종 프로젝트 때에는 효율적으로 돌아가게 하고 싶다. 

  - 또한 알림기능은 양방향성이 아니어도 되어서 sse를 선택했던 것인데,  
sse를 해보니 websocket도 다음에 채팅기능 같은 것이 필요하다면 배워보고픈 생각이 들었다.                                    

---

### 🙋‍♀️ 권민수 - @mins00kwon

- **이번 프로젝트에서 맡은 역할**
  - 프론트엔드 구현(커스텀 마커, 게시글, 마이페이지 캘린더)
  - 백엔드 구현(카카오 로그인, 게시글 조회, 좋아요 , 댓글, 캘린더)

- **잘한 점**
  - 카카오 로그인, 네이버 지도 Api 등등 처음 다뤄보는 기능들이 많았음. 처음에는 굉장히 막막하게 느껴졌으나, 자료를 찾아보면서 이해도를 높이고 결국 구현에 성공함. 
  - 커스텀 마커의 UI를 재미있게 꾸밈

- **아쉬운 점**
  - 일부 기능이 미구현 된 채로 시연하게 된 점이 크게 아쉬움. 프론트엔드 개발자와 백엔드 개발자가 달라서 프론트 코드를 이해하고 수정하는데 많은 시간이 소요됨. 
  - 구현은 되었더라도 로직적으로 비효율적인 부분들이 잇음
  - 프로세스 전체에 대한 포괄적인 이해와 구체적인 계획을 기반으로 움직이는 것이 아니라, 그때 그때 해야할 것 같은 것을 하면서 프로젝트를 진행함. 

- **배운 점**
  - 안되는건 없다. 일단 부딪히고, 공부하면 뭐든 된다. 
  
- **다음 프로젝트에 적용하고 싶은 점**
  - 도메인 분배를 잘 하여 같은 부분에 대한 프론트와 백 개발을 한 명이 하도록
  - 프로젝트 조율에 적극족으로 임하고 싶음. 이번 프로젝트때는 다들 나보다 개발 능력도 뛰어나고, 다들 열심히 하시니 내가 조율을 할 필요도 없고, 이런 저런 말을 하기 민망하게 느껴지기도 했음. 하지만 이번 프로젝트를 마치며 팀원간 소통의 측면에서 아쉬움이 남았음. 비록 개발 능력이 조금 떨어지더라도, 필요한 정보를 공부하고, 팀원들에게 물어보며 프로젝트 조율을 맡아보고 싶음.  
---

### 🙋‍♀️ 팀원 정동한 - @rainyday1367

- **이번 프로젝트에서 맡은 역할**
  - 로그인, 로그아웃, 회원가입 구현
  - pinia 회원 store 설계
  - DB 설계
  - SQL 작성

- **잘한 점**
  - 저번에 배운 Spring Security Chain 필터 흐름대로 Jwt 적용을 했던 것
  - Access, Refresh Jwt에서 많이 사용하는 흐름을 넣어본 것
  - Redis를 도입하여 일반 DB보다는 속도가 향상된 로직을 구현한 것

- **아쉬운 점**
  - 토큰 예외처리에 대한 지식 부족
  - 토큰 구현에 대한 시간 분배 부족
  - 배포 때 도메인이 달라진다는 부분을 까먹고 http-only cookie를 적용했던 점
  - UI 개발에 팀원들을 도와줄 때 컴포넌트 나누는 부분이 부족
  - 프론트엔드 개발을 먼저 하여, JSON-server 연동할 때 로직을 복잡하게 하여 팀원들이 헷갈림
  - 주기적인 리뷰를 부족하게 하여 팀원들과 소통을 많이 못해준 점

- **배운 점**
  - 전체적으로 많이 사용하는 Jwt 흐름에 대해 알 수 있었다.
  - Redis를 이제 사용할 수 있게 되어 캐싱 전략에 대해만 공부하면 조금 더 도입할 수 있다.

- **다음 프로젝트에 적용하고 싶은 점**
  - 코드 리뷰를 잘 진행해주기
  - 배포에 대한 부분을 공부하여 배포 담당을 도와주기
  - 로직에 대한 꼼꼼함을 추가하기
  - 도메인 하나를 조금 더 세세하게 로직을 짜놓고 구현하기

---

### 🙋‍♀️ 장시원 - @swjang7269

- **이번 프로젝트에서 맡은 역할**
  - 젠킨스와 아르고cd, docker를 이용한 CI / CD 설계
  - 게시글 관련 프론트엔드 UI 설계 및 페이지네이션
  - 스탬프, 뱃지 관련 백엔드 구현
 
- **잘한 점**
  - 젠킨스와 아르고, 도커를 활용하여 시스템 아키텍처를 설계한 점
  - 로그를 활용하여 배포시 발생한 에러 위치를 잡은 점
  - cqrs 계층 구조를 지켜 로직을 처리한 점
  - 사용성을 고려하여 이미지리스트와 게시글 리스트에 네비게이션을 제공한점

- **아쉬운 점**
  - 배포 환경을 설정하느라 개발에 많은 시간을 쓰지 못한 점
  - 프로젝트에 많은 참여를 하지 못해 이해도가 부족한 점
  - 배포 환경을 고려하지 않고 개발을 진행한 점
 
- **배운 점**
  - 로컬 개발 환경과 배포 환경의 차이점 -> 개발 시 고려해야할 사항
  - CORS 문제 발생 시 해결 방법
  - CI / CD 설계
 
- **다음 프로젝트에 적용하고 싶은 점**
  - 코드 리뷰에 더 적극적으로 참여하여 다른 팀원들의 코드에 대한 이해도를 높이기
  - 외부 api 활용에 좀 더 참여
  - 배포 환경을 고려하여 개발하기

---

### 🙋‍♀️ 한석현 - @Hancoal

- **이번 프로젝트에서 맡은 역할**
  - 프론트엔드 UI 전체 설계 및 구현 (Vue3 + Vuetify)
  - Naver Maps API와 장소 등록 기능 개발
  - 사진 업로드 및 썸네일 이미지 관리
  - 게시글/일기 통합 등록 및 MyBatis 기반 백엔드 연동

- **잘한 점**
  - 사용자의 입력 흐름을 고려해 직관적인 UX를 구성함
  - 지도 기반 위치 등록 기능에서 장소 검색과 커스텀 마커를 완성도 높게 구현
  - 오류 발생 시 빠르게 디버깅하고 사용자 친화적인 에러 핸들링을 일부 적용함

- **아쉬운 점**
  - Axios 에러 핸들링이 일관되지 않아, 에러 메시지를 사용자에게 명확히 전달하지 못한 부분이 있었음
  - 컴포넌트 재사용성을 고려한 설계가 부족해 유지보수가 어려운 구조가 일부 존재함
  - 초반 요구사항 정리에 시간을 충분히 들이지 못해 일부 흐름이 중간에 바뀌었음

- **배운 점**
  - Pinia의 `store` 구조 설계 및 활용법
  - Composition API에서의 코드 분리 및 재사용 방식
  - Spring Boot + MyBatis로 multipart/form-data 처리하는 백엔드 로직
  - JWT 인증 처리 흐름과 토큰 만료에 따른 갱신 방식

- **다음 프로젝트에 적용하고 싶은 점**
  - 기획 단계에서 Figma 등으로 와이어프레임을 먼저 정리하고 공유할 것
  - Axios interceptor를 활용해 공통 에러 핸들링 구조 확립
  - 폴더 구조를 도메인 중심으로 재정비하여 유지보수 용이성 확보
  - 공통 UI 컴포넌트는 초기에 별도 폴더로 분리하여 재사용성을 높이기
---

### 🙋‍♀️ 정민선 - @minsun24

- **이번 프로젝트에서 맡은 역할**
  - Figma를 활용한 전체 UI/UX 기획 및 설계
  - Naver Cloud Maps API를 활용해 지도 렌더링 UI 구
  - geocoder 서브모듈을 사용한 도로명 주소 → 좌표 검색 기능 개발 
  - Naver Search API를 백엔드와 연동해 키워드 기반 장소 검색 기능 구현
  - Vue + Pinia를 이용한 회원 상태 및 UI 상태 전역 관리
  - 사용자 라우팅 구조 설계 및 로그인/로그아웃 흐름 구현
  - AWS S3를 이용한 이미지 업로드 설정 및 환경 구성
  - 관리자 신고 및 규제 처리 기능 구현


- **잘한 점**
  - 팀 내 API 명세 및 응답 구조를 일관되게 유지하여 개발 협업 효율 향상
  - GlobalExceptionHandler를 활용한 예외 처리 체계화
  - 전역 상태(Pinia)를 효율적으로 활용하여 컴포넌트 간 상태 공유 및 UI 흐름 안정화

- **아쉬운 점**
  - 개발 일정 및 리소스 부족 등의 이유로 인터랙션 및 스타일 세부 요소들이 일부 미완성된 점이 아쉬웠음
  - PR(풀 리퀘스트) 내용을 더 꼼꼼하게 확인했더라면 코드 품질이 높아졌을 것
  - Axios 에러 핸들링에서 예외 케이스(권한 없음, 서버 오류 등)를 더 세분화했으면 좋았을 것
  
- **배운 점**
  - Pinia를 활용한 상태 관리 설계 패턴
  -  AWS S3 환경 구성 및 이미지 업로드 흐름
  -  지도 기반 API 설계 및 프론트–백 연동 방식
  -  JWT 인증 처리 흐름과 토큰 만료에 따른 갱신 방식


- **다음 프로젝트에 적용하고 싶은 점**
  - 서비스 기획서/기능 정의서를 더 명확히 작성하고 시작하기
  - 기능 구현에 앞서 사용자 흐름과 주요 시나리오를 먼저 정의하고, 이에 따라 기능의 우선순위를 체계적으로 설정해 개발 진행하기
  - 정기적인 코드 리뷰를 습관화하여 코드 품질을 높이고 오류를 조기에 발견하기
  - 작업 분담 시 담당 도메인과 마감 기한을 명확히 정의하고 팀원 간 공유 체계 마련하기
 

---

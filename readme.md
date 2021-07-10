## gradle 복습

### 요구사항

#### 1.루트 디렉토리에 "web", "server", "comp" 총 3개의 디렉토리를 만들어야 한다.

#### 2. 각 디렉토리 안에 폴더를 만들면 [디렉토리 이름-폴더 이름] 으로 프로젝트가 생성되어야 한다.

#### 3. 최종적으로 생성된 프로젝트 안에는

<ul>
<li>src/main/java/{패키지 이름}</li>
<li>src/main/resources</li>
<li>src/test/java/{패키지 이름}</li>
<li>src/test/resources</li>
</ul>
들이 생성되어야 한다.

#### 4. 생성된 프로젝트의 최상단 루트에는 "build.gradle" 파일이 생성되어야 한다.

#### 5. 루트 디렉토리의 "build.gradle" 에는 다음과 같은 사항이 들어가야 한다.

<ul>
<li>
빌드스크립트
    <ul>
        <li>build.gradle 파일들에 사용될 변수들을 설정해야 한다. 스프링 버전 변수, 스프링 부트 변수, 롬복 변수들이 있다.</li>
        <li>리파지토리를 설정해야 한다.</li>
        <li>클래스경로 의존성을 추가해야 한다. (스프링 부트 변수:spring-boot-gradle-plugin:스프링 버전 변수)</li>
    </ul>

</li>
<br/>

<li>
모든 프로젝트들에 대해 
    <ul>
        <li>그룹을 설정해야 한다.</li>
        <li>버전을 설정해아 한다.</li>
    </ul>
</li>
<br/>

<li>
서브(하위)프로젝트들에 대해 
    <ul>
        <li>플러그인을 설정해야 한다. java, 스프링 부트 변수, io.spring.dependency-management, idea 를 설정한다.</li>
        <li>리파지토리를 설정해야 한다.</li>
        <li>configurations 를 설정해야 한다.</li>
        <li>의존성을 설정해야 한다.</li>
    </ul>
    
</li>
</ul>

### 이 요구사항 대로 settings.gradle, build.gradle 작성해보기.

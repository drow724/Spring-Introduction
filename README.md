# Spring-Introduction
Spring Boot, Web MVC, DB Access Technology Learned by Code

프로젝트 환경설정

스프링 부트 스타터 사이트로 이동해서 스프링 프로젝트 생성
https://start.spring.io

프로젝트 선택

  Project: Gradle Project
  
  Spring Boot: 2.3.xLanguage: Java
  
  Packaging: Jar
  
  Java: 11
  
  Project Metadata
  
  groupId: hello
  
  artifactId: hello-spring
  
  Dependencies: Spring Web, Thymeleaf

Gradle 전체 설정

build.gradle

plugins {

id 'org.springframework.boot' version '2.3.1.RELEASE'

id 'io.spring.dependency-management' version '1.0.9.RELEASE'

id 'java'

}

group = 'hello'

version = '0.0.1-SNAPSHOT'

sourceCompatibility = '11'

repositories {

mavenCentral()

}

dependencies {

implementation 'org.springframework.boot:spring-boot-starter-thymeleaf'

implementation 'org.springframework.boot:spring-boot-starter-web'

testImplementation('org.springframework.boot:spring-boot-starter-test') {

exclude group: 'org.junit.vintage', module: 'junit-vintage-engine'

  }

}

test {

useJUnitPlatform()

}

동작 확인
기본 메인 클래스 실행
스프링 부트 메인 실행 후 에러페이지로 간단하게 동작 확인( http://localhost:8080)

IntelliJ Gradle 대신에 자바 직접 실행
최근 IntelliJ 버전은 Gradle을 통해서 실행 하는 것이 기본 설정이다. 이렇게 하면 실행속도가 느리다. 
다음과 같이 변경하면 자바로 바로 실행해서 실행속도가 더 빠르다.

Preferences Build, Execution, Deployment Build Tools Gradle

Build and run using: Gradle IntelliJ IDEA

Run tests using: Gradle IntelliJ IDEA

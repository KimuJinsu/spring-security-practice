# Spring Security Project 🚀

이 프로젝트는 **Spring Boot 3**을 기반으로 **Spring Security**의 주요 개념과 기능들을 학습하는 내용을 담고 있습니다. 인증, 권한 설정, URL 접근 제어 등의 다양한 보안 기능을 구현하며, `ch2_1`부터 `ch8_1`까지 단계별로 학습을 진행했습니다.

## 개발 환경 🛠️
- **Java 버전**: 17
- **Spring Boot**: 3.x
- **데이터베이스**: H2 (임베디드 DB 사용), MySQL
- **빌드 툴**: Maven

## Spring Security란? 🔐

**Spring Security**는 Java 애플리케이션의 보안을 강화하는 강력한 프레임워크로, 다음과 같은 기능을 제공합니다:
- **인증 (Authentication)**: 사용자가 누구인지 확인하는 기능
- **인가 (Authorization)**: 특정 기능이나 데이터에 접근할 수 있는 권한을 부여하는 기능
- **보안 설정**: URL 접근 제한, 세션 관리, CSRF 보호 등의 웹 애플리케이션 보안 기능 제공

Spring Security는 다양한 인증 방식과 권한 제어를 지원하며, **Spring**과의 높은 호환성 덕분에 널리 사용되고 있습니다.

## 진행 내용 요약 📘

### 1. Spring Security 기본 설정
- **기본 인증 설정**: `SecurityFilterChain`과 `HttpSecurity`를 사용하여 HTTP Basic 인증을 구성했습니다.
- **URL 접근 제어**: `requestMatchers`를 활용해 특정 URL 패턴에 대한 접근 제어를 설정했습니다.

### 2. In-Memory 인증 🗝️
- **InMemoryUserDetailsManager**: 메모리 기반으로 사용자 정보를 관리하고, 사용자마다 다른 역할(`ADMIN`, `MANAGER` 등)을 부여했습니다.

### 3. 정규 표현식 URL 패턴 매칭 🔍
- **정규 표현식 매칭**: `/product/{code:^[0-9]*$}` 패턴과 같은 정규 표현식을 활용해 URL 접근 제어를 설정했습니다. `requestMatchers`는 Spring Boot 3에서 정규 표현식을 인식하도록 확장되었습니다.

### 4. 권한 및 역할 기반 접근 제어 🛡️
- **역할 부여 및 접근 제어**: 특정 역할(`hasRole`, `hasAuthority`)에 따라 접근을 제한하는 방법을 학습했습니다.

### 5. CSRF 보호 설정 🔒
- **CSRF 비활성화**: REST API 개발과 같은 경우에 CSRF 보호를 비활성화(`csrf().disable()`)하여 설정했습니다.

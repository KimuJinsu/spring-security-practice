
# 🚀 Spring Security Project

이 프로젝트는 **Spring Boot 3**을 기반으로 **Spring Security**의 주요 개념과 기능을 학습하고 실습한 내용을 담고 있습니다.  
단계별로 인증, 권한 설정, URL 접근 제어 등 다양한 보안 기능을 구현하며, Spring Security의 원리를 직접 체험했습니다.  

---

## 🛠️ 개발 환경

- **Java 버전**: 17
- **Spring Boot**: 3.x
- **데이터베이스**: H2 (임베디드 DB 사용), MySQL
- **빌드 툴**: Maven

---

## 🔐 Spring Security란?

**Spring Security**는 Java 애플리케이션 보안을 강화하기 위한 강력한 프레임워크입니다.  
다음과 같은 주요 보안 기능을 제공합니다:

- **인증 (Authentication)**: 사용자의 신원을 확인하는 기능.
- **인가 (Authorization)**: 사용자에게 특정 리소스 접근 권한을 부여하는 기능.
- **보안 설정**: URL 접근 제어, 세션 관리, CSRF 보호 등의 웹 보안 기능.

Spring Security는 다양한 인증 방식과 권한 제어를 지원하며, **Spring Framework**와의 높은 호환성을 바탕으로 널리 사용되고 있습니다.

---

## 📘 진행 내용 요약

### 1. Spring Security 기본 설정
- `SecurityFilterChain`과 `HttpSecurity`를 사용하여 **HTTP Basic 인증**을 설정.
- `requestMatchers`를 활용해 특정 URL 패턴에 대한 접근 제어를 구현.

### 2. In-Memory 인증 🗝️
- **InMemoryUserDetailsManager**를 사용해 메모리 기반으로 사용자 정보를 관리.
- 사용자마다 역할(`ADMIN`, `MANAGER` 등)을 부여하고, 해당 역할에 따라 접근을 제한.

### 3. 정규 표현식 URL 패턴 매칭 🔍
- **정규 표현식 매칭**을 활용하여 URL 접근 제어 설정.
- 예를 들어, `/product/{code:^[0-9]*$}`와 같은 패턴을 정의해 숫자로 구성된 코드만 접근 가능하도록 제한.

### 4. 권한 및 역할 기반 접근 제어 🛡️
- **`hasRole`와 `hasAuthority`**를 사용하여 역할 및 권한 기반 접근 제어를 구현.
- 사용자에게 부여된 역할에 따라 특정 리소스 접근 가능 여부를 설정.

### 5. CSRF 보호 설정 🔒
- REST API 개발 시, 필요에 따라 CSRF 보호를 **비활성화(`csrf().disable()`)**.
- CSRF 보호를 비활성화하면 클라이언트와 서버 간의 상태를 관리하는 데 유용하며, 비상태적인 RESTful 서비스를 지원.

---

## 🎯 학습 포인트

1. **인증과 인가의 차이점 이해**:
   - 인증(Authentication)은 사용자가 누구인지 확인하는 작업.
   - 인가(Authorization)는 특정 리소스에 대한 접근 권한을 확인.

2. **Spring Boot 3과 Spring Security의 통합**:
   - 최신 Spring Boot 3의 기능과 개선 사항을 활용한 보안 설정.

3. **실무에 활용할 수 있는 보안 패턴 학습**:
   - 역할 및 권한 기반 접근 제어.
   - REST API 보안을 위한 CSRF 보호와 비활성화 전략.

---

이 프로젝트는 **Spring Security**의 핵심 개념을 이해하고, 이를 실무에서 적용하기 위한 기초를 다질 수 있는 실습 프로젝트입니다.  
Spring Boot와 함께 제공되는 보안 설정의 유연성을 경험하며, 더 나은 애플리케이션 보안을 구현할 수 있는 능력을 키우는 데 중점을 두었습니다. 🚀

<div align="center">

# Weather WebApp

[Demo Online](#demo-online) • [Instalação](#instalação) • [Tecnologias](#tecnologias)

![Java](https://img.shields.io/badge/Java-17-ED8B00?logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.5.5-6DB33F?logo=springboot&logoColor=white)
![Thymeleaf](https://img.shields.io/badge/Thymeleaf-templates-005F0F?logo=thymeleaf&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-ready-2496ED?logo=docker&logoColor=white)

</div>

---

### Sumário
- [Introdução](#introdução)
- [Demo Online](#demo-online)
- [Pré-requisitos](#pré-requisitos)
- [Instalação](#instalação)
- [Tecnologias](#tecnologias)
- [Estrutura do Projeto](#estrutura-do-projeto)

# Introdução

**Weather WebApp** é uma aplicação Spring Boot Web que consome a [WeatherAPI](https://www.weatherapi.com) para exibir informações meteorológicas, com as páginas renderizadas no servidor via **Thymeleaf**.

# Demo Online

- Endpoint da aplicação (Render): [springboot-weather-webapp.onrender.com](https://springboot-weather-webapp.onrender.com)
- Página do projeto (Vercel): [springboot-weather-webapp.vercel.app](https://springboot-weather-webapp.vercel.app)

# Pré-requisitos

- **JDK 17**;
- Uma chave de API da [WeatherAPI](https://www.weatherapi.com) (gratuita), para integração dos dados meteorológicos;
- Opcional: **Docker**, caso prefira rodar via container.

# Instalação

Clone o repositório:

```sh
git clone https://github.com/cmarinho-dev/spring-weather-webapp.git
cd spring-weather-webapp
```

Rode a aplicação com o Gradle Wrapper:

```sh
# Linux/macOS
./gradlew bootRun

# Windows
gradlew.bat bootRun
```

A aplicação sobe, por padrão, em `http://localhost:8080`.

### Via Docker

O projeto já inclui um `Dockerfile` pronto para build e execução em container:

```sh
docker build -t spring-weather-webapp .
docker run -p 8080:8080 spring-weather-webapp
```

# Tecnologias

- **Java 17**;
- **Spring Boot 3.5.5**;
- **Spring Web** — camada HTTP/MVC;
- **Spring Data JPA** — persistência de dados;
- **Spring Cloud OpenFeign** — cliente HTTP declarativo, usado para consumir a WeatherAPI;
- **Thymeleaf** — motor de templates server-side;
- **H2 Database** — banco em memória, em runtime;
- **Spring Boot DevTools** — recarregamento automático em desenvolvimento;
- **JUnit 5** — testes.

# Estrutura do Projeto

```
spring-weather-webapp/
├── src/main/           # Código-fonte da aplicação (Java + templates Thymeleaf)
├── gradle/wrapper/       # Gradle Wrapper
├── build.gradle.kts     # Configuração do build e dependências
├── settings.gradle.kts
└── Dockerfile            # Build/execução em container
```

---

<div align="center">

Feito com Spring Boot + Thymeleaf, consumindo dados da WeatherAPI.

</div>

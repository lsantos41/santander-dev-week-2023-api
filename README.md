# Santander 2025 - Ciência de Dados com Python

Fork da API da Santander Dev Week 2023 construída em Java 17 com Spring Boot 3.

## Principais Tecnologias
 - **Java 17**: Utilizaremos a versão LTS mais recente do Java para tirar vantagem das últimas inovações que essa linguagem robusta e amplamente utilizada oferece;
 - **Spring Boot 3**: Trabalharemos com a mais nova versão do Spring Boot, que maximiza a produtividade do desenvolvedor por meio de sua poderosa premissa de autoconfiguração;
 - **Spring Data JPA**: Exploraremos como essa ferramenta pode simplificar nossa camada de acesso aos dados, facilitando a integração com bancos de dados SQL;
 - **OpenAPI (Swagger)**: Vamos criar uma documentação de API eficaz e fácil de entender usando a OpenAPI (Swagger), perfeitamente alinhada com a alta produtividade que o Spring Boot oferece;
 - **Railway**: facilita o deploy e monitoramento de nossas soluções na nuvem, além de oferecer diversos bancos de dados como serviço e pipelines de CI/CD.

## Como instalar a API localmente (Windows)

✅  Clonar o repositório
```bash
git clone https://github.com/digitalinnovationone/santander-dev-week-2023-api
```
```bash
cd santander-dev-week-2023-api
```

✅  Instalar dependências
- Instalar o Java 17 (JDK 17)
- Baixe o JDK 17 (Windows):
```bash
https://adoptium.net/temurin/releases/?version=17
```
- Escolha: Temurin 17 (LTS) – x64 – MSI Installer
- Instale clicando em “Next, Next, Finish”
- Verificar versão Java
```bash
  java -version
```
- A resposta deve ser algo como:
    `openjdk version "17.0.x"`
  
  
✅  Crie um arquivo chamado "pom.xml" (sem aspas) no diretório raiz (santander-dev-week-2023-api)
```javascript
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<!-- O SPRING BOOT DEFINE TODAS AS VERSÕES DAS DEPENDÊNCIAS -->
	<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
		<version>3.0.2</version>
		<relativePath/>
		<!-- lookup parent from repository -->
	</parent>
	<groupId>me.dio</groupId>
	<artifactId>santander-dev-week-2023-api</artifactId>
	<version>0.0.1-SNAPSHOT</version>
	<name>santander-dev-week-2023-api</name>
	<description>Santander Dev Week 2023 API</description>
	<properties>
		<java.version>17</java.version>
	</properties>
	<dependencies>
		<!-- SPRING WEB -->
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>
		<!-- SPRING DATA JPA -->
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-jpa</artifactId>
		</dependency>
		<!-- H2 DATABASE -->
		<dependency>
			<groupId>com.h2database</groupId>
			<artifactId>h2</artifactId>
			<scope>runtime</scope>
		</dependency>
		<!-- Lombok -->
		<dependency>
			<groupId>org.projectlombok</groupId>
			<artifactId>lombok</artifactId>
			<optional>true</optional>
		</dependency>
		<!-- TESTES -->
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
		</dependency>
		<!-- OPENAPI / SWAGGER -->
		<dependency>
			<groupId>org.springdoc</groupId>
			<artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
			<version>2.5.0</version>
		</dependency>
	</dependencies>
	<build>
		<plugins>
			<!-- Plugin do Spring Boot -->
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
			</plugin>
		</plugins>
	</build>
</project>

```

✅  Instalar o Maven
- Baixe o Maven ZIP:
```bash
https://maven.apache.org/download.cgi
```
- Escolha: Binary zip archive
- Crie a pasta "Apache\maven" (sem aspas) em "C:\Program Files".
  Ficando da seguinte maneira:
```bash
 C:\Program Files\Apache\maven
```
- Extraia o conteúdo baixado do Maven para `"C:\Program Files\Apache\maven"`

 ## Variáveis de Ambiente
- Crie a variável de ambiente:
  `MAVEN_HOME`
 - Adicione o path: 
  `C:\Program Files\Apache\maven`

- Adicione ao PATH às varáveis de ambiente:
`C:\Program Files\Apache\maven\bin`

## Instalar Chocolatey
- Abra o Powershell como administrador e rode o seguinte comando:
```bash
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

- Abra um terminal como administrador e execute o seguinte comando:
```bash
choco install maven
```

## Executando a API

- Para acessar à API, abra um terminal e acesso o diretório do projeto:
`cd santander-dev-week-2023-api`
- Rode os seguintes comandos:
```bash
   mvn clean install
```
```bash
   mvn spring-boot:run
```
 
 



## Documentação da API (Swagger)

Acesso ao Swagger
```bash
http://localhost:8080/swagger-ui.html
```

## Referência

 - [Maven](https://maven.apache.org/download.cgi)
 - [Chocolatey](https://chocolatey.org/install)


# Portfolio Tracking Api in spring boot

This is portfolio tarcking rest api build in spring boot used to get trading in stock market.




## Authors

- [@ingleajay]


  
## Functionality

1. Adding Trades
2. Remove All Trades
3. Remove Trades by Id
3. Update Trades
4. Fetching Portfolio
5. Fetching Holdings
6. Fetching Returns
7. Buy Trades
8. Sell Trades




  
## Create project

Create project with spring boot

```bash
 https://start.spring.io/
```


## Add Swagger to project (openapi)

Swagger UI allows your development team or your end consumers to visualize and interact with the API’s resources without having any of the implementation logic in place. It’s automatically generated from your OpenAPI (formerly known as Swagger)

```bash
 http://localhost:8081/swagger-ui/index.html?

 http://localhost:8081/v3/api-docs/
```


## Dependency in pom.xml

Add all required dependency

```bash

<dependency>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-data-jpa</artifactId>
</dependency>

<dependency>

		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-web</artifactId>
</dependency>

<dependency>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-devtools</artifactId>
		<scope>runtime</scope>
		<optional>true</optional>
</dependency>
	
<dependency>
		<groupId>mysql</groupId>
		<artifactId>mysql-connector-java</artifactId>
		<scope>runtime</scope>
</dependency>

<dependency>
	  <groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-test</artifactId>
		<scope>test</scope>
</dependency>

<dependency>
		<groupId>javax.validation</groupId>
		<artifactId>validation-api</artifactId>
</dependency>

<dependency>
		<groupId>org.hibernate</groupId>
		<artifactId>hibernate-validator</artifactId>
		<version>6.1.5.Final</version>
</dependency>

<dependency>
		<groupId>org.springdoc</groupId>
		<artifactId>springdoc-openapi-ui</artifactId>
		<version>1.2.32</version>
</dependency>

```
## Resource : Application.properties


```bash
server.port = 8081
spring.datasource.name=ds
spring.datasource.url=jdbc:mysql://localhost:3306/portfolio?
spring.datasource.username=root
spring.datasource.password=XXXXXXXX
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.properties.hibernate.dialect = org.hibernate.dialect.MySQL8Dialect
spring.jpa.hibernate.ddl-auto=update

springdoc.swagger-ui.operationsSorter=method
```

## API Reference

#### Adding Trades

```http
  POST /api/addtrades
```

#### Delete All Trades

```http
  DELETE /api/removetrades
```
#### Delete Trade By Id

```http
  DELETE /api/removetrade/{tradeid}
```

| Parameter | Type     | Description                         |
| :-------- | :------- | :--------------------------------   |
| `tradeid` | `Integer`| **Required**. Id of trade to delete |

#### Update Trade By Id

```http
  PUT /api/updatetrade/{tradeid}
```
| Parameter | Type     | Description                         |
| :-------- | :------- | :--------------------------------   |
| `tradeid` | `Integer`| **Required**. Id of trade to update |

#### Buy Trade 

```http
  POST /api/buytrade/{tradeid}
```
| Parameter | Type     | Description                            |
| :-------- | :------- | :--------------------------------      |
| `tradeid` | `Integer`| **Required**. Id of trade to buy trade |

#### Sell Trade 

```http
  POST /api/selltrade/{tradeid}
```
| Parameter | Type     | Description                             |
| :-------- | :------- | :--------------------------------       |
| `tradeid` | `Integer`| **Required**. Id of trade to sell trade |

#### Fetch Holding Trade 

```http
  GET /api/fetchholdtrade
```

#### Fetch All Trade 

```http
  GET /api/fetchtrade
```

#### Fetch Return  

```http
  GET /api/fetchreturn
```

## Screenshots

[Swagger ui ]

https://www.canva.com/design/DAEojXfPSls/op30Xxl68PJhmdR-abs-3g/view?utm_content=DAEojXfPSls&utm_campaign=designshare&utm_medium=link&utm_source=publishsharelink


# ☕ Java-Projects

> Programas orientados a objetos y aplicaciones empresariales en Java

## 📋 Descripción

Colección de **proyectos Java profesionales** enfocados en **programación orientada a objetos (POO)**, **patrones de diseño** y **desarrollo empresarial**. Desde aplicaciones de escritorio hasta APIs REST, todo con arquitectura sólida.

Perfecto para:
- 🎓 Aprender POO en Java
- 🏢 Desarrollar aplicaciones empresariales
- 🏗️ Entender patrones de diseño
- 🔌 Crear APIs y microservicios
- 📱 Desarrollo de aplicaciones robustas

## 🎯 Contenido Principal

```
Java-Projects/
├── core-concepts/
│   ├── oop/                  # Programación Orientada a Objetos
│   ├── inheritance/          # Herencia y polimorfismo
│   ├── abstraction/          # Clases abstractas
│   ├── encapsulation/        # Encapsulamiento
│   └── interfaces/           # Interfaces
├── design-patterns/
│   ├── creational/
│   │   ├── Singleton.java
│   │   ├── Factory.java
│   │   ├── Builder.java
│   │   └── Prototype.java
│   ├── structural/
│   │   ├── Adapter.java
│   │   ├── Decorator.java
│   │   ├── Facade.java
│   │   └── Proxy.java
│   └── behavioral/
│       ├── Observer.java
│       ├── Strategy.java
│       ├── Command.java
│       └── State.java
├── data-structures/
│   ├── LinkedList.java
│   ├── Stack.java
│   ├── Queue.java
│   ├── BinaryTree.java
│   ├── Graph.java
│   └── HashTable.java
├── algorithms/
│   ├── sorting/
│   ├── searching/
│   ├── graph/
│   └── dynamic_programming/
├── database/
│   ├── jdbc/                 # JDBC y conexiones
│   ├── orm/                  # Hibernate/JPA
│   └── migrations/           # Migraciones
├── web-applications/
│   ├── spring-boot/          # Spring Boot
│   ├── rest-api/             # REST APIs
│   ├── mvc/                  # MVC Pattern
│   └── security/             # Spring Security
├── desktop-apps/
│   ├── javafx/               # JavaFX GUI
│   ├── swing/                # Swing GUI
│   └── games/                # Juegos simples
├── utilities/
│   ├── file-handling/
│   ├── string-processing/
│   ├── json-processing/
│   └── http-client/
├── tests/
│   ├── unit-tests/           # JUnit
│   └── integration-tests/    # Testing
├── pom.xml                   # Maven
└── docs/
```

## 🚀 Características

- ✅ Código limpio y bien estructurado
- ✅ Patrones de diseño implementados
- ✅ Tests unitarios incluidos
- ✅ Documentación exhaustiva
- ✅ Ejemplos prácticos
- ✅ Manejo de excepciones
- ✅ Logging profesional
- ✅ Configuración flexible

## 📦 Requisitos

- **Java 11+**
- **Maven 3.6+** o **Gradle 7.0+**
- **IDE:** IntelliJ IDEA, Eclipse o VS Code

## 🔧 Instalación

```bash
git clone https://github.com/DanAle910/Java-Projects.git
cd Java-Projects

# Con Maven
mvn clean install
mvn spring-boot:run

# Con Gradle
./gradlew build
./gradlew bootRun
```

## 💡 Ejemplos Principales

### 1. Patrón Singleton
```java
public class ConfigManager {
    private static ConfigManager instance;
    
    private ConfigManager() {}
    
    public static synchronized ConfigManager getInstance() {
        if (instance == null) {
            instance = new ConfigManager();
        }
        return instance;
    }
}
```

### 2. Patrón Factory
```java
public class LogisticsFactory {
    public static Transport createTransport(String type) {
        switch(type.toLowerCase()) {
            case "truck":
                return new Truck();
            case "plane":
                return new Plane();
            default:
                throw new IllegalArgumentException("Tipo desconocido");
        }
    }
}
```

### 3. REST API con Spring Boot
```java
@RestController
@RequestMapping("/api/users")
public class UserController {
    
    @Autowired
    private UserService userService;
    
    @GetMapping
    public ResponseEntity<List<User>> getAllUsers() {
        return ResponseEntity.ok(userService.findAll());
    }
    
    @PostMapping
    public ResponseEntity<User> createUser(@RequestBody User user) {
        return ResponseEntity
            .status(HttpStatus.CREATED)
            .body(userService.save(user));
    }
}
```

## 📊 Proyectos Incluidos

### 1. Sistema de Gestión de Usuarios
- CRUD completo
- Validación
- Base de datos

### 2. API REST de Productos
- Spring Boot
- Paginación
- Filtrado avanzado

### 3. Aplicación de Chat
- GUI con JavaFX
- Comunicación en red
- Múltiples usuarios

## 🧪 Testing

```bash
# Ejecutar todos los tests
mvn test

# Test específico
mvn test -Dtest=CalculatorTest
```

## 🤝 Contribuciones

Contribuciones bienvenidas:
- Nuevos proyectos
- Patrones adicionales
- Mejoras en código

## 📄 Licencia

MIT License - Ver [LICENSE](LICENSE)

## 📞 Contacto

- **GitHub:** [@DanAle910](https://github.com/DanAle910)

---

⭐ Si te fue útil, ¡deja una estrella!
# min-bom

## Purpose
Bill of Materials POM that centralizes dependency version management for all min-* projects.

## Guidelines
- **Architecture**: BOM POM - no source code
- **Dependencies**: Manages versions for external and internal dependencies
- **Parent**: min-root (21.0.0)
- **Changes**: Only add/update dependency versions in dependencyManagement
- **Testing**: Test by building projects that import this BOM

## Key Dependencies Managed
- JUnit Jupiter (5.13.1)
- Lombok (1.18.34) 
- Checker Framework (3.49.1)
- Apache Commons IO (2.19.0)
- Internal min-* libraries

## Usage in Projects
```xml
<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>com.olexyn</groupId>
            <artifactId>min-bom</artifactId>
            <version>21.1.0</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
```

## Maintenance
- Keep external dependency versions current
- Coordinate internal min-* library versions
- Version bumps require updating all dependent projects
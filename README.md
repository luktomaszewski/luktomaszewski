```java
package com.github.luktomaszewski;

/**
 * Software engineer · geo geek · running freak.
 */
public final class LukTomaszewski implements SoftwareEngineer, GeoGeek, Runner {

    @Override
    public Profile profile() {
        return Profile.builder()
                .role("Software Engineer")
                .focus("Java", "Kotlin", "DevOps", "GIS")
                .openTo("supervisory board roles in successful companies with good financial results")
                .build();
    }

    @Override
    public Skills skills() {
        return Skills.builder()
                .languages("Java", "Kotlin", "Python")
                .frameworks("Spring Boot", "Hibernate", "Liquibase", "Swagger", "JUnit", "Mockito")
                .databases("PostgreSQL + PostGIS", "Oracle + Spatial", "MSSQL")
                .technologies("Gradle", "ELK", "ActiveMQ", "RabbitMQ", "Git")
                .devOps("Docker", "Kubernetes", "Helm", "Terraform", "Bicep", "GitLab CI/CD", "Bash/Zsh")
                .cloud("Azure", "AWS")
                .gis("ArcGIS", "FME", "QGIS", "GeoMedia", "GeoServer", "ArcPy", "ogr2ogr",
                     "OGC", "WMS", "WFS", "SLD", "GeoJSON", "LiDAR/LAS")
                .build();
    }

    @Override
    public List<String> hobbies() {
        return List.of("running", "geoscience & GIS", "programming & technologies", "music", "aviation");
    }

    @Override
    public Stream<Repository> contribute(World world) {
        return world.stream()
                .filter(GeoGeek::isGeoAwesome)
                .map(Repository::toGitHub);
    }
}
```

<p align="center">
  <a href="https://roadmap.sh"><img alt="roadmap.sh: backend, spring-boot, java" src="https://roadmap.sh/card/tall/657629265145316d25e4ac0a?variant=dark&roadmaps=backend%2Cspring-boot%2Cjava"></a>
  <a href="https://roadmap.sh"><img alt="roadmap.sh: devops, docker, kubernetes, aws" src="https://roadmap.sh/card/tall/657629265145316d25e4ac0a?variant=dark&roadmaps=devops%2Cdocker%2Ckubernetes%2Caws"></a>
</p>

# Reto2_POO_ServicioMedico

 ### **Fecha:** 19-02-2024

**1.** Relación paciente - cita médica

```mermaid
classDiagram
    direction RL
    class CitaMédica{
        + Pertenencia EPS
        + Prepagada
        + Especialidad
        + Fecha y hora
        + Ubicación
    }
    class Paciente{
        
    }
    Paciente --> CitaMédica : solicita()
```

**2.** Relación paciente - cita médica

```mermaid
classDiagram
    class Paciente{    
    }
    class CitaMédica{
        + Pertenencia EPS
        + Prepagada
        + Especialidad
        + Fecha y hora
        + Ubicación
    }
    class Especialidad{
        + Especialidad CitaMédica
        + Examenes previos
    }
    class EPS{
        + Tipo EPS
        + Afiliado/Beneficiario
        + Cobertura
        + Autorización
    }
    class IPS{
        + Autorización
        + Tipo
        + Servicios
        + Horarios
    }
    class Regimen de Salud{
        + Contributivo/Subsidiado
        + Autorización
    }
    Paciente --> CitaMédica : solicita
    Especialidad --* CitaMédica 
    IPS *--*  EPS 
    EPS *--  CitaMédica 
    Regimen de Salud --* CitaMédica 
```

**3.** Relaciones entre especialidades

```mermaid
classDiagram
    direction LR
    Especialidad <|-- Cardiología 
    Especialidad <|-- Pediatria
    Especialidad <|-- Dermatología
    Especialidad <|-- Ginecología  
    Especialidad <|-- Hematología
    Especialidad <|-- Oftalmología
    Especialidad <|-- Otorrinolaringología  
    Especialidad <|-- Pediatría
    Especialidad <|-- Oncología 
    class Especialidad{
        + Especialidad CitaMédica
        + Examenes previos
    }
    class Cardiología {
      + Historia Clínica
      + Diagnostico
      + Plan de tratamiento
    }
    class Pediatria{ 
      + Historia Clínica
      + Diagnostico
      + Plan de tratamiento
    }
    class Dermatología{
      + Historia Clínica
      + Diagnostico
      + Plan de tratamiento
    }
    class Ginecología {
      + Historia Clínica
      + Diagnostico
      + Plan de tratamiento
    }
    class Hematología{
      + Historia Clínica
      + Diagnostico
      + Plan de tratamiento
    }
    class Oftalmología{
      + Historia Clínica
      + Diagnostico
      + Plan de tratamiento
    }
    class Otorrinolaringología {
      + Historia Clínica
      + Diagnostico
      + Plan de tratamiento
    }
    class Pediatría{
      + Historia Clínica
      + Diagnostico
      + Plan de tratamiento
    }
    class Oncología {
      + Historia Clínica
      + Diagnostico
      + Plan de tratamiento
    }
```

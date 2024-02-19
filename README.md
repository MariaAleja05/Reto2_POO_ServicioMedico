# Reto2_POO_ServicioMedico

 ### **Fecha:** 19-02-2024

**1.** Relación paciente - cita médica

```mermaid
classDiagram
    direction RL
    class CitaMédica{
        + Pertenencia EPS
        + Especialidad
    }
    class Paciente{
        
    }
    Paciente"2" --> "1" CitaMédica : solicita()
```

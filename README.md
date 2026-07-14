# 🎯 Daniel | Blue Team & Threat Detection Portfolio

![Role](https://img.shields.io/badge/Role-IT%20Security%20%26%20Blue%20Team-blue)
![Environment](https://img.shields.io/badge/Environment-Real%20Production-success)
![Focus](https://img.shields.io/badge/Focus-Detection%20Engineering%20%7C%20DFIR-orange)

Bienvenido a mi portfolio profesional de ciberseguridad. Este repositorio centraliza toda la evidencia pública, laboratorios prácticos y documentación técnica generada a lo largo de mi plan de especialización en **Defensa Activa, Ingeniería de Detección y DFIR**.

A diferencia de los entornos simulados tradicionales, la mayor parte de este trabajo ha sido conceptualizada, diseñada y validada utilizando la telemetría, alertas e incidentes analizados en una infraestructura de producción real (Wazuh, FortiGate, Microsoft 365, Active Directory con controladores legados y flota de más de 80 terminales móviles en operativa diaria).

---

## 🛠️ Stack de Tecnologías & Herramientas

| Categoría | Herramientas / Estándares Utilizados |
| :--- | :--- |
| **Frameworks de Trabajo** | MITRE ATT&CK, Pyramid of Pain, Alerting & Detection Strategy (ADS) de Palantir. |
| **Ingeniería de Detección** | Sigma Rule Format (SigmaHQ), `sigma-cli`, Wazuh Decoders/Rulesets. |
| **Forense y Análisis (DFIR)** | Wireshark (análisis de tráfico PCAP), Sysmon (instrumentación de endpoints), Event Viewer, Volatility, Autopsy. |
| **Simulación de Adversarios** | Atomic Red Team (Red Canary) para validación de alertas. |

---

## 📂 Estructura del Repositorio

```text
.
├── 📂 coverage/                    # Evaluaciones de cobertura y visibilidad
│   └── wazuh-attack-coverage.json  # Capa de MITRE ATT&CK Navigator
├── 📂 docs/                        # Filosofía de detección y criterios del SOC
│   └── detection-philosophy.md     # Tolerancia a FPs, criticidad y triage
├── 📂 sigma-rules/                 # Reglas de detección personalizadas (YAML)
│   ├── README.md                   # Documentación de métricas, falsos positivos y tuning
│   └── [reglas-sigma].yml          # Colección de reglas de comportamiento
└── 📂 writeups/                    # Informes y análisis de investigaciones reales
    ├── 01-bruteforce-ipv6-m365.md  # Análisis técnico de un ataque real a tenant cloud
    ├── 02-pcap-analysis.md         # Análisis forense de tráfico de red y balizamiento (C2)
    ├── 03-dfir-report-gap-analysis.md # Ingeniería inversa de amenazas en nuestro entorno
    └── 04-cyberdefenders-reto.md   # Resolución de retos interactivos de endpoint

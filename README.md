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
.
├── 📂 coverage/               # Evaluaciones de cobertura y visibilidad
│   └── wazuh-attack-coverage.json  # Capa de MITRE ATT&CK Navigator
├── 📂 docs/                   # Filosofía de detección y criterios del SOC
│   └── detection-philosophy.md     # Tolerancia a FPs, criticidad y triage
├── 📂 sigma-rules/            # Reglas de detección personalizadas (YAML)
│   ├── README.md              # Documentación de métricas, falsos positivos y tunning
│   └── [reglas-sigma].yml     # Colección de reglas de comportamiento
└── 📂 writeups/               # Informes y análisis de investigaciones reales
├── 01-bruteforce-ipv6-m365.md  # Análisis técnico de un ataque real a tenant cloud
├── 02-pcap-analysis.md         # Análisis forense de tráfico de red y balizamiento (C2)
├── 03-dfir-report-gap-analysis.md  # Ingeniería inversa de amenazas industriales en nuestro entorno
└── 04-cyberdefenders-reto.md   # Resolución detallada de retos interactivos de endpoint

---

## 📈 Proyectos Destacados e Hitos de Aprendizaje

### 1. Ingeniería de Detección Práctica (SigmaHQ ➡️ Wazuh)
Creación, testeo y despliegue de reglas de detección basadas en comportamiento para evadir la obsolescencia de los IOCs estáticos. Cada una de las reglas creadas en la carpeta `/sigma-rules/` incluye un análisis exhaustivo de falsos positivos teóricos y reales identificados en producción.
* **Detección de Movimiento Lateral y Autenticaciones Anómalas:** Reglas específicas para conexiones RDP originadas fuera del rango controlado de nuestra flota de terminales móviles (PDAs).
* **Monitoreo de Infraestructura Crítica:** Control estricto de la creación de nuevos servicios del sistema (T1543.003) en servidores Windows legados.
* **Evasión de Defensa y PowerShell:** Reglas orientadas a interceptar la ejecución de comandos PowerShell codificados en Base64 (T1059.001) a nivel de servidor.

### 2. Análisis de Incidentes en Escenarios Reales (Writeups)
Documentación meticulosa bajo un estándar profesional que detalla no solo la detección de un ataque, sino su mitigación sistemática:
* **Ataque de Fuerza Bruta IPv6 (M365):** Mapeo completo en la matriz ATT&CK (T1110.003 - Password Spraying), análisis de correlación temporal, geolocalización de ASNs atacantes e implementación de políticas de mitigación.
* **Análisis Forense de Red:** Identificación de flujos de beaconing (balizamiento), exfiltración DNS y reconocimiento de tráfico Command & Control (C2) utilizando capturas de paquetes (PCAP).

---

## 🎯 Filosofía de Defensa

> *"Detectar un hash es trivial y molesta poco al atacante; cambiar el costo de su operación detectando sus tácticas, técnicas y procedimientos (TTPs) es lo que realmente nos da la ventaja."* — Adaptado del concepto de Pyramid of Pain (David Bianco).

Mi enfoque técnico se basa en la **Detección de Comportamientos Excepcionales** y la mejora proactiva de la visibilidad corporativa a través de la instrumentación de logs detallados (Sysmon + logs de cortafuegos de frontera), reduciendo el ruido operativo mediante una estricta estrategia de afinación (tunning) para evitar la fatiga por alertas.

---

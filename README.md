# 🛡️ CyberLab Writeups

[![GitHub Pages](https://img.shields.io/badge/pages-live-00d4aa?style=flat-square&logo=github)](https://tomasgj.github.io/cyberlab-writeups/)
[![Estado](https://img.shields.io/badge/estado-completado-3ddc84?style=flat-square)](#-writeups-disponibles)
[![Licencia](https://img.shields.io/badge/licencia-MIT-22d3ee?style=flat-square)](LICENSE)

Documentación de mi laboratorio personal de ciberseguridad.

## 🔗 Writeup publicado

👉 **https://tomasgj.github.io/cyberlab-writeups/**

Versión HTML con diseño completo (o [ver el código fuente](./index.html)).

## 🏗️ Arquitectura del laboratorio

- **Netgate pfSense** — Firewall / Router (192.168.1.1)
- **Windows Server 2022** — Domain Controller AD DS (192.168.1.10)
- **Kali Linux** — Máquina de ataque (192.168.1.20)
- **Red interna:** `Zona-Ataque`
- **Dominio:** `hacklab.local`

## 📚 Writeups disponibles

| # | Título | Fase | Enlace |
|---|--------|------|--------|
| 1 | De invitado a SYSTEM en Active Directory | Reconocimiento → SYSTEM → Defensa GPO | [Ver](https://tomasgj.github.io/cyberlab-writeups/) |

## 🧭 Contenido del writeup

| Sección | Tema |
|---------|------|
| 01 | Introducción y alcance |
| 02 | Topología del laboratorio |
| 03 | Reconocimiento con nmap |
| 04 | Enumeración de usuarios (kerbrute + netexec) |
| 05 | Acceso y movimiento lateral (impacket-psexec) |
| 06 | Análisis de causa raíz |
| 07 | Contramedida defensiva: GPO de bloqueo de CMD |
| 08 | Lecciones aprendidas |
| 09 | Referencias y herramientas |

## 🎓 Lecciones clave

- Kerberos (puerto 88) filtra la existencia de usuarios aunque SMB esté bloqueado.
- Credenciales válidas permiten enumeración completa del dominio.
- PsExec abusa de `ADMIN$` para ejecución remota como SYSTEM.
- Los grupos con privilegios excesivos son el mayor riesgo interno.
- Las GPOs permiten aplicar seguridad segmentada por departamento — pero **complementan**, no sustituyen, el control de accesos.

## 🛠️ Herramientas utilizadas

`nmap` · `kerbrute` · `netexec` · `impacket` · Group Policy Management · pfSense · VirtualBox

## 🚀 Publicar localmente

```bash
git clone https://github.com/TomasGj/cyberlab-writeups.git
cd cyberlab-writeups
python3 -m http.server 8000
# Abrir http://localhost:8000
```

## 📄 Estructura del repositorio

```
cyberlab-writeups/
├── index.html          # Writeup completo (publicado en GitHub Pages)
├── README.md           # Este archivo
├── LICENSE
├── assets/
│   └── img/            # Capturas de evidencia (01-... a 09-...)
└── docs/               # Material de apoyo
```

## ⚠️ Aviso

Todo el contenido es con fines **educativos** en un entorno aislado y controlado.
No se incluyen credenciales reales, datos de terceros ni direcciones de producción.

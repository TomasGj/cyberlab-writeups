# 🛡️ CyberLab Writeups

Documentación de mi laboratorio personal de ciberseguridad.

## 🏗️ Arquitectura del laboratorio

- **Netgate pfSense** — Firewall / Router (192.168.1.1)
- **Windows Server 2022** — Domain Controller AD DS (192.168.1.10)
- **Kali Linux** — Máquina de ataque (192.168.1.101)
- **Red interna:** `Zona-Ataque`
- **Dominio:** `hacklab.local`

## 📚 Writeups disponibles

| # | Título | Fase |
|---|--------|------|
| 1 | Active Directory Attack Path | Reconocimiento → SYSTEM → Defensa GPO |

## 🔗 Ver writeup completo

👉 [Abrir el writeup HTML](./index.html) *(o el enlace de GitHub Pages una vez activado)*

## 🎓 Lecciones clave

- Kerberos (puerto 88) filtra la existencia de usuarios aunque SMB esté bloqueado.
- Credenciales válidas permiten enumeración completa del dominio.
- PsExec abusa de `ADMIN$` para ejecución remota como SYSTEM.
- Los grupos con privilegios excesivos son el mayor riesgo interno.
- Las GPOs permiten aplicar seguridad segmentada por departamento.

## ⚠️ Aviso

Todo el contenido es con fines **educativos** en un entorno aislado y controlado.

# FIWARE Dockers

Stack **FIWARE** desplegado con **Docker Compose** para montar una plataforma IoT/Contexto completa: **Orion Context Broker** (con MongoDB), **Keyrock IdM** + **Wilma PEP Proxy** (seguridad OAuth2), **IoT Agent JSON**, **Cygnus NGSI** (persistencia) + **PostgreSQL**, y herramientas de soporte como **Grafana**, **pgAdmin** y **n8n**.

> Este repositorio está pensado como base reproducible para pruebas, demos y aprendizaje.
---

## Componentes incluidos

- **MongoDB**: base de datos para Orion.
- **Orion Context Broker**: núcleo NGSI (gestión de entidades/contexto).
- **Keyrock (IdM)**: gestión de identidades y OAuth2.
- **Wilma PEP Proxy**: proxy de seguridad delante de Orion (protección con Keyrock).
- **IoT Agent JSON**: registro de dispositivos y traducción IoT → NGSI.
- **Cygnus NGSI**: persistencia/ETL de eventos NGSI hacia bases de datos.
- **PostgreSQL**: almacenamiento para Cygnus.
- **pgAdmin**: administración web de PostgreSQL.
- **Grafana**: visualización/observabilidad (dashboards).
- **n8n**: automatización de flujos y webhooks.

---

## Requisitos

- Docker y Docker Compose (plugin `docker compose`)
- Puertos libres en la máquina (si cambias mapeos, revisa `ports:`)

---

## Puertos por defecto

- Orion: `1026`
- Wilma (PEP Proxy): `1027`
- Keyrock: `3000`
- IoT Agent JSON: `4041` (Northbound), `7896` (Southbound)
- Cygnus: `5080` (API), `5055` (service)
- PostgreSQL: `5432`
- pgAdmin: `88`
- Grafana: `3003`
- n8n: `5678` *(por defecto ligado a 127.0.0.1 para mayor seguridad)*

---

## 📜 Licencia

Este proyecto se distribuye bajo la licencia MIT. Puedes usarlo, modificarlo y distribuirlo libremente citando la fuente.


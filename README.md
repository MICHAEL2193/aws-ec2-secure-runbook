# AWS EC2: Runbook de endurecimiento básico (Ubuntu)

## Objetivo
Provisionar una instancia EC2 Ubuntu, conectarme por SSH y aplicar medidas básicas de seguridad
de forma reproducible (pensado para entornos de laboratorio que se resetean).

## Qué demuestra este proyecto
- Creación de EC2 y configuración de Security Group con exposición mínima
- Conexión SSH y diagnóstico de fallos típicos
- Endurecimiento básico en Linux (actualizaciones, usuario no root, UFW)
- Documentación basada en evidencias (outputs y capturas)

## Arquitectura (alto nivel)
VPC -> Subnet -> EC2 (Ubuntu) -> Security Group (SSH restringido)

## Checklist por sesión

### Sesión 1: Provisionar + SSH
- [ ] Crear EC2 Ubuntu
- [ ] Restringir SSH (22) solo a mi IP
- [ ] Descargar key pair (.pem) y ajustar permisos
- [ ] Conectar por SSH a la instancia
- [ ] Guardar evidencias (comandos + capturas)

### Sesión 2: Hardening básico
- [ ] Crear usuario no root
- [ ] Habilitar UFW y dejar solo lo necesario
- [ ] Aplicar actualizaciones de seguridad
- [ ] Guardar evidencias

### Sesión 3: Troubleshooting (aprendizaje)
- [ ] Documentar 3 fallos comunes y su solución:
  - Timeout por Security Group / IP
  - Permisos incorrectos de la clave (.pem)
  - Usuario incorrecto (ubuntu vs otros)

## Evidencias
(Pega aquí outputs y/o capturas, sin credenciales)
- Comando SSH utilizado (con placeholders)
- `ufw status`
- `ss -tulpn`
- `whoami` / `id`
- Captura del Security Group (inbound rules)

## Notas de seguridad
- No subir al repo: claves `.pem`, Access Keys, tokens, contraseñas.
- Usar placeholders: `<IP_PUBLICA>`, `<REGION>`, `<DNS>`.

## Resumen en inglés (opcional)
(Write 5–8 lines summarizing what you built and validated.)


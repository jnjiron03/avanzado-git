# Changelog

Todos los cambios relevantes de este proyecto se documentan aquí.
Formato basado en [Keep a Changelog](https://keepachangelog.com/es/1.0.0/).

---

## [v1.2] — 2026-04-28

### Fixed
- Estandarizados todos los mensajes de commit al formato convencional (`feat:`, `fix:`, `docs:`)
- Limpieza del historial de commits con `git rebase -i`

---

## [v1.1] — 2026-04-28

### Added
- Configuración del workflow de GitHub Actions en `.github/workflows/validate.yml`
- Validación automática del script Bash con `shellcheck` en cada push a main
- Badge de estado del workflow en el `README.md`

---

## [v1.0] — 2026-04-28

### Added
- Repositorio `avanzado-git` creado en GitHub con autenticación SSH
- Script `script.sh` con comandos básicos de shell
- Archivo `README.md` con descripción del proyecto
- Archivo `config.txt` con parámetros de configuración

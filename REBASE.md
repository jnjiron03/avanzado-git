# Documentación del proceso de Rebase

## ¿Qué es git rebase -i?

`git rebase -i` (rebase interactivo) me permite reescribir el historial de commits
antes de subirlos al repositorio. Es útil para limpiar mensajes confusos, fusionar
commits pequeños que no aportan valor por separado, y dejar el historial más legible.

## Situación inicial

Tenía 5 commits con mensajes poco claros:

| Hash | Mensaje original |
|------|-----------------|
| abc1234 | Arreglos |
| def5678 | Cambios |
| ghi9012 | Actualización de cosas |
| jkl3456 | más cambios |
| mno7890 | listo |

## Acciones realizadas

### Fase 1 — Abrir el rebase interactivo
Ejecuté `git rebase -i HEAD~5` para trabajar con los últimos 5 commits.

### Fase 2 — Elegir qué hacer con cada commit
- Usé `reword` en los commits abc1234 y ghi9012 para cambiar sus mensajes.
- Usé `squash` en def5678, jkl3456 y mno7890 para fusionarlos con el commit anterior.

### Fase 3 — Escribir los nuevos mensajes
Cambié los mensajes para que describan qué se hizo y por qué:
- `feat: añadir archivo de configuración base`
- `feat: añadir parámetros avanzados de configuración`

### Fase 4 — Subir los cambios
Usé `git push --force` porque el historial reescrito no coincide con el remoto.
Este comando sobreescribe el historial remoto, por eso solo lo hago en ramas propias.

## Por qué es importante

Un historial limpio ayuda a cualquier persona del equipo a entender qué cambios
se hicieron y por qué, sin tener que revisar el código línea a línea.

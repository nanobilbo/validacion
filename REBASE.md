# Limpieza de commits con git rebase -i

## Proceso realizado

1. Creo 3 commits con mensajes poco claros: "Arreglos", "Cambios", "Actualización de cosas"
2. Ejecuté `git rebase -i HEAD~3`
3. En el editor, cambié:
   - `pick` → `reword` para mejorar mensajes
   - `pick` → `squash` para fusionar commit 2 con commit 1
4. Reescribí mensajes:
   - Commit 1: "feat: añadir función saludar()"
   - Commit 2 (fusionado): ahora parte del commit 1
   - Commit 3: "docs: añadir función ayuda()"
5. Ejecuté `git push --force origin main`

## Resultado final
- Historial limpio y semántico
- Commits fusionados donde correspondía
- Mensajes claros siguiendo Conventional Commits

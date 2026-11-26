# Runner (Fabric 1.21.1)

Port a mod de Fabric del plugin Runner 1.2 (Manhunt: speedrunners vs. cazadores).

## Compilar (sin PC)
1. Sube esta carpeta a un repositorio de GitHub (desde el navegador del móvil sirve).
2. Pestaña **Actions** → workflow **build** → Run workflow.
3. Descarga el artefacto `runner-fabric-jar` → dentro está el `.jar`.
4. Ponlo en `mods/` junto con **Fabric API** (1.21.1) y Fabric Loader.

Con PC: `gradle build` (JDK 21) → `build/libs/`.

## Comandos (`/speedrunner` o `/sr`)
runner <jugador> · hunter <jugador> · start · stop · compass ·
setup (prep <seg> | goal <dragon|nether|end|advancement [id]> | hearts <runner|hunter> <corazones>)

## Diferencias respecto al plugin
- LuckPerms ya no hace falta: `runner/hunter/start/stop/setup` requieren ser OP (nivel 2); `/sr compass` lo puede usar cualquiera (solo funciona para cazadores).
- Config en `config/runner.json` y textos en `config/runner/lang.json` (ru/en, editable).
- `setup hearts` recibe corazones (se guardan como HP = corazones × 2).
- Al terminar la partida se conservan los roles, se quitan las brújulas y la vida máxima vuelve a 20.
- No se incluyó RunnerAPI (era solo para otros plugins de Bukkit).

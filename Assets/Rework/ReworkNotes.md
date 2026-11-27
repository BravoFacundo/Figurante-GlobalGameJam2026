# Figurante — Rework Notes

Juego de la Global Game Jam 2026 (en los commits: Facundo Bravo, Germán Di Francesco, Tomás Marmoni; créditos completos en la pantalla Credits).
Repo original: github.com/GermanDiFrancesco/GlobalGameJam2026 · Fork: github.com/BravoFacundo/Figurante-GlobalGameJam2026
Motor: Unity 6.3 LTS (proyecto creado en 6000.3.6f1). Escena única: `Assets/_Scenes/Main.unity`.

## Estado (nov 2026)
- Versión post-jam estable: main de German (incluye el trabajo local del 6/2/2026 que nunca se había commiteado).
- Build rápida para itch.io + portfolio (WebGL, Gzip + Decompression Fallback).
- Arreglos de build hechos en el fork:
  - MusicManager sin `DontDestroyOnLoad` (al reintentar se recarga la escena y la referencia quedaba rota).
  - Pausa con Esc **o** P, solo durante la partida (antes se podía abrir el menú en Win/Lose).
  - Volver de la pausa ya no reinicia el reloj (`ShowScreen("Game")` llamaba a `StartTimer()`).
  - Botón Salir oculto en WebGL (`exitButton` en UIManager).

## Para después

### Repo / proyecto
- [ ] Sacar del repo `.idea/`, `.vscode/`, `*.slnx` y sumarlos al `.gitignore`.
- [ ] Borrar `Sound/Music/Music_Win.ogg.sfk` (cache de Sound Forge) y sumar `*.sfk` al `.gitignore`.
- [ ] Escenas/assets sin uso: `Tests.unity`, `Settings/Scenes/URP2DSceneTemplate.unity`, `Lit2DSceneTemplate.scenetemplate` (3.9 MB), `Ticket_Highlighted 1.png` (duplicado), `LoseBehaviuor.cs` (vacío), `InputSystem_Actions.inputactions` (el input es por KeyCode).
- [ ] Packages que probablemente sobran: collab-proxy, multiplayer.center, visualscripting, sdk/toolchain linux, test-framework, timeline, spriteshape, aseprite/psdimporter (verificar antes).
- [ ] Root folder y jerarquía con el método de `retomar-proyecto-juego` (AssetUsageReport + HierarchyValidator).

### Código
- [ ] Logs y comentarios en español → inglés.
- [ ] UIManager: pantallas por string → enum; `startedGame`/`endedTutorial` públicos → estado de partida en GameController.
- [ ] GameController: `SetupTimer` se suscribe a `OnMidnightReached` cada vez; el reloj vive en UIManager (moverlo a un Timer propio).
- [ ] Reintentar sin recargar escena (reset de NPCs, pistas, carroza y jugador) si algún día deja de ser escena única.
- [ ] MusicManager: estados Menu/Tutorial/Game más claros (FirstEnterMenu vs EnterMenu).

### Experiencia de jugador
- [ ] Controles visibles fuera del tutorial (WASD moverse, Espacio mantener para interrogar/acusar, Esc/P pausa).
- [ ] Mute / slider de volumen.
- [ ] Revisar qué muestra la pantalla Score.
- [ ] Botón de pausa en pantalla (y evaluar controles táctiles para mobile).

### Build / peso
- [ ] Texturas grandes (cinemáticas y fondos de 1–2 MB): bajar Max Size / compresión para WebGL.
- [ ] Company Name (hoy `DefaultCompany`) y versión (`1.0`) para builds de escritorio.
- [ ] Descarga Windows en GitHub Releases + README con captura y link para jugar.

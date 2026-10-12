# wzMenus 1.0.0 — Wz Studios

Plugin para Paper 1.21.11 / Java 21. Fase 5: validación, paginación, refresco dinámico y empaquetado.

## Compilar
`mvn clean package` → `target/wzMenus-1.0.0.jar`

## Instalación
Coloca el JAR en `plugins/`, inicia Paper y revisa `plugins/wzMenus/`.

## Comandos
`/wzmenus open example`, `/wzmenus open paginated`, `/wzmenus edit example`, `/wzmenus create id`, `/wzmenus delete id confirm`, `/wzmenus reload`, `/wzmenus validate`.

## Paginación
`menu.pagination.enabled: true`, `previous-slot`, `next-slot` y `items.<id>.page` (comienza en 1). Los slots de navegación no deben estar ocupados por objetos.

## Refresco
`menu.refresh-ticks: 20` actualiza nombres, lores y condiciones visuales mientras el menú está abierto. Usar 0 para desactivar, o múltiplos de 5 >= 5.

## Integraciones
PlaceholderAPI, WorldGuard y HeadDatabase son opcionales; esta fase conserva la implementación anterior.

## Precauciones
Antes de publicar, probar en un servidor Paper real con y sin integraciones. La edición de acciones y condiciones desde la GUI sigue pendiente: usar YAML. No cargar configuraciones no confiables, especialmente acciones `[console]`.


## v1.0.2 - Cooldown por reclamación
Configuración `items.<id>.cooldown.seconds`, `cooldown.message`, almacenamiento en `cooldowns.yml`.
Ejemplo: `menus/example.yml` contiene una vela azul con recompensa de $5,000 cada 24 horas.

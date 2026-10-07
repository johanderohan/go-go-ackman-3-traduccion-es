# Go Go Ackman 3 — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/super-nintendo/go-go-ackman-3)**.

Traducción al **español de España** de *Go Go Ackman 3* para Super Nintendo / Super Famicom.

El repositorio contiene este README. El **parche IPS** está disponible en [Releases](https://github.com/johanderohan/go-go-ackman-3-traduccion-es/releases). Necesitas tu propia copia de la ROM japonesa, sin cabecera de copiador.

## Descarga

**[Descargar parche v1.0](https://github.com/johanderohan/go-go-ackman-3-traduccion-es/releases/download/v1.0/go_go_ackman_3_es_1.0.ips)** · [Todas las versiones](https://github.com/johanderohan/go-go-ackman-3-traduccion-es/releases)

## Estado de la traducción

**Versión 1.0**, publicada tras la revisión y aprobación de johanderohan. El contenido binario es idéntico al de la candidata 0.9 RC1 validada.

| Parte | Estado |
|---|---|
| Guion | 558 entradas de diálogo traducidas |
| Tienda | 15 descripciones, con precios y efectos conservados |
| Menús | JUGAR, OPCIONES, dificultad, controles y audio en castellano |
| Título animado | PULSA START |
| Fases | Rótulos y títulos de las cinco fases traducidos |
| Marcador | TIEMPO adaptado al espacio original |
| Derrota y continuación | FIN DE PARTIDA, ¿Continuar?, Sí y No |
| Epílogo | CONTINUARÁ y PRÓXIMAMENTE |
| Fuente | Tildes, ñ y signos de apertura |

Se conservan los logotipos, las firmas, los créditos y los textos integrados en decorados ajenos al guion o los menús. El recuento de entradas no representa un porcentaje de cobertura de todos los gráficos del juego.

### Comprobaciones realizadas

- Reconstrucción de la v1.0 y comparación byte a byte con la candidata aprobada.
- Aplicación del IPS sobre el original y verificación del tamaño, checksum y SHA-256 del resultado.
- Carga individual de las 558 entradas de diálogo y las 15 descripciones en Snes9x, con comparación de los glifos transferidos a memoria gráfica y capturas de composición.
- Arranque, introducción, menú y acceso al primer combate mediante el mando.
- Alternancia NORMAL/FÁCIL y ESTÉR./MONO mediante el mando.
- Carga de las cinco tarjetas de fase, revisión de capturas y conservación del recurso original de retratos animados.
- Pantalla de derrota y ambas respuestas de continuación; rótulo del epílogo.
- Arranque con bsnes2014 Balanced en macOS y Snes9x 1.63 para Linux x86-64 en un entorno de prueba.

Las pruebas de entradas aisladas comprueban su composición; no equivalen a una partida completa. Las tarjetas, la pantalla de derrota y el epílogo se revisaron mediante estados de prueba. johanderohan ha revisado la traducción y aprobado la v1.0; la cobertura detallada de sus pruebas no se ha especificado. No se afirma una validación exhaustiva de todas las rutas, animaciones o dispositivos.

## Criterios de traducción

Castellano de España a partir del japonés extraído de esta ROM, con biblia de términos y voces y guion bilingüe de revisión. Se mantiene la continuidad con las traducciones de [Go Go Ackman](https://github.com/johanderohan/go-go-ackman-traduccion-es) y [Go Go Ackman 2](https://github.com/johanderohan/go-go-ackman-2-traduccion-es).

Ackman emplea un registro directo y burlón. Gordon lo trata de usted y lo llama «señor Ackman». Se mantienen **Ackman**, **Gordon**, **Angelito**, **Bócal**, **Raguel**, **Jibril**, **Elegia**, **Marjo** y **Ermitaño**. En esta entrega, **Joséphine Yamamoto** conserva el apellido que aparece en su propio guion japonés. Son decisiones de esta localización, no denominaciones oficiales en castellano.

Se distingue salud, salud máxima y vida extra, así como nivel del arma y nivel mínimo. Los precios y la unidad «P» se conservan. El selector de sonido utiliza **ESTÉR.** por su límite de seis celdas; **START** conserva el nombre del botón del mando.

Traducción elaborada con asistencia de Codex y revisión del material extraído. No se ha realizado una segunda revisión lingüística humana independiente.

## Cómo aplicar el parche

1. Descarga el `.ips` de [Releases](https://github.com/johanderohan/go-go-ackman-3-traduccion-es/releases).
2. Utiliza una copia limpia de **Go Go Ackman 3 (Japan).sfc**, de **2 097 152 bytes**, sin cabecera adicional de 512 bytes. Su CRC32 es **9A18290C**.
3. Comprueba el SHA-256 de tu archivo contra la tabla inferior.
4. Aplica el IPS con una herramienta compatible con la ampliación de ROMs y guarda el resultado en un archivo nuevo. Se aplica directamente al original japonés, sin parches previos.
5. Comprueba el SHA-256 de la ROM resultante, de **4 194 304 bytes**, y ábrela en tu emulador o dispositivo compatible.

| Archivo | SHA-256 |
|---|---|
| ROM japonesa original | `e6aa42ae74f200d4f57d5e7c11e6c9e4b08eaa06e812ef33c2c86cf71715f1c7` |
| Parche v1.0 | `53e99d2a8fb65d7e9fbb98e561f6e9e116b8e8b12436b7a69cde42f9368c8b9c` |
| ROM traducida v1.0 | `ce0bdce3dcc314d3ef98c3f7b0a3460bbbddb1c427b99f66390131c7900c5466` |

Para calcular SHA-256:

```bash
sha256sum "juego.sfc"                  # Linux
shasum -a 256 "juego.sfc"              # macOS
CertUtil -hashfile "juego.sfc" SHA256  # Windows
```

Empieza desde el arranque del juego: los estados instantáneos de otras versiones pueden conservar gráficos o código anteriores en memoria. Si ya utilizas la candidata 0.9 RC1 y su huella coincide con la indicada, tienes el mismo contenido binario que la v1.0 y no necesitas volver a parchear.

## Informar de errores

Abre una [incidencia](https://github.com/johanderohan/go-go-ackman-3-traduccion-es/issues) e indica la versión del parche, emulador y núcleo, fase y acción que provoca el fallo. Una captura ayuda a localizarlo. No adjuntes la ROM.

## Créditos

Se conservan los créditos y avisos del juego original, incluidos **Banpresto** y **Bird Studio / Shueisha**.

Traducción castellana preparada para **johanderohan** con asistencia de Codex. Revisión y aprobación de la versión 1.0: **johanderohan**.

Proyecto de aficionados, sin carácter oficial ni relación con los titulares del juego. Este repositorio es independiente de los de las dos primeras entregas. Se publican el README y el IPS en Releases; no se distribuyen ROMs, partidas ni el corpus extraído.

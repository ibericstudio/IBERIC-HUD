IBC HUD - ESX / QBCORE
=====================

INSTALACION
1. Sustituye la carpeta anterior por esta carpeta SK-Hud.
2. Asegurate de iniciar ox_lib y el framework antes del HUD.
3. En server.cfg: ensure IBC-Hud

CAMBIAR DE FRAMEWORK
Abre config.lua y modifica SOLO esta linea:

Config.Framework = 'qbcore'

Para ESX usa:
Config.Framework = 'esx'

Valores permitidos: 'qbcore' o 'esx'. No es necesario editar client.lua ni server.lua.

ESX - NECESIDADES
El HUD lee hambre y sed desde esx_status. Asegurate de tener esx_status iniciado.
Puedes cambiar los nombres de estados en Config.ESX.
El estres ESX usa un contador propio del HUD por defecto, porque ESX no incluye un
status de estres estandar. Si tu servidor tiene un status 'stress' en esx_status,
puedes activar Config.ESX.UseStressStatus = true.

COLORES
Los colores por defecto se han adaptado a la ilustracion incluida en build/cityBackground.png:
lavanda, rosa suave y melocoton. Edita Config.Theme en config.lua:
- primary: color principal
- secondary: color secundario
- accent: acento
- background: fondo
- text: texto
- muted: texto secundario

FUNCIONES
- Conserva la interfaz NUI original y su distribucion.
- Mantiene el velocimetro, minimapa, estres, voz, radio, telefono y cinturon.
- Conserva el export ToggleHud(bool).
- Se han añadido comprobaciones para fuel, estados y datos del jugador.

DEPENDENCIAS
- ox_lib (cache, notificaciones y carga de textura)
- QBCore o ESX, segun Config.Framework
- esx_status para hambre/sed en ESX
- Recurso de combustible configurado en Config.fuel (por defecto LegacyFuel)
- pma-voice para eventos de voz, si se utiliza

NOTA
No se incluyo un archivo de logo independiente en el RAR original. La paleta de color
se ha tomado de la imagen cityBackground.png que ya venia dentro del recurso.

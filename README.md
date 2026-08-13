# FluyLab - Descargas

Programas de FluyLab listos para instalar. **Aqui solo hay binarios: no hay codigo fuente.**

## Cafe OS - Programa de impresion

Conecta [Cafe OS](https://cafe.fluylab.com) con las impresoras termicas del cafe.

Existe porque **ningun navegador puede hablarle directo a una impresora termica**:
una pagina web no puede abrir un socket al puerto 9100. Por eso este programa
corre dentro del cafe, recibe las ordenes y las manda a la impresora.

### Instalar

1. Descarga los **tres archivos** de la ultima publicacion a la misma carpeta
2. Clic derecho en `instalar.ps1` -> **Ejecutar con PowerShell**
3. Pega la clave que sale en Cafe OS -> Ajustes -> Impresoras

Queda corriendo solo, sin ventana, y arranca al prender el computador.
Para quitarlo: `desinstalar.ps1`.

La primera vez Windows dira *"editor desconocido"*: **Mas informacion ->
Ejecutar de todas formas**.

### Requisitos

- Windows
- Impresora termica de 58 u 80 mm que hable **ESC/POS por el puerto 9100**
  (la gran mayoria: Epson, 3nStar, Xprinter y genericas)
- La impresora conectada al **mismo router** que el computador, por cable de red

### Seguridad

El programa **no hace nada sin una cuenta de Cafe OS**. Sin la clave solo
muestra una pantalla pidiendola. La clave se puede anular en cualquier momento
desde Ajustes -> Impresoras -> Quitar acceso.

No contiene claves, ni acceso a bases de datos, ni codigo de Cafe OS.

### Si algo no imprime

El registro esta en `%APPDATA%\CafeOS-Impresionegistro.txt` y dice
exactamente que paso.

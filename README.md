# 🐍 SnakeASM

Juego clásico de la serpiente desarrollado en **lenguaje ensamblador** para entorno DOS.  
El objetivo es controlar la serpiente, comer frutas para sumar puntos y evitar chocar con los bordes o con su propio cuerpo.

---

## 📌 Descripción

Este proyecto fue programado en ensamblador y pone en práctica conceptos de bajo nivel como:

- manejo de interrupciones
- lectura de teclado
- control del cursor en pantalla
- impresión de caracteres
- validación de colisiones
- lógica de juego

Es una implementación retro del famoso juego de la viborita, ejecutado en modo texto.

---

## 🛠 Requisitos

Para ejecutar este juego en tu computadora necesitas:

- **MASM** o **TASM**
- **LINK** o **TLINK**
- Un entorno compatible con programas DOS, como:
  - **DOSBox**
  - **emu8086**

---

## 📂 Archivo principal

El archivo principal del proyecto es:

```asm
JuegoSerpienteMod.asm
```
## ▶️ Cómo ejecutarlo

### Opción 1: Con **DOSBox + MASM/TASM**

1. Guarda el archivo `JuegoSerpienteMod.asm` en una carpeta, por ejemplo: `C:\GameASM`

2. Abre **DOSBox** y monta la carpeta:
`mount c c:\GameASM`
`c:`

3. Ensambla y ejecuta el programa.

**Con MASM**
`masm JuegoSerpienteMod.asm;`
`link JuegoSerpienteMod.obj;`
`JuegoSerpienteMod.exe`

**Con TASM**
`tasm JuegoSerpienteMod.asm`
`tlink JuegoSerpienteMod.obj`
`JuegoSerpienteMod.exe`

### Opción 2: Con **emu8086**

1. Abre **emu8086**.  
2. Carga el archivo `JuegoSerpienteMod.asm`.  
3. Presiona **Compile**.  
4. Después selecciona **Run** o **Emulate**.

## 🎮 Controles

Usa estas teclas para mover la serpiente: **W** → Arriba, **S** → Abajo, **A** → Izquierda, **D** → Derecha, **X** → Salir.

> ⚠️ **Importante:** desactiva las mayúsculas para que los controles funcionen correctamente.

## 📜 Reglas del juego

La serpiente se mueve dentro de un área delimitada. Cada fruta consumida suma puntos. El juego termina si chocas con un borde, chocas con tu propio cuerpo o presionas la tecla `X`. Si alcanzas la puntuación máxima, ganas la partida.

## ✨ Características

Interfaz en modo texto, generación aleatoria de frutas, sistema de puntaje, detección de colisiones, restricción para evitar regresar en dirección contraria y mensajes de bienvenida, derrota y victoria.

## 🧠 Estructura del programa

Algunos procedimientos principales del código son: `mostrar_bienvenida` → muestra el mensaje inicial, `asignar_dimensiones` → configura el área de juego, `instrucciones` → muestra los controles, `generar_fruta` → coloca una fruta en una posición válida, `leer_teclado` → detecta la tecla presionada, `moverSerpiente` → actualiza el movimiento, `verificar_fruta` → detecta si se comió una fruta, `verificar_lim` → valida colisiones con bordes, `verificar_cuerpo` → valida colisiones con el cuerpo, `imprimir_score` → muestra los puntos.

## 💻 Tecnologías usadas

**Assembly x86**, **Interrupciones DOS** (`int 21h`) e **Interrupciones BIOS** (`int 10h`).

## 🚀 Objetivo del proyecto

Este juego fue desarrollado como práctica para reforzar conocimientos de programación en ensamblador, aplicando lógica de videojuegos y control directo del hardware a bajo nivel.

## 📷 Vista general

Juego retro en consola con estilo clásico, donde cada movimiento cuenta y la precisión es clave para alcanzar la máxima puntuación.

# 🛰️ Albatastic Scout
### PCB compacta para nodos solares sencillos y clientes de despliegue rápido

**Albatastic Scout** es una placa *barebones* de la familia Albatastic diseñada específicamente para actuar como nodo cliente autónomo o baliza temporal (ideal para acampadas y exteriores). Su diseño estilizado optimiza el espacio para albergar una gran capacidad de energía y compatibilidad de radio sin añadir florituras.

---

## 🛠️ Características Principales

### 📻 Conectividad y Control
*   **Compatibilidad Multi-Radio:** Soporta módulos **E22/E22P**, **E80**, **E28** y **HT-RA62**.
*   **Cerebro:** NRF52840 Pro Micro de bajo consumo.
*   **Sensor Integrado:** Espacio dedicado para un sensor ambiental **BME280** (presión, temperatura y humedad).

### 🔋 Alimentación y Gestión Solar
*   **Gran Autonomía:** Diseñada para alojar **2 baterías 18650** con su respectivo circuito BMS de protección.
*   **Flexibilidad MPPT:** Compatible con módulos MPPT como el CN3795 / CN3791 / SD30CRMA.
*   **Regulación de Voltaje:** Posibilidad de montar 2 boosters para el E22/E22P.
*   **Control Físico:** Incluye un interruptor de encendido/apagado general en placa.

---

## 📦 Lista de Materiales (BOM)

### 🔹 1. Componentes Base (Comunes para todos los montajes)
Estos componentes son necesarios independientemente de la configuración elegida:

| Componente | Descripción / Modelo | Cantidad | Enlace de Compra | Notas |
| :--- | :--- | :---: | :---: | :--- |
| **MCU / Cerebro** | NRF52840 Pro Micro | 1 | [🛒 Comprar](https://es.aliexpress.com/item/1005007383375306.html) | Microcontrolador principal de bajo consumo |
| **Sensor Ambiental (opcional)** | Módulo BME280 | 1 | [🛒 Comprar](https://es.aliexpress.com/item/1005002963592665.html) | Medición de temperatura, humedad y presión |
| **Soporte Baterías** | Portabaterías para 1x 18650 | 2 | [🛒 Comprar](https://es.aliexpress.com/item/4000692031094.html) | Alojamiento para celdas Li-ion 18650 |
| **Protección Batería** | Circuito BMS 1S | 1 | [🛒 Comprar](https://es.aliexpress.com/item/1005008217119006.html) | Módulo de protección contra sobrecarga/sobredescarga |
| **Interruptor** | Interruptor Encendido/Apagado | 1 | [🛒 Comprar](https://es.aliexpress.com/item/1005006143122311.html) | Interruptor general de encendido |
| **Resistencias 1206** | 1x 680K 1x 1M (o 2x 1M) | 2 | [🛒 Comprar](https://es.aliexpress.com/item/1005002991902748.html) | Resistencias para monitorear el nivel de la batería |


---

### 🔹 2. Guía de Selección de Componentes Configurables

Sigue estos pasos para seleccionar los componentes según la configuración de tu nodo:

#### 1️⃣ **Paso 1: Elige el Módulo de Radio** *(Selecciona 1)*

| Opción | Módulo | Descripción / Características | Enlace de Compra |
| :--- | :--- | :--- | :---: |
| **Opción A** | **E22P** | Semtech SX1262 / SX1268. Recomendado para enlaces de muy largo alcance y máxima potencia LoRa. | [🛒 Comprar](https://es.aliexpress.com/item/1005010297548005.html) |
| **Opción B** | **E22** | Semtech SX1262 / SX1268. Recomendado para enlaces de muy largo alcance y máxima potencia LoRa. Sin filtros integrados | [🛒 Comprar](https://es.aliexpress.com/item/1005009741346732.html) |
| **Opción C** | **E80** | Módulo LoRa de bajo consumo de 433/868 y 2.4GHz | [🛒 Comprar](https://es.aliexpress.com/item/1005009119868850.html) |
| **Opción D** | **E28** | Módulo LoRa de 2.4GHz Ideal para alta velocidad de transmisión o redes locales. | [🛒 Comprar](https://es.aliexpress.com/item/1005010288386483.html) |
| **Opción E** | **HT-RA62** | Módulo compacto basado en SX1262. | [🛒 Comprar](https://es.aliexpress.com/item/1005008363549136.html) |

#### 2️⃣ **Paso 2: Elige el Cargador Solar (MPPT)** *(Selecciona 1)*

| Opción | Módulo MPPT | Descripción / Aplicación | Enlace de Compra |
| :--- | :--- | :--- | :---: |
| **Opción A** | **CN3791** | MPPT sencillo y fiable para paneles de 6, 9 y 12V. Revisar siempre la versión que os llega, a veces la mandan aleatoriamente | [🛒 Comprar](https://es.aliexpress.com/item/1005008286456080.html) |
| **Opción B** | **CN3795** | Controlador MPPT con voltaje de panel flexible (9-18+V) y voltaje de salida ajustable. | [🛒 Comprar](https://es.aliexpress.com/item/1005009189097890.html) |
| **Opción C** | **SD30CRMA** | Controlador sencillo para 9, 12 y 18V con salida ajustable | [🛒 Comprar](https://es.aliexpress.com/item/1005007473789907.html) |

#### 3️⃣ **Paso 3: Elige la Regulación / Boost para la Radio** *(Solo para E22/E22P y E28)*

| Opción | Modo de Alimentación | Descripción / Recomendación | Enlace de Compra |
| :--- | :--- | :--- | :---: |
| **Opción A (E28) ** | **Modo QRP** *(Sin regulador dedicado)* | La radio se alimenta directamente de los 3.3V del Pro Micro. Para transmisiones QRP con E28. | N/A |
| **Opción B** | **Mini Buck-Boost 3.3V / 5V** | Opción mini para alimentar el E22/E28 a 5/3.3V respectivamente | [🛒 Comprar](https://es.aliexpress.com/item/1005011637436564.html) |
| **Opción C (E22/E22P)** | **Boost 5V 3A** | Opción para alimentar el E22/E22P a 5V | [🛒 Comprar](https://es.aliexpress.com/item/1005007013856492.html) |
| **Opción D (E22/E22P)** | **HW-085** | Opción mini para alimentar el E22 a 5V respectivamente | [🛒 Comprar](https://es.aliexpress.com/item/1005008051438437.html) |

---


**Enlaces no afiliados**
<details>
<summary><b>📋 Historial de Cambios (Changelog)</b></summary>

<br>

### 🚧 v1.1 - Por testear
* **Corregido:** Corregido que la salida del CN3791 no estaba conectada.
* **Corregido:** El E28 no estaba conectado a 3.3V
* **Añadido:** Añadido opción de buck-boost de 3.3V/5V para el E22P/E28.
* **Añadido:** Selector de alimentación para el E28 (Pro micro para QRP, Buck-Boost para potencia máxima).

### 🟢 v1.0 (Inicial) - Testeando
* **Diseño:** Versión inicial del PCB *barebones* para nodos clientes.
* **Energía:** Integración de soporte para doble batería 18650 y BMS.
* **Radio:** Soporte multi-módulo (E22/E22P, E80, E28, HT-RA62).
* **Sensórica:** Huella añadida para sensor BME280.
* **Power:** Enrutado para boosters dedicados al E22/E22P y pads para módulos MPPT.

</details>

---

## 📐 Vista del Diseño

A continuación se muestra el render de la PCB, donde se puede apreciar la distribución alargada equivalente a 3 placas *Compact* de ancho, optimizando el espacio para el módulo solar y el portabaterías trasero:

<p align="center">
  <img width="500" alt="Albatastic Scout PCB Render" src="https://github.com/user-attachments/assets/ff0325e0-aca7-458b-9571-c9f083cb64d4" />
</p>

---

> 💡 **Nota de uso:** Esta placa está pensada para nodos finales (Clients) sencillos y/o temporales. No se recomienda su uso como Router de infraestructura pesada debido a su enfoque simplificado y la ausencia de hardware resiliente.

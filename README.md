# 🛰️ Albatastic Scout

> ⚠️ **Aviso de responsabilidad / Legal Disclaimer:**  
> **🇪🇸:** Queda bajo la responsabilidad exclusiva del usuario final garantizar que la fabricación, configuración y uso de estas placas o dispositivos cumpla con la legislación y normativa de telecomunicaciones aplicable en su país o región.  
> **🇬🇧:** It is the sole responsibility of the end user to ensure that the assembly, configuration, and operation of these PCBs comply with applicable local telecommunications laws and regulations.

---

## 🇪🇸 Castellano

### PCB compacta para nodos solares sencillos y clientes de despliegue rápido

**Albatastic Scout** es una placa *barebones* de la familia Albatastic diseñada específicamente para actuar como nodo cliente solar sencillo, ideal para clientes sencillos y/o nodos temporales (acampadas, camping, cruceros, etc). Su diseño estilizado optimiza el espacio para albergar una gran capacidad de energía y compatibilidad de radio sin añadir florituras.

---

### 🛠️ Características Principales

#### 📻 Conectividad y Control
* **Compatibilidad Multi-Radio:** Soporta módulos **E22/E22P**, **E80**, **E28** y **HT-RA62**.
* **Cerebro:** NRF52840 Pro Micro de bajo consumo.
* **Sensor Integrado:** Espacio dedicado para un sensor ambiental **BME280** (presión, temperatura y humedad).

#### 🔋 Alimentación y Gestión Solar
* **Gran Autonomía:** Diseñada para alojar **2 baterías 18650** con su respectivo circuito BMS de protección.
* **Flexibilidad MPPT:** Compatible con módulos MPPT como el CN3795 / CN3791 / SD30CRMA.
* **Regulación de Voltaje:** Posibilidad de montar 2 boosters para el E22/E22P.
* **Control Físico:** Incluye un interruptor de encendido/apagado general en placa.

---

### 📦 Lista de Materiales (BOM)

#### 🔹 1. Componentes Base (Comunes para todos los montajes)
Estos componentes son necesarios independientemente de la configuración elegida:

| Componente | Descripción / Modelo | Cantidad | Enlace de Compra | Notas |
| :--- | :--- | :---: | :---: | :--- |
| **MCU / Cerebro** | NRF52840 Pro Micro | 1 | [🛒 Comprar](https://es.aliexpress.com/item/1005007383375306.html) | Microcontrolador principal de bajo consumo |
| **Sensor Ambiental (opcional)** | Módulo BME280 | 1 | [🛒 Comprar](https://es.aliexpress.com/item/1005002963592665.html) | Medición de temperatura, humedad y presión |
| **Soporte Baterías** | Portabaterías para 1x 18650 | 2 | [🛒 Comprar](https://es.aliexpress.com/item/4000692031094.html) | Alojamiento para celdas Li-ion 18650 |
| **Protección Batería** | Circuito BMS 1S | 1 | [🛒 Comprar](https://es.aliexpress.com/item/1005008217119006.html) | Módulo de protección contra sobrecarga/sobredescarga |
| **Interruptor** | Interruptor Encendido/Apagado | 1 | [🛒 Comprar](https://es.aliexpress.com/item/1005006143122311.html) | Interruptor general de encendido |
| **Resistencias 1206** | 1x 680K 1x 1M (o 2x 1M) | 2 | [🛒 Comprar](https://es.aliexpress.com/item/1005002991902748.html) | Resistencias para monitorear el nivel de la batería |
| **Botón reset** | Botón de reset | 1 | [🛒 Comprar](https://es.aliexpress.com/item/4001125532910.html) | Pulsador SMD/PTH para reset |
| **Baterías 18650** | Baterías 18650 | 2 | [🛒 Comprar](https://www.nkon.nl/es/) | Recomiendo usar baterías nuevas y de calidad |

---

#### 🔹 2. Guía de Selección de Componentes Configurables

Sigue estos pasos para seleccionar los componentes según la configuración de tu nodo:

##### 1️⃣ Paso 1: Elige el Módulo de Radio *(Selecciona 1)*

| Opción | Módulo | Descripción / Características | Enlace de Compra |
| :--- | :--- | :--- | :---: |
| **Opción A** | **E22P** | Semtech SX1262 / SX1268. Recomendado para enlaces de muy largo alcance y máxima potencia LoRa. Disponible en 433, 868 y 915 | [🛒 Comprar](https://es.aliexpress.com/item/1005010297548005.html) |
| **Opción B** | **E22** | Semtech SX1262 / SX1268. Sin filtros integrados, disponible en más bandas | [🛒 Comprar](https://es.aliexpress.com/item/1005009741346732.html) |
| **Opción C** | **E80** | Módulo LoRa de bajo consumo de 433/868 y 2.4GHz | [🛒 Comprar](https://es.aliexpress.com/item/1005009119868850.html) |
| **Opción D** | **E28** | Módulo LoRa de 2.4GHz. Ideal para alta velocidad de transmisión o redes locales. | [🛒 Comprar](https://es.aliexpress.com/item/1005010288386483.html) |
| **Opción E** | **HT-RA62** | Módulo compacto basado en SX1262. | [🛒 Comprar](https://es.aliexpress.com/item/1005008363549136.html) |

##### 2️⃣ Paso 2: Elige el Cargador Solar (MPPT) *(Selecciona 1)*

| Opción | Módulo MPPT | Descripción / Aplicación | Enlace de Compra |
| :--- | :--- | :--- | :---: |
| **Opción A** | **CN3791** | MPPT sencillo y fiable para paneles de 6, 9 y 12V. Revisar siempre la versión que os llega, a veces la mandan aleatoriamente | [🛒 Comprar](https://es.aliexpress.com/item/1005008286456080.html) |
| **Opción B** | **CN3795** | Controlador MPPT con voltaje de panel flexible (9-18+V) y voltaje de salida ajustable. | [🛒 Comprar](https://es.aliexpress.com/item/1005009189097890.html) |
| **Opción C** | **SD30CRMA** | Controlador sencillo para 9, 12 y 18V con salida ajustable | [🛒 Comprar](https://es.aliexpress.com/item/1005007473789907.html) |

##### 3️⃣ Paso 3: Elige la Regulación / Boost para la Radio *(Solo para E22/E22P y E28)*

| Opción | Modo de Alimentación | Descripción / Recomendación | Enlace de Compra |
| :--- | :--- | :--- | :---: |
| **Opción A (E28)** | **Modo QRP** *(Sin regulador dedicado)* | La radio se alimenta directamente de los 3.3V del Pro Micro. Para transmisiones QRP con E28. | N/A |
| **Opción B** | **Mini Buck-Boost 3.3V / 5V** | Opción mini para alimentar el E22/E28 a 5/3.3V respectivamente | [🛒 Comprar](https://es.aliexpress.com/item/1005011637436564.html) |
| **Opción C (E22/E22P)** | **Boost 5V 3A** | Opción para alimentar el E22/E22P a 5V | [🛒 Comprar](https://es.aliexpress.com/item/1005007013856492.html) |
| **Opción D (E22/E22P)** | **HW-085** | Opción mini para alimentar el E22/E22P a 5V | [🛒 Comprar](https://es.aliexpress.com/item/1005008051438437.html) |
| **Opción E (V1.2+)** | **TPS63020** | Opción mini para alimentar el E22/E28 a 5/3.3V respectivamente | [🛒 Comprar](https://es.aliexpress.com/item/1005008099216597.html) |

*(Enlaces no afiliados)*

---

### 🔩 Instrucciones de Montaje

> ⚠️ **Advertencia importante de seguridad:** Antes de colocar las baterías o conectar un panel solar, verifica con un multímetro en modo continuidad que no existen cortocircuitos entre VCC, 3.3V, 5V y GND.

Se recomienda realizar el ensamblaje siguiendo el método de empezar por dentro e ir hacia fuera:

#### 1️⃣ Paso 1: Componentes Pasivos SMD e interruptor
1. **Resistencias SMD (1206):** Soldar las 2 resistencias del divisor de tensión (680K y 1M, o 2x 1M según tu configuración) destinadas al monitoreo del voltaje de batería.
2. **Control:** Soldar el **botón de reset** y el **interruptor On/Off** principal en la placa. Para soldar el interruptor, recomiendo cortarle las patas algo, darle la vuelta a la PCB, introducir el interruptor hasta que las patas se queden a ras de la cara donde van las baterías y añadir estaño. Hay que asegurarse de que se quede plano.

#### 2️⃣ Paso 2: Micro Controlador (Similar a la Albatastic compact)
1. **Paso previo:** Insertar la tira de pines por la cara larga a la PCB (asegúrate de hacerlo apoyado sobre una mesa para que estos no se introduzcan para abajo). Apoyar el Pro Micro sobre los pines.
2. **Añadir estaño:** Añade estaño a uno de los pines de la tira a cada lado y retira el Pro Micro. Acto seguido, suelda todos los pines.
3. **Elimina el plástico de los pines:** Elimina el separador de los pines con cuidado valiéndote de unas pinzas o alicates (¡ojo sin rayar la PCB!).
4. **Suelda el Pro Micro:** Empuja el Pro Micro hasta el fondo y suéldalo. Corta el sobrante.

##### Si quieres poder quitar el ProMicro sin desoldar:
4. **Importante:** Coloca unos pines hembra sobre los pines macho ya soldados a la placa y empújalos hasta el fondo.
5. **Suelda el Pro Micro:** Suelda el Pro Micro como en el paso normal.

#### 3️⃣ Paso 3: Sensor BME280 (Opcional)
1. Soldar el sensor **BME280** en sus pines dedicados para mediciones de temperatura, humedad y presión.

#### 4️⃣ Paso 4: Regulador / Boost de Radio (según selección de alimentación)
* **E80 y RA62:** No es necesario nada, avanza al siguiente paso.
* **Modo QRP (E28):** Si no usas módulo boost externo, suelda el selector para alimentar la radio directamente con los 3.3V del Pro Micro.
* **Con boost (E22/E22P):** Suelda el boost a la placa directamente.
* **Con buck-boost (E28/E22/E22P):** Suelda el buck-boost a la placa y comprueba el voltaje que da. Para el E28, suelda el selector de alimentación en posición buck-boost. Para el E22/E22P, suelda el jumper para 5V.

#### 5️⃣ Paso 5: Módulo de Radio
1. **Módulo de Radio:** Suelda la radio seleccionada (**E22P**, **E22**, **E80**, **E28** o **HT-RA62**). Suelda el selector E22/E22P según corresponda (o déjalo sin soldar si no es ninguno de estos dos).
   * *⚠️ Nunca enciendas ni transmitas con la radio sin la antena conectada.*

#### 6️⃣ Paso 6: Controlador de carga MPPT
1. Suelda el controlador de carga MPPT en la posición correcta.  
   * *⚠️ OJO con la polaridad de los CN3791.*

#### 7️⃣ Paso 7: BMS y baterías
1. **BMS:** Suelda el BMS respetando la polaridad. Para ello es recomendable soldar este en un ángulo o con cierta separación. Un truco consiste en poner estaño en dos pads del BMS (hasta que sobresalga 2-3mm), y luego, darle la vuelta y mientras lo sujetas con unas pinzas, aplicar calor al estaño para que se funda y se una.
2. **Baterías:** Suelda el portabaterías. Inserta las baterías respetando la polaridad.
3. **Encendido inicial:** Conecta la antena. En el primer encendido, es necesario encenderlo con el MPPT o el USB-C del Pro Micro para activar el BMS.

---

> 💡 **Nota de uso:** Esta placa está pensada para nodos finales (Clients) sencillos y/o temporales. No se recomienda su uso como Router de infraestructura pesada debido a su enfoque simplificado y la ausencia de hardware resiliente. Si necesitas hardware resiliente y/o reset, te recomiendo la [Albatastic Pro](https://github.com/EmilioAL-Git/PCB-Albatastic-PRO/tree/main).

---

## 🇬🇧 English

### Compact PCB for simple solar nodes and quick-deployment clients

**Albatastic Scout** is a barebones board from the Albatastic family, specifically designed to act as a simple solar client node—ideal for lightweight client setups and/or temporary nodes (camping, outdoor activities, cruises, etc.). Its streamlined layout optimizes space to accommodate high battery capacity and multi-radio compatibility without extra frills.

---

### 🛠️ Key Features

#### 📻 Connectivity & Control
* **Multi-Radio Compatibility:** Supports **E22/E22P**, **E80**, **E28**, and **HT-RA62** modules.
* **Brain / MCU:** Low-power NRF52840 Pro Micro.
* **Integrated Sensor:** Dedicated footprint for a **BME280** environmental sensor (pressure, temperature, and humidity).

#### 🔋 Power & Solar Management
* **High Autonomy:** Designed to hold **two 18650 batteries** with a matching 1S BMS protection circuit.
* **MPPT Flexibility:** Compatible with solar MPPT charger modules like CN3795 / CN3791 / SD30CRMA.
* **Voltage Regulation:** Capability to mount up to 2 boost converters for E22/E22P modules.
* **Physical Control:** Onboard master ON/OFF switch included.

---

### 📦 Bill of Materials (BOM)

#### 🔹 1. Base Components (Common for all builds)
These components are required regardless of your chosen configuration:

| Component | Description / Model | Qty | Purchase Link | Notes |
| :--- | :--- | :---: | :---: | :--- |
| **MCU / Brain** | NRF52840 Pro Micro | 1 | [🛒 Buy](https://es.aliexpress.com/item/1005007383375306.html) | Low-power main microcontroller |
| **Environmental Sensor (optional)** | BME280 Module | 1 | [🛒 Buy](https://es.aliexpress.com/item/1005002963592665.html) | Temperature, humidity, and pressure sensing |
| **Battery Holder** | 1x 18650 Battery Holder | 2 | [🛒 Buy](https://es.aliexpress.com/item/4000692031094.html) | Enclosure for 18650 Li-ion cells |
| **Battery Protection** | 1S BMS Circuit | 1 | [🛒 Buy](https://es.aliexpress.com/item/1005008217119006.html) | Overcharge/overdischarge protection module |
| **Switch** | Power ON/OFF Switch | 1 | [🛒 Buy](https://es.aliexpress.com/item/1005006143122311.html) | Main power toggle switch |
| **1206 Resistors** | 1x 680K 1x 1M (or 2x 1M) | 2 | [🛒 Buy](https://es.aliexpress.com/item/1005002991902748.html) | Resistors for battery voltage monitoring |
| **Reset Button** | Reset Push Button | 1 | [🛒 Buy](https://es.aliexpress.com/item/4001125532910.html) | SMD/PTH reset push button |
| **18650 Batteries** | 18650 Cells | 2 | [🛒 Buy](https://www.nkon.nl/es/) | Recommended to use new, high-quality cells |

---

#### 🔹 2. Configurable Component Selection Guide

Follow these steps to choose components based on your intended node setup:

##### 1️⃣ Step 1: Select the Radio Module *(Select 1)*

| Option | Module | Description / Features | Purchase Link |
| :--- | :--- | :--- | :---: |
| **Option A** | **E22P** | Semtech SX1262 / SX1268. Recommended for ultra-long-range links & maximum LoRa power. Available in 433, 868, and 915 MHz | [🛒 Buy](https://es.aliexpress.com/item/1005010297548005.html) |
| **Option B** | **E22** | Semtech SX1262 / SX1268. Unfiltered variant, available in additional frequency bands | [🛒 Buy](https://es.aliexpress.com/item/1005009741346732.html) |
| **Option C** | **E80** | Ultra-low power LoRa module for 433/868 MHz and 2.4GHz | [🛒 Buy](https://es.aliexpress.com/item/1005009119868850.html) |
| **Option D** | **E28** | 2.4GHz LoRa module. Ideal for high data throughput or local mesh networks. | [🛒 Buy](https://es.aliexpress.com/item/1005010288386483.html) |
| **Option E** | **HT-RA62** | Compact module based on SX1262. | [🛒 Buy](https://es.aliexpress.com/item/1005008363549136.html) |

##### 2️⃣ Step 2: Select Solar Charger (MPPT) *(Select 1)*

| Option | MPPT Module | Description / Application | Purchase Link |
| :--- | :--- | :--- | :---: |
| **Option A** | **CN3791** | Simple, reliable MPPT for 6V, 9V, and 12V panels. Always verify the board received, as suppliers sometimes send random versions | [🛒 Buy](https://es.aliexpress.com/item/1005008286456080.html) |
| **Option B** | **CN3795** | MPPT controller with flexible panel input voltage (9-18+V) and adjustable output voltage. | [🛒 Buy](https://es.aliexpress.com/item/1005009189097890.html) |
| **Option C** | **SD30CRMA** | Simple controller for 9V, 12V, and 18V panels with adjustable output | [🛒 Buy](https://es.aliexpress.com/item/1005007473789907.html) |

##### 3️⃣ Step 3: Select Radio Regulation / Boost *(Only for E22/E22P and E28)*

| Option | Power Mode | Description / Recommendation | Purchase Link |
| :--- | :--- | :--- | :---: |
| **Option A (E28)** | **QRP Mode** *(No dedicated regulator)* | The radio is powered directly from the Pro Micro 3.3V rail. For QRP transmission with E28. | N/A |
| **Option B** | **Mini Buck-Boost 3.3V / 5V** | Compact option to power E22/E28 at 5V/3.3V respectively | [🛒 Buy](https://es.aliexpress.com/item/1005011637436564.html) |
| **Option C (E22/E22P)** | **Boost 5V 3A** | Power module to supply 5V to E22/E22P | [🛒 Buy](https://es.aliexpress.com/item/1005007013856492.html) |
| **Option D (E22/E22P)** | **HW-085** | Mini boost option to power E22/E22P at 5V | [🛒 Buy](https://es.aliexpress.com/item/1005008051438437.html) |
| **Option E (V1.2+)** | **TPS63020** | Mini option to power E22/E28 at 5V/3.3V respectively | [🛒 Buy](https://es.aliexpress.com/item/1005008099216597.html) |

*(Non-affiliated links)*

---

### 🔩 Assembly Instructions

> ⚠️ **Important Safety Warning:** Before inserting batteries or connecting a solar panel, use a multimeter in continuity mode to verify that there are no short circuits between VCC, 3.3V, 5V, and GND.

Assembly should proceed using the "inside-out" method:

#### 1️⃣ Step 1: SMD Passive Components & Power Switch
1. **SMD Resistors (1206):** Solder the 2 voltage divider resistors (680K and 1M, or 2x 1M depending on configuration) used for battery monitoring.
2. **Control:** Solder the **reset button** and the main **ON/OFF switch**. For the switch, trim the leads slightly, flip the PCB, insert until leads are flush with the battery side, and solder. Ensure it sits completely flat.

#### 2️⃣ Step 2: Microcontroller (Similar to Albatastic Compact)
1. **Preparation:** Insert header pins long-side down into the PCB resting on a flat surface. Place the Pro Micro on top.
2. **Solder Headers:** Solder one pin on each side, remove the Pro Micro, and solder all remaining pin headers to the board.
3. **Remove Plastic Spacers:** Carefully remove the plastic pin spacer strip using pliers or tweezers (avoid scratching the PCB!).
4. **Solder Pro Micro:** Push the Pro Micro all the way down onto the pins, solder, and trim excess pin length.

##### If you want a removable Pro Micro:
4. **Alternative:** Place female headers over the male pins already soldered to the board and push them all the way down.
5. **Solder Pro Micro:** Solder the Pro Micro onto the female headers.

#### 3️⃣ Step 3: BME280 Sensor (Optional)
1. Solder the **BME280** sensor on its dedicated pins for ambient temperature, humidity, and pressure monitoring.

#### 4️⃣ Step 4: Radio Regulator / Boost Module
* **E80 & RA62:** No module required, skip to next step.
* **QRP Mode (E28):** If not using an external boost module, solder the jumper to power the radio directly from the Pro Micro 3.3V line.
* **With Boost (E22/E22P):** Solder the boost board directly.
* **With Buck-Boost (E28/E22/E22P):** Solder the buck-boost board and check output voltage. For E28, set jumper selector to buck-boost position. For E22/E22P, set jumper for 5V output.

#### 5️⃣ Step 5: Radio Module
1. **Radio Module:** Solder the selected radio module (**E22P**, **E22**, **E80**, **E28**, or **HT-RA62**). Solder the E22/E22P selector jumper if applicable.
   * *⚠️ Never turn on or transmit with the radio without an antenna attached.*

#### 6️⃣ Step 6: MPPT Solar Charger Controller
1. Solder the MPPT charge controller module in the correct orientation.  
   * *⚠️ Double check CN3791 pinout and polarity.*

#### 7️⃣ Step 7: BMS & Batteries
1. **BMS:** Solder the BMS respecting polarity. A good trick is pre-tinning two pads on the BMS (2-3mm solder blob), flipping it over while holding with tweezers, and applying heat to melt and fuse the connection.
2. **Batteries:** Solder the battery holder. Insert 18650 batteries strictly observing polarity.
3. **Initial Power-On:** Attach antenna. On first boot, power must be applied via MPPT or Pro Micro USB-C to wake up and activate the BMS.

---

> 💡 **Usage Note:** This board is designed for simple and/or temporary client end-nodes. It is not recommended for heavy infrastructure router nodes due to its simplified design and lack of hardware resilience features. If you require resilient hardware and/or reset capability, check out [Albatastic Pro](https://github.com/EmilioAL-Git/PCB-Albatastic-PRO/tree/main).

---

## 📋 Historial de Cambios / Changelog

<details>
<summary><b>Click to expand / Clic para desplegar</b></summary>

<br>

### 🚧 v1.2 - Por testear / Untested
* **Añadido / Added:** Convertidor buck-boost de 3.3/5V adicional para el E22P/E28 / Additional 3.3V/5V buck-boost converter for E22P/E28.
* **Recolocado / Repositioned:** Interruptor ON/OFF / ON/OFF switch.
* **Mejora / Improvement:** Mejora estética para mejor legibilidad / Visual and legibility improvements.

### 🚧 v1.1 - Por testear / Untested
* **Corregido / Fixed:** La salida del CN3791 no estaba conectada / Unconnected output line on CN3791.
* **Corregido / Fixed:** El E28 no estaba conectado a 3.3V / E28 missing 3.3V connection.
* **Añadido / Added:** Opción de buck-boost de 3.3V/5V para E22P/E28 / 3.3V/5V buck-boost option for E22P/E28.
* **Añadido / Added:** Selector de alimentación para el E28 (Pro Micro para QRP, Buck-Boost para máxima potencia) / Power selector for E28 (Pro Micro QRP vs Buck-Boost full power).

### 🟢 v1.0 (Inicial / Initial) - Testeando / Testing
* **Diseño / Design:** Versión inicial de PCB *barebones* para nodos cliente / Initial barebones PCB version for client nodes.
* **Energía / Power:** Integración de soporte para doble batería 18650 y BMS / Dual 18650 battery holder & BMS support.
* **Radio:** Soporte multi-módulo (E22/E22P, E80, E28, HT-RA62) / Multi-module support (E22/E22P, E80, E28, HT-RA62).
* **Sensórica / Sensors:** Huella añadida para sensor BME280 / Footprint added for BME280 sensor.
* **Power:** Enrutado para boosters dedicados al E22/E22P y pads para módulos MPPT / Dedicated booster routing for E22/E22P and MPPT pads.

</details>

---

## 📐 Vista del Diseño / Design View

A continuación se muestra el render de la PCB / Below is the PCB render showing the elongated 3x Compact layout:

<p align="center">
  <img width="500" alt="Albatastic Scout PCB Render" src="https://github.com/user-attachments/assets/ff0325e0-aca7-458b-9571-c9f083cb64d4" />
</p>

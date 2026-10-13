# 🛰️ Albatastic Scout

> ⚠️ **Aviso de Responsabilidad / Legal Disclaimer:**  
> **🇪🇸:** Queda bajo la responsabilidad exclusiva del usuario final garantizar que la fabricación, configuración y uso de estas placas o dispositivos cumpla con la legislación y normativa de telecomunicaciones aplicable en su país o región.  
> **🇬🇧:** It is the sole responsibility of the end user to ensure that the assembly, configuration, and operation of these PCBs comply with applicable local telecommunications laws and regulations.

---

## 🇪🇸 Castellano

### PCB compacta para nodos solares sencillos y clientes de despliegue rápido

**Albatastic Scout** es una placa *barebones* de la familia Albatastic diseñada específicamente para actuar como nodo cliente solar sencillo. Es ideal para clientes finales y/o nodos temporales de despliegue rápido (acampadas, rutas, cruceros, etc.). Su diseño estilizado optimiza el espacio para albergar una gran capacidad de energía y compatibilidad de radio sin añadir florituras innecesarias.

### 🛠️ Características Principales

#### 📻 Conectividad y Control
- **Compatibilidad Multi-Radio:** Soporta módulos **E22 / E22P**, **E80**, **E28** y **HT-RA62**.
- **Cerebro (MCU):** NRF52840 Pro Micro de muy bajo consumo.
- **Sensor Integrado:** Espacio dedicado para un sensor ambiental **BME280** (presión, temperatura y humedad).

#### 🔋 Alimentación y Gestión Solar
- **Gran Autonomía:** Diseñada para alojar **2 baterías 18650** con su respectivo circuito BMS de protección (1S).
- **Flexibilidad MPPT:** Compatible con módulos de carga solar MPPT como el CN3795, CN3791 o SD30CRMA.
- **Regulación de Voltaje:** Posibilidad de montar hasta 2 *boosters* / conversores para alimentar los módulos E22/E22P o E28.
- **Control Físico:** Incluye un interruptor de encendido/apagado general (ON/OFF) integrado en la placa.

---

<details>
<summary><b>📦 Lista de Materiales (BOM) </b><i>(Haz clic para desplegar)</i></summary>
<br>

#### 🔹 1. Componentes Base (Comunes para todos los montajes)
Estos componentes son necesarios independientemente de la configuración elegida:

| Componente | Descripción / Modelo | Cant. | Enlace de Compra | Notas |
| :--- | :--- | :---: | :--- | :--- |
| **MCU / Cerebro** | NRF52840 Pro Micro | 1 | [🛒 Comprar](https://es.aliexpress.com/item/1005007383375306.html) | Microcontrolador principal de bajo consumo. |
| **Sensor (Opcional)** | Módulo BME280 | 1 | [🛒 Comprar](https://es.aliexpress.com/item/1005002963592665.html) | Medición de temperatura, humedad y presión. |
| **Soporte Baterías** | Portabaterías 1x 18650 | 2 | [🛒 Comprar](https://es.aliexpress.com/item/4000692031094.html) | Alojamiento para celdas Li-ion 18650. |
| **Protección Batería**| Circuito BMS 1S | 1 | [🛒 Comprar](https://es.aliexpress.com/item/1005008217119006.html) | Protección contra sobrecarga y sobredescarga. |
| **Interruptor** | Encendido/Apagado | 1 | [🛒 Comprar](https://es.aliexpress.com/item/1005006143122311.html) | Interruptor general de energía (ON/OFF). |
| **Resistencias 1206** | 1x 680K, 1x 1M (o 2x 1M) | 2 | [🛒 Comprar](https://es.aliexpress.com/item/1005002991902748.html) | Divisor de tensión para monitorear la batería. |
| **Botón Reset** | Pulsador táctil | 1 | [🛒 Comprar](https://es.aliexpress.com/item/4001125532910.html) | Pulsador SMD/PTH para reset. |
| **Baterías 18650** | Celdas Li-ion 18650 | 2 | [🛒 Comprar](https://www.nkon.nl/es/) | Se recomienda usar baterías nuevas y de calidad. |

#### 🔹 2. Guía de Selección de Componentes Configurables
Sigue estos pasos para seleccionar los componentes según la configuración de tu nodo:

**1️⃣ Paso 1: Elige el Módulo de Radio (Selecciona 1)**
| Opción | Módulo | Descripción / Características | Enlace |
| :--- | :--- | :--- | :---: |
| **A** | **E22P** | Semtech SX1262/SX1268. Recomendado para enlaces de máximo alcance y potencia LoRa. (433/868/915) | [🛒 Comprar](https://es.aliexpress.com/item/1005010297548005.html) |
| **B** | **E22** | Semtech SX1262/SX1268. Sin filtros integrados, disponible en más bandas. | [🛒 Comprar](https://es.aliexpress.com/item/1005009741346732.html) |
| **C** | **E80** | Módulo LoRa de bajo consumo para 433/868 MHz y 2.4GHz. | [🛒 Comprar](https://es.aliexpress.com/item/1005009119868850.html) |
| **D** | **E28** | Módulo LoRa de 2.4GHz. Ideal para alta velocidad de transmisión o redes locales cortas. | [🛒 Comprar](https://es.aliexpress.com/item/1005010288386483.html) |
| **E** | **HT-RA62** | Módulo ultra-compacto basado en SX1262. | [🛒 Comprar](https://es.aliexpress.com/item/1005008363549136.html) |

**2️⃣ Paso 2: Elige el Cargador Solar MPPT (Selecciona 1)**
| Opción | Módulo | Descripción / Aplicación | Enlace |
| :--- | :--- | :--- | :---: |
| **A** | **CN3791** | MPPT sencillo y fiable (6, 9 y 12V). *Revisar versión al recibir, el envío suele ser aleatorio.* | [🛒 Comprar](https://es.aliexpress.com/item/1005008286456080.html) |
| **B** | **CN3795** | MPPT con voltaje de entrada de panel flexible (9-18+V) y voltaje de salida ajustable. | [🛒 Comprar](https://es.aliexpress.com/item/1005009189097890.html) |
| **C** | **SD30CRMA** | Controlador sencillo para 9, 12 y 18V con salida ajustable. | [🛒 Comprar](https://es.aliexpress.com/item/1005007473789907.html) |

**3️⃣ Paso 3: Elige la Regulación / Boost para la Radio (Solo E22 / E22P / E28)**
| Opción | Alimentación | Descripción | Enlace |
| :--- | :--- | :--- | :---: |
| **A (E28)** | **Modo QRP** | Sin regulador dedicado. La radio usa los 3.3V del Pro Micro (Baja potencia). | N/A |
| **B** | **Mini Buck-Boost** | Mini módulo para alimentar el E22/E28 a 5V/3.3V respectivamente. | [🛒 Comprar](https://es.aliexpress.com/item/1005011637436564.html) |
| **C (E22/P)** | **Boost 5V 3A** | Elevador de tensión para alimentar el E22/E22P a 5V. | [🛒 Comprar](https://es.aliexpress.com/item/1005008051438437.html) |
| **D (E22/P)** | **HW-085** | Opción mini para alimentar el E22/E22P a 5V. | [🛒 Comprar](https://es.aliexpress.com/item/1005007013856492.html) |
| **E (V1.2+)** | **TPS63020** | Opción mini para alimentar el E22/E28 a 5V/3.3V respectivamente. | [🛒 Comprar](https://es.aliexpress.com/item/1005008099216597.html) |

*(Nota: Los enlaces no son afiliados)*
</details>

<details>
<summary><b>🔩 Instrucciones de Montaje </b><i>(Haz clic para desplegar)</i></summary>
<br>

> ⚠️ **Advertencia importante de seguridad:** Antes de colocar las baterías o conectar un panel solar, verifica SIEMPRE con un multímetro (modo continuidad) que no existen cortocircuitos entre VCC, 3.3V, 5V y GND.

Se recomienda realizar el ensamblaje siguiendo el método "de dentro hacia fuera" (perfil más bajo primero):

#### 1️⃣ Paso 1: Componentes Pasivos SMD y Botón Reset
1. **Resistencias SMD (1206):** Suelda las 2 resistencias del divisor de tensión (680K y 1M, o 2x 1M según tu configuración) destinadas al monitoreo del voltaje de batería.
2. **Control:** Suelda el **botón de reset**.
<p align="center"><img width="450" alt="Botón Reset y SMD" src="https://github.com/user-attachments/assets/a9409473-f548-42eb-82bb-4ad1ca9701d4" /></p>

#### 2️⃣ Paso 2: Microcontrolador (MCU)
1. **Paso previo:** Inserta la tira de pines por la cara larga a la PCB (apóyala sobre una mesa plana para que los pines no se hundan). Coloca el Pro Micro sobre los pines.
<p align="center"><img width="450" alt="Colocación de pines" src="https://github.com/user-attachments/assets/040c51aa-8b79-4a94-864d-5560db9f15ed" /></p>

2. **Fijación inicial:** Añade estaño a un pin de cada lado para fijar la tira y retira el Pro Micro. Acto seguido, suelda el resto de los pines a la placa principal.
3. **Retirar espaciador:** Elimina el separador de plástico negro de los pines con cuidado usando unas pinzas o alicates (¡cuidado de no rayar la PCB!).
<p align="center"><img width="450" alt="Eliminación del plástico" src="https://github.com/user-attachments/assets/c86b3496-590d-4df6-988b-60bc62861795" /></p>

4. **Soldar Pro Micro:** Empuja el Pro Micro hasta el fondo y suéldalo. Corta el sobrante de los pines.
<p align="center"><img width="450" alt="Soldadura del Pro Micro" src="https://github.com/user-attachments/assets/abfaf76c-c716-4578-8789-00339532d341" /></p>

> 💡 **Opción desmontable (Zócalo):** Si prefieres poder retirar el MCU sin desoldar, coloca pines hembra sobre los pines macho ya soldados a la placa. Empújalos hasta el fondo y suelda el Pro Micro sobre los pines hembra.
<p align="center"><img width="450" alt="Opción desmontable Pro Micro" src="https://github.com/user-attachments/assets/c834e84b-9a76-411f-a737-599288a12b1c" /></p>

#### 3️⃣ Paso 3: Regulador / Boost de Radio
- **E80 y RA62:** No es necesario regulador externo, avanza al siguiente paso.
- **Modo QRP (E28):** Si no usas módulo boost externo, suelda el jumper/selector para alimentar la radio directamente con los 3.3V del Pro Micro.
- **Con Boost (E22/E22P):** Suelda el módulo boost directamente a la placa.
- **Con Buck-Boost (E28/E22/E22P):** Suelda el buck-boost a la placa y comprueba con un multímetro el voltaje de salida antes de continuar. Para el E28, suelda el selector en posición *buck-boost*. Para E22/E22P, suelda el jumper para 5V.

#### 4️⃣ Paso 4: Módulo de Radio
1. Suelda el módulo de radio seleccionado (**E22P, E22, E80, E28 o HT-RA62**). 
2. Suelda el selector E22/E22P según corresponda (déjalo sin soldar si usas otro módulo).
> ⚠️ **NUNCA enciendas ni transmitas con la radio sin la antena conectada. Dañarás el amplificador de la radio.**

#### 5️⃣ Paso 5: Interruptor y Sensor BME280
1. **Sensor:** Suelda el **BME280** en sus pines dedicados.
2. **Interruptor:** Suelda el **interruptor On/Off** principal. *Consejo:* Corta las patas ligeramente, dale la vuelta a la PCB e introduce el interruptor hasta que quede a ras por la cara de las baterías antes de soldar. Debe quedar perfectamente plano.
<p align="center"><img width="450" alt="Interruptor y Sensor BME" src="https://github.com/user-attachments/assets/92099a40-0d97-4dfa-82c5-f6a467fbbd49" /></p>

#### 6️⃣ Paso 6: Controlador de carga MPPT
1. Suelda el controlador MPPT en la posición correcta.
> ⚠️ **OJO** con la polaridad y pinout si usas el módulo **CN3791**.

#### 7️⃣ Paso 7: BMS y Baterías
1. **BMS:** Suelda el BMS respetando estrictamente la polaridad. *Truco:* Pon una pequeña gota de estaño en dos pads del BMS (2-3mm de altura), dale la vuelta sujetándolo con pinzas, y aplica calor por debajo de la placa para fundirlo y unirlo.
2. **Portabaterías:** Suéldalo a la placa e inserta las baterías 18650 prestando atención a la polaridad.
3. **Encendido Inicial:** Conecta la antena. En el primer uso, es necesario aplicar corriente (vía panel solar al MPPT o cable USB-C al Pro Micro) para "despertar" y activar el circuito BMS.
</details>

> 💡 **Nota de Uso:** Esta placa está pensada para ser un nodo cliente final (Client) o repetidor temporal sencillo. No se recomienda su uso como Router de infraestructura pesada o en ubicaciones inaccesibles debido a su enfoque simplificado (ausencia de hardware watchdog/reseteo automático). Si necesitas un nodo de infraestructura robusto y resiliente, te recomendamos la [Albatastic Pro](https://github.com/EmilioAL-Git/PCB-Albatastic-PRO/tree/main).

---

## 🇬🇧 English

### Compact PCB for simple solar nodes and quick-deployment clients

**Albatastic Scout** is a barebones board from the Albatastic family, specifically designed to act as a simple solar client node. It is ideal for lightweight client setups and/or temporary rapid-deployment nodes (camping, hiking, cruises, etc.). Its streamlined layout optimizes space to accommodate high battery capacity and multi-radio compatibility without unnecessary frills.

### 🛠️ Key Features

#### 📻 Connectivity & Control
- **Multi-Radio Compatibility:** Supports **E22 / E22P**, **E80**, **E28**, and **HT-RA62** modules.
- **Brain / MCU:** Ultra-low-power NRF52840 Pro Micro.
- **Integrated Sensors:** Dedicated footprint for a **BME280** environmental sensor (pressure, temperature, and humidity).

#### 🔋 Power & Solar Management
- **High Autonomy:** Designed to hold **two 18650 batteries** with a matching 1S BMS protection circuit.
- **MPPT Flexibility:** Compatible with solar MPPT charger modules like the CN3795, CN3791, and SD30CRMA.
- **Voltage Regulation:** Capability to mount up to 2 boost converters to adequately power high-output E22/E22P or E28 modules.
- **Physical Control:** Onboard master ON/OFF toggle switch included.

---

<details>
<summary><b>📦 Bill of Materials (BOM) </b><i>(Click to expand)</i></summary>
<br>

#### 🔹 1. Base Components (Common for all builds)
These components are required regardless of your chosen radio/power configuration:

| Component | Description / Model | Qty | Purchase Link | Notes |
| :--- | :--- | :---: | :--- | :--- |
| **MCU / Brain** | NRF52840 Pro Micro | 1 | [🛒 Buy](https://es.aliexpress.com/item/1005007383375306.html) | Low-power main microcontroller. |
| **Sensor (Optional)** | BME280 Module | 1 | [🛒 Buy](https://es.aliexpress.com/item/1005002963592665.html) | Temperature, humidity, and pressure. |
| **Battery Holder** | 1x 18650 Holder | 2 | [🛒 Buy](https://es.aliexpress.com/item/4000692031094.html) | Enclosure for 18650 Li-ion cells. |
| **Battery Protection**| 1S BMS Circuit | 1 | [🛒 Buy](https://es.aliexpress.com/item/1005008217119006.html) | Overcharge and overdischarge protection. |
| **Switch** | Power ON/OFF Switch | 1 | [🛒 Buy](https://es.aliexpress.com/item/1005006143122311.html) | Main power toggle switch. |
| **1206 Resistors** | 1x 680K, 1x 1M (or 2x 1M) | 2 | [🛒 Buy](https://es.aliexpress.com/item/1005002991902748.html) | Resistors for battery voltage monitoring. |
| **Reset Button** | Tactile Push Button | 1 | [🛒 Buy](https://es.aliexpress.com/item/4001125532910.html) | SMD/PTH reset push button. |
| **18650 Batteries** | 18650 Li-ion Cells | 2 | [🛒 Buy](https://www.nkon.nl/es/) | Recommended to use new, high-quality cells. |

#### 🔹 2. Configurable Component Selection Guide
Follow these steps to choose components based on your intended node setup:

**1️⃣ Step 1: Select the Radio Module (Select 1)**
| Option | Module | Description / Features | Purchase Link |
| :--- | :--- | :--- | :---: |
| **A** | **E22P** | Semtech SX1262/SX1268. Recommended for ultra-long-range links & maximum LoRa power. (433/868/915 MHz) | [🛒 Buy](https://es.aliexpress.com/item/1005010297548005.html) |
| **B** | **E22** | Semtech SX1262/SX1268. Unfiltered variant, available in additional frequency bands. | [🛒 Buy](https://es.aliexpress.com/item/1005009741346732.html) |
| **C** | **E80** | Ultra-low power LoRa module for 433/868 MHz and 2.4GHz. | [🛒 Buy](https://es.aliexpress.com/item/1005009119868850.html) |
| **D** | **E28** | 2.4GHz LoRa module. Ideal for high data throughput or local mesh networks. | [🛒 Buy](https://es.aliexpress.com/item/1005010288386483.html) |
| **E** | **HT-RA62** | Ultra-compact module based on SX1262. | [🛒 Buy](https://es.aliexpress.com/item/1005008363549136.html) |

**2️⃣ Step 2: Select Solar Charger (MPPT) (Select 1)**
| Option | Module | Description / Application | Purchase Link |
| :--- | :--- | :--- | :---: |
| **A** | **CN3791** | Simple, reliable MPPT (6V, 9V, 12V). *Verify the board received, as suppliers often mix versions.* | [🛒 Buy](https://es.aliexpress.com/item/1005008286456080.html) |
| **B** | **CN3795** | MPPT controller with flexible panel input voltage (9-18+V) and adjustable output voltage. | [🛒 Buy](https://es.aliexpress.com/item/1005009189097890.html) |
| **C** | **SD30CRMA**| Simple controller for 9V, 12V, and 18V panels with adjustable output. | [🛒 Buy](https://es.aliexpress.com/item/1005007473789907.html) |

**3️⃣ Step 3: Select Radio Regulation / Boost Module (Only for E22 / E22P / E28)**
| Option | Power Mode | Description | Purchase Link |
| :--- | :--- | :--- | :---: |
| **A (E28)** | **QRP Mode** | No dedicated regulator. The radio is powered directly from the Pro Micro 3.3V rail. | N/A |
| **B** | **Mini Buck-Boost**| Compact option to power E22/E28 at 5V/3.3V respectively. | [🛒 Buy](https://es.aliexpress.com/item/1005011637436564.html) |
| **C (E22/P)** | **Boost 5V 3A** | Power module to supply a stable 5V to the E22/E22P. | [🛒 Buy](https://es.aliexpress.com/item/1005008051438437.html) |
| **D (E22/P)** | **HW-085** | Mini boost option to power E22/E22P at 5V. | [🛒 Buy](https://es.aliexpress.com/item/1005007013856492.html) |
| **E (V1.2+)** | **TPS63020** | Mini option to power E22/E28 at 5V/3.3V respectively. | [🛒 Buy](https://es.aliexpress.com/item/1005008099216597.html) |

*(Note: Links are non-affiliated)*
</details>

<details>
<summary><b>🔩 Assembly Instructions </b><i>(Click to expand)</i></summary>
<br>

> ⚠️ **Important Safety Warning:** Before inserting batteries or connecting a solar panel, ALWAYS use a multimeter in continuity mode to verify that there are no short circuits between VCC, 3.3V, 5V, and GND.

Assembly should proceed using the "inside-out" method (solder the lowest-profile components first):

#### 1️⃣ Step 1: SMD Passive Components & Reset Button
1. **SMD Resistors (1206):** Solder the 2 voltage divider resistors (680K and 1M, or 2x 1M depending on configuration) used for battery monitoring.
2. **Control:** Solder the **reset push button**.
<p align="center"><img width="450" alt="Reset Button and SMD" src="https://github.com/user-attachments/assets/a9409473-f548-42eb-82bb-4ad1ca9701d4" /></p>

#### 2️⃣ Step 2: Microcontroller (MCU)
1. **Preparation:** Insert header pins long-side down into the PCB resting on a flat surface. Place the Pro Micro on top.
<p align="center"><img width="450" alt="Header pin alignment" src="https://github.com/user-attachments/assets/040c51aa-8b79-4a94-864d-5560db9f15ed" /></p>

2. **Tack and Solder:** Solder one pin on each side to secure the headers, remove the Pro Micro, and solder all remaining header pins directly to the board.
3. **Remove Plastic Spacers:** Carefully remove the black plastic spacer strips using pliers or tweezers (avoid scratching the PCB traces!).
<p align="center"><img width="450" alt="Removing plastic spacer" src="https://github.com/user-attachments/assets/c86b3496-590d-4df6-988b-60bc62861795" /></p>

4. **Solder Pro Micro:** Push the Pro Micro all the way down onto the pins, solder them, and trim any excess pin length protruding from the top.
<p align="center"><img width="450" alt="Soldering Pro Micro" src="https://github.com/user-attachments/assets/abfaf76c-c716-4578-8789-00339532d341" /></p>

> 💡 **Removable Alternative (Socket):** Place female headers over the male pins already soldered to the board and push them all the way down. Solder the Pro Micro onto the female headers.
<p align="center"><img width="450" alt="Removable Pro Micro assembly" src="https://github.com/user-attachments/assets/c834e84b-9a76-411f-a737-599288a12b1c" /></p>

#### 3️⃣ Step 3: Radio Regulator / Boost Module
- **E80 & RA62:** No module required, skip to the next step.
- **QRP Mode (E28):** If not using an external boost module, solder the jumper to power the radio directly from the Pro Micro 3.3V line.
- **With Boost (E22/E22P):** Solder the boost board directly.
- **With Buck-Boost (E28/E22/E22P):** Solder the buck-boost board and check the output voltage with a multimeter before continuing. For E28, set the jumper selector to the buck-boost position. For E22/E22P, set the jumper for 5V output.

#### 4️⃣ Step 4: Radio Module
1. Solder the selected radio module (**E22P, E22, E80, E28, or HT-RA62**). 
2. Solder the E22/E22P selector jumper if applicable.
> ⚠️ **NEVER turn on or transmit with the radio without an antenna attached. This will permanently damage the amplifier.**

#### 5️⃣ Step 5: Power Switch & BME280 Sensor
1. **Sensor:** Solder the **BME280** module on its dedicated pins.
2. **Power Switch:** Solder the main **ON/OFF switch**. *Tip:* Trim the leads slightly, flip the PCB, insert until the leads are flush with the battery side, and solder. Ensure it sits completely flat.
<p align="center"><img width="450" alt="Power Switch and BME Sensor" src="https://github.com/user-attachments/assets/92099a40-0d97-4dfa-82c5-f6a467fbbd49" /></p>

#### 6️⃣ Step 6: MPPT Solar Charger Controller
1. Solder the MPPT charge controller module in the correct orientation.  
> ⚠️ **DOUBLE CHECK** the CN3791 pinout and polarity before soldering.

#### 7️⃣ Step 7: BMS & Batteries
1. **BMS:** Solder the BMS respecting polarity. *Trick:* Pre-tin two pads on the BMS (with a 2-3mm solder blob), flip it over while holding it with tweezers, and apply heat to the bottom of the board to melt and fuse the connection.
2. **Batteries:** Solder the battery holders in place. Insert 18650 batteries strictly observing polarity.
3. **Initial Power-On:** Attach an antenna. On first boot, power must be applied via the MPPT input or Pro Micro USB-C to "wake up" and activate the BMS protection circuit.
</details>

> 💡 **Usage Note:** This board is designed for simple, temporary client end-nodes. It is not recommended for heavy infrastructure router nodes or hard-to-reach locations due to its simplified design and lack of automatic hardware reset features. If you require resilient infrastructure hardware, check out [Albatastic Pro](https://github.com/EmilioAL-Git/PCB-Albatastic-PRO/tree/main).

---

## 📋 Historial de Cambios / Changelog

<details>
<summary><b>Click to expand / Clic para desplegar</b></summary>
<br>

### 🚧 v1.2.1 - Por testear / Untested
- **Corregido / Fixed:** Corregido problema de conexión que impedía el uso del HT RA62 / Fixed connection issue preventing the use of the HT RA62.

### 🟢 v1.2 - Testeada / Tested
- **Añadido / Added:** Convertidor buck-boost de 3.3/5V adicional para el E22P/E28 / Additional 3.3V/5V buck-boost converter support for E22P/E28.
- **Recolocado / Repositioned:** Interruptor ON/OFF para mejor accesibilidad / ON/OFF switch moved for better accessibility.
- **Mejora / Improvement:** Mejoras estéticas y en la legibilidad de la serigrafía / Visual layout and silkscreen legibility improvements.

### 🚧 v1.1 - Por testear / Untested
- **Corregido / Fixed:** La salida del CN3791 no estaba conectada / Unconnected output line on CN3791.
- **Corregido / Fixed:** El E28 no estaba conectado a 3.3V / E28 missing 3.3V connection.
- **Añadido / Added:** Opción de buck-boost de 3.3V/5V para E22P/E28 / 3.3V/5V buck-boost option for E22P/E28.
- **Añadido / Added:** Selector de alimentación para el E28 (Pro Micro para QRP, Buck-Boost para máxima potencia) / Power selector for E28 (Pro Micro QRP vs Buck-Boost full power).

### 🟢 v1.0 (Inicial / Initial) - Testeada / Tested
- **Diseño / Design:** Versión inicial de PCB *barebones* para nodos cliente / Initial barebones PCB version for client nodes.
- **Energía / Power:** Integración de soporte para doble batería 18650 y BMS / Dual 18650 battery holder & BMS support.
- **Radio:** Soporte multi-módulo (E22/E22P, E80, E28, HT-RA62) / Multi-module support (E22/E22P, E80, E28, HT-RA62).
- **Sensórica / Sensors:** Huella añadida para sensor BME280 / Footprint added for BME280 sensor.
- **Regulación / Boost:** Enrutado para boosters dedicados al E22/E22P y pads para módulos MPPT / Dedicated booster routing for E22/E22P and MPPT pads.
</details>

---

## 📐 Vista del Diseño / Design View

A continuación se muestra el render de la PCB / Below is the PCB render showing the elongated layout:

<p align="center">
  <img width="550" alt="Albatastic Scout PCB Render" src="https://github.com/user-attachments/assets/ff0325e0-aca7-458b-9571-c9f083cb64d4" />
</p>

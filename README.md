# 🛰️ Albatastic Scout
### PCB compacta para nodos solares sencillos y clientes de despliegue rápido

**Albatastic Scout** es una placa *barebones* de la familia Albatastic diseñada específicamente para actuar como nodo cliente solar sencillo, ideal para clientes sencillos y/o nodos temporales (Acampadas, camping, cruceros, etc). Su diseño estilizado optimiza el espacio para albergar una gran capacidad de energía y compatibilidad de radio sin añadir florituras.

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
| **Botón reset** | Botón de reset | 1 | [🛒 Comprar](https://es.aliexpress.com/item/4001125532910.html) | Pulsador SMD/PTH para reset |
| **Baterías 18650** | Baterías 18650 | 2 | [🛒 Comprar](https://www.nkon.nl/es/) | Recomiendo usar baterías nuevas y de calidad |

---

### 🔹 2. Guía de Selección de Componentes Configurables

Sigue estos pasos para seleccionar los componentes según la configuración de tu nodo:

#### 1️⃣ **Paso 1: Elige el Módulo de Radio** *(Selecciona 1)*

| Opción | Módulo | Descripción / Características | Enlace de Compra |
| :--- | :--- | :--- | :---: |
| **Opción A** | **E22P** | Semtech SX1262 / SX1268. Recomendado para enlaces de muy largo alcance y máxima potencia LoRa. Disponible en 433, 868 y 915 | [🛒 Comprar](https://es.aliexpress.com/item/1005010297548005.html) |
| **Opción B** | **E22** | Semtech SX1262 / SX1268. Sin filtros integrados, disponible en más bandas | [🛒 Comprar](https://es.aliexpress.com/item/1005009741346732.html) |
| **Opción C** | **E80** | Módulo LoRa de bajo consumo de 433/868 y 2.4GHz | [🛒 Comprar](https://es.aliexpress.com/item/1005009119868850.html) |
| **Opción D** | **E28** | Módulo LoRa de 2.4GHz. Ideal para alta velocidad de transmisión o redes locales. | [🛒 Comprar](https://es.aliexpress.com/item/1005010288386483.html) |
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
| **Opción A (E28)** | **Modo QRP** *(Sin regulador dedicado)* | La radio se alimenta directamente de los 3.3V del Pro Micro. Para transmisiones QRP con E28. | N/A |
| **Opción B** | **Mini Buck-Boost 3.3V / 5V** | Opción mini para alimentar el E22/E28 a 5/3.3V respectivamente | [🛒 Comprar](https://es.aliexpress.com/item/1005011637436564.html) |
| **Opción C (E22/E22P)** | **Boost 5V 3A** | Opción para alimentar el E22/E22P a 5V | [🛒 Comprar](https://es.aliexpress.com/item/1005007013856492.html) |
| **Opción D (E22/E22P)** | **HW-085** | Opción mini para alimentar el E22 a 5V respectivamente | [🛒 Comprar](https://es.aliexpress.com/item/1005008051438437.html) |

*(Enlaces no afiliados)*

---

## 🔩 Instrucciones de Montaje

> ⚠️ **Advertencia importante de seguridad:** Antes de colocar las baterías o conectar un panel solar, verifica con un multímetro en modo continuidad que no existen cortocircuitos entre VCC, 3.3V, 5V y GND.

Se recomienda realizar el ensamblaje siguiendo el método de empezar por dentro e ir hacia fuera:

#### 1️⃣ **Paso 1: Componentes Pasivos SMD e interruptor**
1. **Resistencias SMD (1206):** Soldar las 2 resistencias del divisor de tensión (680K y 1M, o 2x 1M según tu configuración) destinadas al monitoreo del voltaje de batería.
2. **Control:** Soldar el **botón de reset** y el **interruptor On/Off** principal en la placa. Para soldar el interruptor, recomiendo cortarle las patas algo, darle la vuelta a la PCB, introducir el interruptor hasta que las patas se queden a ras de la cara donde van las baterías y añadir estaño. Hay que asegurarse de que se quede plano

#### 2️⃣ **Paso 2: Micro Controlador** (Similiar a la Albatastic compact)
1. **Paso previo:** Insertar la tira de pines por la cara larga a la PCB. (asegúrate de hacerlo apoyado sobre una mesa para que estos no se introduzcan para abajo). Apoyar el promicro sobre los pines
2. **Añadir estaño:** Añade estaño a uno de los pines de la tira a cada lado y retira el promicro. Acto seguido, suelda todos los pines
3. **Elimina el plástico de los pines:** Elimina el separador de los pines, con cuidado y valiendote de unas pinzas, alicates, etc (sin rallar la PCB OJO!!)
4. **Suelda el promicro:** Empuja el promicro hasta el fondo y sueldalo. Corta el sobrante

Si quieres poder quitar el ProMicro sin desoldar:
4a. **Importante:** Coloca unos pines hembra sobre los pines macho ya soldados a la placa y empújalos hasta el fondo.
5a. **Suelda el promicro:** Suelda el pro micro como en el paso 5 normal.

#### 3️⃣ **Paso 3: Sensor BME280 (Opcional)**
1. Soldar el sensor **BME280** en sus pines dedicados para mediciones de temperatura, humedad y presión.

#### 4️⃣ **Paso 4: Regulador / Boost de Radio (según selección de alimentación)**
* **E80 y RA62:** No es necesario nada, avanza al siguiente paso.
* **Modo QRP (E28):** Si no usas módulo boost externo, suelda el selector para alimentar la radio directamente con los 3.3V del Pro Micro.
* **Con boost (E22/E22P):** Suelda el boost a la placa directamente.
* **Con buck-boost (E28/E22/E22P):** Suelda el buck boost a la placa y comprueba el voltaje que da. Para el E28, suelda el selector de alimentación en posición buck-boost. Para el E22/E22P, suelda el jumper para 5V

#### 4️⃣ **Paso 4: Módulo de Radio y Microcontrolador**
1. **Módulo de Radio:** Suelda la radio seleccionada (**E22P**, **E22**, **E80**, **E28** o **HT-RA62**). Suelda el selector E22/E22P según corresponda (o dejalo sin soldar si no es ninguno de estos dos)
   * *⚠️ Nunca enciendas ni transmitas con la radio sin la antena conectada.*

#### 5️⃣ **Paso 5: Controlador de carga MPPT**
1. Suelda el controlador de carga MPPT en la posición correcta. 
* *⚠️ OJO con la polaridad de los CN3791.*

#### 6️⃣ **Paso 6: BMS y baterías**
1. **BMS:** Suelda el BMS respetando la polaridad. Para ello es recomendable soldar este en un ángulo o con cierta separación. Un truco consiste en poner estaño en dos pads del BMS (hasta que sobresalga 2-3mm), y luego, darle la vuelta y mientras lo sujetas con unas pinzas, aplicar calor al estaño para que se funda y se una
2. **Baterías:** Suelda el porta baterías. Inserta las baterías respetando la polaridad.
3. **Encendido inicial:** Conecta la antena. En el primer encendido, es necesario encenderlo con el MPPT o el USB-C del pro micro, para activar el BMS

---

<details>
<summary><b>📋 Historial de Cambios (Changelog)</b></summary>

<br>

### 🚧 v1.2 - Por testear
* **Añadido:** Añadido otro convertidor buck-boost de 3.3/5V para el E22P/E28.
* **Recolocado:** Recolocado el interruptor on-off.
* **Mejora:** Mejora en estética para un mejor entendimiento.


### 🚧 v1.1 - Por testear
* **Corregido:** Corregido que la salida del CN3791 no estaba conectada.
* **Corregido:** El E28 no estaba conectado a 3.3V.
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

> 💡 **Nota de uso:** Esta placa está pensada para nodos finales (Clients) sencillos y/o temporales. No se recomienda su uso como Router de infraestructura pesada debido a su enfoque simplificado y la ausencia de hardware resiliente. Si necesitas hardware resiliente y/o reset, te recomiendo la [Albatastic Pro](https://github.com/EmilioAL-Git/PCB-Albatastic-PRO/tree/main)

# 🛰️ Albatastic Scout
### PCB compacta para nodos solares sencillos y clientes de despliegue rápido

**Albatastic Scout** es una placa *barebones* de la familia Albatastic diseñada específicamente para actuar como nodo cliente autónomo o baliza temporal (ideal para acampadas y exteriores). Su diseño estilizado optimiza el espacio para albergar una gran capacidad de energía y compatibilidad de radio sin añadir florituras.

---

## 🛠️ Características Principales

### 📻 Conectividad y Control
*   **Compatibilidad Multi-Radio:** Soporta módulos **E22/E22P**, **E80**, **E28** y **HT-RA62**.
*   **Cerebro:** NRF52840 Pro Micro de bajo consumo .
*   **Sensor Integrado:** Espacio dedicado para un sensor ambiental **BME280** (presión, temperatura y humedad).

### 🔋 Alimentación y Gestión Solar
*   **Gran Autonomía:** Diseñada para alojar **2 baterías 18650** con su respectivo circuito BMS de protección.
*   **Flexibilidad MPPT:** Compatible con módulos MPPT como el CN3795 / CN3791 / SD30CRMA.
*   **Regulación de Voltaje:** Posibilidad de montar 2 boosters para el E22/E22P
*   **Control Físico:** Incluye un interruptor de encendido/apagado general en placa.

---

## 📐 Vista del Diseño

A continuación se muestra el render de la PCB, donde se puede apreciar la distribución alargada equivalente a 3 placas *Compact* de ancho, optimizando el espacio para el módulo solar y el portabaterías trasero:

<p align="center">
  <img width="500" alt="Albatastic Scout PCB Render" src="https://github.com/user-attachments/assets/ff0325e0-aca7-458b-9571-c9f083cb64d4" />
</p>

---

> 💡 **Nota de uso:** Esta placa está pensada para nodos finales (Clients) sencillos y/o temporales. No se recomienda su uso como Router de infraestructura pesada debido a su enfoque simplificado y la ausencia de hardware resiliente.

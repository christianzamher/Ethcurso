# KipuBank - Smart Contract

**Descripción**:
Un contrato de bóveda personal que permite a los usuarios depositar y retirar ETH con límites de seguridad:
- **Límite global de depósitos** (`bankCap`): Máximo total de ETH que el banco puede almacenar.
- **Límite por retiro** (`withdrawalLimit`): Máximo que un usuario puede retirar en una transacción.
- **Eventos**: Registra depósitos/retiros y actualiza contadores.
- **Seguridad**: Usa `checks-effects-interactions`, errores personalizados y transferencias seguras.

---

## 🛠 Despliegue

### Requisitos
- [Remix IDE](https://remix.ethereum.org/) (o Hardhat/Foundry).
- MetaMask con fondos en una **testnet** (ej: Sepolia).
- Solidity ^0.8.20.

### Pasos
1. **Compilar**:
   - Abre el archivo en Remix (`contracts/KipuBank.sol`).
   - Selecciona el compilador **0.8.20** y compila.

2. **Desplegar**:
   - Ve a la pestaña **Deploy & Run**.
   - Conecta MetaMask a la testnet (ej: Sepolia).
   - Ingresa los parámetros del constructor:
     - `_bankCap`: Ej: `100 ether` (límite global).
     - `_withdrawalLimit`: Ej: `1 ether` (límite por retiro).
   - Haz clic en **Deploy**.

3. **Verificar en Etherscan** (opcional):
   - Copia la dirección del contrato desplegado.
   - Ve a [Etherscan](https://sepolia.etherscan.io/) > **Verify Contract**.
   - Pega el código y selecciona el compilador **0.8.20**.

---

## 🤖 Interacción

### Funciones clave
| Función          | Descripción                                  | Ejemplo (Remix)               |
|------------------|----------------------------------------------|-------------------------------|
| `deposit()`       | Deposita ETH en tu bóveda (envía valor).      | `deposit{value: 0.5 ether}()` |
| `withdraw(uint)` | Retira ETH (hasta `withdrawalLimit`).        | `withdraw(0.3 ether)`         |
| `getBalance()`    | Consulta tu saldo.                          | `getBalance("0xTuDireccion")` |

### Eventos
- **Deposit**: Emite al depositar (user, amount, newBalance).
- **Withdrawal**: Emite al retirar (user, amount, newBalance).

---

## 🔗 Contrato Desplegado
- **Testnet**: [Sepolia](https://sepolia.etherscan.io/)
- **Dirección**: [`0x...`](https://sepolia.etherscan.io/address/0x...) *(reemplaza con tu dirección)*
- **Código verificado**: [Ver en Etherscan](#) *(opcional)*

---

---

## 🌐 Contacto 
- LinkedIn: [[Visitame en LinkedIn](https://www.linkedin.com/in/christianzamorahermida/)]  
 

---
✦ *Este documento forma parte de mi primera etapa de aprendizaje y representa el inicio de mi participación activa en el ecosistema Web3.*  

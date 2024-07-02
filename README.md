# Sistema de Controle e Gerenciamento de Ordens de Serviço em Oficina Mecânica

## Descrição do Projeto Conceitual

Este projeto consiste em um esquema conceitual para um sistema de controle e gerenciamento de ordens de serviço em uma oficina mecânica. O sistema permite o gerenciamento eficiente das ordens de serviço, veículos, clientes, mecânicos, serviços e peças utilizadas.

### Entidades e Relacionamentos

1. **Cliente**
   - **Atributos**: 
     - `idCliente` (PK)
     - `Nome`
     - `Endereço`
     - `Contato`

2. **Veículo**
   - **Atributos**: 
     - `idVeículo` (PK)
     - `Modelo`
     - `Ano`
     - `Placa`
     - `idCliente` (FK)

3. **Mecânico**
   - **Atributos**: 
     - `idMecânico` (PK)
     - `Nome`
     - `Endereço`
     - `Especialidade`

4. **Ordem de Serviço (OS)**
   - **Atributos**: 
     - `idOrdem de Serviço` (PK)
     - `Data de Emissão`
     - `Valor Total`
     - `Status`
     - `idVeículo` (FK)
     - `idMecânico` (FK)

5. **Serviço**
   - **Atributos**: 
     - `idServiço` (PK)
     - `Descrição`
     - `Valor de Mão-de-Obra`

6. **Peça**
   - **Atributos**: 
     - `idPeça` (PK)
     - `Descrição`
     - `Preço`

7. **Serviço_OS**
   - **Atributos**:
     - `idOrdem de Serviço` (FK)
     - `idServiço` (FK)
     - `Quantidade`
     - `Valor Total`

8. **Peças Utilizadas**
   - **Atributos**:
     - `idOrdem de Serviço` (FK)
     - `idPeça` (FK)
     - `Quantidade`
     - `Valor Total`

### Relacionamentos:

- **Cliente** 1:1 **Veículo**
- **Veículo** 1:N **Ordem de Serviço (OS)**
- **Mecânico** 1:1 **Ordem de Serviço (OS)**
- **Ordem de Serviço (OS)** 1:N **Serviço_OS**
- **Serviço** 1:N **Serviço_OS**
- **Ordem de Serviço (OS)** 1:N **Peças Utilizadas**
- **Peça** 1:N **Peças Utilizadas**



Este esquema conceitual foi projetado para proporcionar um gerenciamento eficiente e organizado das operações de uma oficina mecânica, garantindo que todas as informações relevantes sejam capturadas e gerenciadas de forma eficaz.

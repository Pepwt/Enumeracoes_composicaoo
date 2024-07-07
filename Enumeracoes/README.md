# Worker Income Calculator

Este projeto é um sistema simples para calcular a renda de um trabalhador com base em seus contratos de horas. O sistema permite a inserção de dados de trabalhadores, contratos e cálculo da renda mensal de um trabalhador.

## Estrutura do Projeto

O projeto está estruturado da seguinte forma:

1. **entities.enums.WorkerLevel**: Enumeração para definir os níveis de um trabalhador (JUNIOR, MID_LEVEL, SENIOR).
2. **entities.Department**: Classe para representar o departamento de um trabalhador.
3. **entities.HourContract**: Classe para representar um contrato por hora, contendo a data, valor por hora e duração em horas.
4. **entities.Worker**: Classe principal que representa um trabalhador, contendo seus dados pessoais, departamento, lista de contratos e métodos para adicionar/remover contratos e calcular a renda.
5. **exe.Program**: Classe principal que contém o método `main` para execução do programa.

## Como Executar

### Pré-requisitos

- Java JDK 8 ou superior
- IDE de sua escolha (Eclipse, IntelliJ, VS Code, etc.)

### Passos

1. Clone este repositório para o seu ambiente local.
2. Abra o projeto na sua IDE de escolha.
3. Compile o projeto.
4. Execute a classe `Program` localizada no pacote `exe`.

### Uso

1. Insira o nome do departamento.
2. Insira os dados do trabalhador (nome, nível e salário base).
3. Insira a quantidade de contratos.
4. Para cada contrato, insira a data (formato DD/MM/YYYY), valor por hora e duração em horas.
5. Insira o mês e ano para calcular a renda (formato MM/YYYY).
6. O programa irá exibir o nome do trabalhador, departamento e renda para o mês/ano especificado.

### Exemplo de Entrada e Saída

**Entrada:**

Enter department's name: Development
Enter worker data:
Name: John
Level: MID_LEVEL
Base salary: 1200.00
How many contracts to this worker? 2
Enter contract #1 data:
Date (DD/MM/YYYY): 20/08/2023
Value per hour: 50.00
Duration (hours): 20
Enter contract #2 data:
Date (DD/MM/YYYY): 13/06/2023
Value per hour: 30.00
Duration (hours): 10
Enter month and year to calculate income (MM/YYYY): 08/2023


**Saída:**

Name: John
Department: Development
Income for 08/2023: 2200.00


### Classes e Métodos

- **WorkerLevel**
  - Enum para definir os níveis: JUNIOR, MID_LEVEL, SENIOR.

- **Department**
  - `String name`
  - Construtores, getters e setters

- **HourContract**
  - `Date date`
  - `double valuePerHour`
  - `Integer hours`
  - Construtores, getters e setters
  - `double totalValue()`: Calcula o valor total do contrato

- **Worker**
  - `String name`
  - `WorkerLevel level`
  - `Double baseSalary`
  - `Department department`
  - `List<HourContract> contracts`
  - Construtores, getters e setters
  - `void addContract(HourContract contract)`: Adiciona um contrato
  - `void removeContract(HourContract contract)`: Remove um contrato
  - `double income(int year, int month)`: Calcula a renda do trabalhador para um determinado mês e ano

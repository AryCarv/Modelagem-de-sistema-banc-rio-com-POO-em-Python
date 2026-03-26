# Sistema Bancário com POO em Python

Um sistema bancário implementado em Python utilizando os princípios de Programação Orientada a Objetos (POO). Este projeto demonstra o uso de classes, herança, propriedades, classes abstratas e padrões de design para criar uma aplicação completa de gerenciamento bancário.

## 📋 Funcionalidades

- **Gerenciamento de Clientes**: Criar e gerenciar informações de clientes (Pessoa Física)
- **Gerenciamento de Contas**: Criar contas correntes vinculadas aos clientes
- **Depósitos**: Realizar depósitos em contas bancárias
- **Saques**: Realizar saques com validação de saldo e limite
- **Extrato**: Consultar histórico de transações e saldo da conta
- **Validações**: 
  - Limite de saques por período
  - Limite de valor por saque
  - Verificação de saldo disponível
  - Validação de dados de entrada

## 🏗️ Arquitetura

### Classes Principais

#### `Cliente`
Classe base que representa um cliente do banco.
- Atributos: `endereco`, `contas`
- Métodos: `realizar_transacao()`, `adicionar_conta()`

#### `PessoaFisica`
Herança de `Cliente`, especializada para pessoas físicas.
- Atributos adicionais: `nome`, `data_nascimento`, `cpf`

#### `Conta`
Classe base para tipos de conta bancária.
- Atributos: `_saldo`, `_numero`, `_agencia`, `_cliente`, `_historico`
- Métodos: `sacar()`, `depositar()`
- Propriedades (Properties): `saldo`, `numero`, `agencia`, `cliente`, `historico`

#### `ContaCorrente`
Herança de `Conta`, implementa conta corrente com limites.
- Atributos adicionais: `limite`, `limite_saques`
- Sobrescreve método `sacar()` com validações específicas

#### `Historico`
Gerencia o histórico de transações de uma conta.
- Armazena informações: tipo, valor, data e hora

#### `Transacao` (Classe Abstrata)
Define a interface para transações bancárias.
- Métodos abstratos: `valor`, `registrar()`

#### `Saque` e `Deposito`
Implementações concretas de `Transacao`.

## 🚀 Como Usar

### Executando o programa

```bash
python desafio-v1.py

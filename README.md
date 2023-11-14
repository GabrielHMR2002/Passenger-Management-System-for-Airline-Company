# Sistema-de-Gerenciamento-de-Passageiros-para-Empresa-Aérea

# Linguagem utilizada: C

# Documentação do Projeto: Sistema de Gerenciamento de Passageiros para Empresa Aérea - Queda Livre

## Visão Geral

Este projeto implementa um sistema de gerenciamento de passageiros para uma fictícia empresa aérea chamada "Queda Livre". O sistema permite o cadastro, pesquisa, remoção e exibição de informações sobre passageiros, além de oferecer suporte para uma fila de espera.

## Funcionalidades Principais

### 1. Escolha de Voo

Ao iniciar o programa, o usuário é apresentado a um menu que oferece opções de voos disponíveis:

- BH-RIO (Opção 1)
- BH-SP (Opção 2)
- BH-BRASILIA (Opção 3)

O usuário seleciona o voo desejado e, a partir desse ponto, todas as operações são realizadas para o voo escolhido.

### 2. Menu de Operações

Após a escolha do voo, o sistema exibe um menu com as seguintes opções:

1. **Mostrar Lista de Passageiros:** Exibe a lista de passageiros cadastrados para o voo.
2. **Pesquisar Passageiro por CPF:** Permite a pesquisa de um passageiro por CPF.
3. **Pesquisar Passageiro por Nome:** Permite a pesquisa de um passageiro por nome.
4. **Cadastrar Passageiro:** Adiciona um novo passageiro ao voo.
5. **Excluir Passageiro da Lista:** Remove um passageiro do voo.
6. **Mostrar Fila de Espera:** Exibe a lista de passageiros em espera para o voo.
9. **Sair:** Encerra o programa.

### 3. Operações com Passageiros

#### 3.1. Mostrar Lista de Passageiros

- Exibe as informações de todos os passageiros cadastrados para o voo selecionado.
- Inclui detalhes como CPF, nome, endereço, telefone, número da passagem e número da poltrona.
- Se o voo não existir, uma mensagem adequada é exibida.

#### 3.2. Pesquisar Passageiro por CPF

- Permite a pesquisa de um passageiro por CPF.
- Exibe as informações do passageiro se encontrado, indicando CPF, nome, endereço, telefone, número da passagem e número da poltrona.
- Caso o passageiro não seja encontrado no voo, a pesquisa é estendida para a fila de espera.

#### 3.3. Pesquisar Passageiro por Nome

- Permite a pesquisa de um passageiro por nome.
- Exibe as informações do passageiro se encontrado, indicando CPF, nome, endereço, telefone, número da passagem e número da poltrona.
- Caso o passageiro não seja encontrado no voo, a pesquisa é estendida para a fila de espera.

#### 3.4. Cadastrar Passageiro

- Solicita informações do novo passageiro, como CPF, nome, endereço, telefone, número da passagem e número da poltrona.
- Verifica se há espaço no voo para cadastrar o passageiro. Se não houver, o passageiro é adicionado à fila de espera.
- Se a fila de espera também estiver cheia, o cadastro não é permitido.

#### 3.5. Excluir Passageiro da Lista

- Remove um passageiro do voo, liberando espaço para outros passageiros.
- Se o passageiro removido estiver na fila de espera, o próximo passageiro da fila é automaticamente movido para o voo.

#### 3.6. Mostrar Fila de Espera

- Exibe a lista de passageiros em espera para o voo selecionado.
- Apresenta as informações de CPF, nome, endereço, telefone, número da passagem e número da poltrona.

### 4. Controle de Espaço

- O sistema verifica a capacidade máxima de passageiros para um voo (`MAX_PASSAGEIROS`) e impede o cadastro caso o limite seja atingido.
- Uma fila de espera é implementada para acomodar passageiros quando o voo está lotado.

### 5. Persistência de Dados

- As informações dos passageiros e da fila de espera são armazenadas em arquivos de texto específicos para cada voo.
- Os arquivos seguem o formato `<nomeVoo>.txt` para os passageiros e `fila_<nomeVoo>.txt` para a fila de espera.


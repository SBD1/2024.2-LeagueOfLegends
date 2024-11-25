# Dicionário de Dados

## Tabela: Invocador
| **Atributo**   | **Tipo de Dados** | **Descrição**                              |
|----------------|--------------------|--------------------------------------------|
| id_invocador   | INT (PK)          | Identificador único do invocador.          |
| nome           | VARCHAR(100)      | Nome do invocador.                         |
| nivel          | INT               | Nível do invocador no jogo.                |

---

## Tabela: Campeao
| **Atributo**        | **Tipo de Dados** | **Descrição**                                   |
|---------------------|--------------------|-----------------------------------------------|
| id_campeao          | INT (PK)          | Identificador único do campeão.               |
| nome                | VARCHAR(100)      | Nome do campeão.                              |
| vida                | FLOAT             | Quantidade de vida inicial do campeão.        |
| dano_ataque         | FLOAT             | Valor do dano de ataque base do campeão.      |
| poder_habilidade    | FLOAT             | Valor do poder de habilidade base do campeão. |
| armadura            | FLOAT             | Valor da armadura base do campeão.            |
| resistencia_magica  | FLOAT             | Resistência mágica base do campeão.           |
| velocidade_ataque   | FLOAT             | Velocidade de ataque do campeão.              |

---

## Tabela: Habilidade
| **Atributo**   | **Tipo de Dados** | **Descrição**                              |
|----------------|--------------------|--------------------------------------------|
| id_habilidade  | INT (PK)          | Identificador único da habilidade.         |
| id_campeao     | INT (FK)          | Referência ao **id_campeao**.              |
| nome           | VARCHAR(100)      | Nome da habilidade.                        |
| descricao      | TEXT              | Descrição detalhada da habilidade.         |
| tipo           | VARCHAR(50)       | Tipo da habilidade (e.g., ativa, passiva). |
| dano           | FLOAT             | Dano causado pela habilidade.              |

---

## Tabela: Loja
| **Atributo**   | **Tipo de Dados** | **Descrição**                              |
|----------------|--------------------|--------------------------------------------|
| id_loja        | INT (PK)          | Identificador único da loja.               |
| nome           | VARCHAR(100)      | Nome da loja.                              |
| localizacao    | VARCHAR(100)      | Localização da loja no mapa.               |

---

## Tabela: Item
| **Atributo**       | **Tipo de Dados** | **Descrição**                              |
|--------------------|--------------------|--------------------------------------------|
| id_item            | INT (PK)          | Identificador único do item.               |
| id_loja            | INT (FK)          | Referência ao **id_loja**.                 |
| nome               | VARCHAR(100)      | Nome do item.                              |
| tipo_item          | VARCHAR(50)       | Tipo do item (e.g., lutador, mago, tanque).|
| atributo_bonus     | VARCHAR(100)      | Atributos adicionais concedidos pelo item. |
| preco              | FLOAT             | Preço do item em gold.                     |

---

## Tabela: Objetivo
| **Atributo**       | **Tipo de Dados** | **Descrição**                              |
|--------------------|--------------------|--------------------------------------------|
| id_objetivo        | INT (PK)          | Identificador único do objetivo.           |
| tipo_objetivo      | VARCHAR(50)       | Tipo do objetivo (e.g., torre, minion).    |
| recompensa_gold    | FLOAT             | Quantidade de gold ao ser abatido.         |
| boost_atributo     | VARCHAR(100)      | Atributos concedidos ao abater (se aplicável). |

---

## Tabela: PaginaRunas
| **Atributo**   | **Tipo de Dados** | **Descrição**                              |
|----------------|--------------------|--------------------------------------------|
| id_pagina      | INT (PK)          | Identificador único da página de runas.    |
| id_invocador   | INT (FK)          | Referência ao **id_invocador**.            |
| nome           | VARCHAR(100)      | Nome da página de runas.                   |
| categoria      | VARCHAR(50)       | Categoria (e.g., Precisão, Dominação).     |

---

## Tabela: Feitico
| **Atributo**   | **Tipo de Dados** | **Descrição**                              |
|----------------|--------------------|--------------------------------------------|
| id_feitico     | INT (PK)          | Identificador único do feitiço.            |
| id_invocador   | INT (FK)          | Referência ao **id_invocador**.            |
| nome           | VARCHAR(100)      | Nome do feitiço.                           |
| descricao      | TEXT              | Descrição detalhada do feitiço.            |

---

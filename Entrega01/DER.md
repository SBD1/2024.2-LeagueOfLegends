# Modelo Relacional

## 1. Entidades

  # **Invocador**
    id_invocador (PK): Identificador único do invocador.
    nome: Nome do invocador.
    nivel: Nível do invocador.
  # **Campeão**
    id_campeao (PK): Identificador único do campeão.
    nome: Nome do campeão.
    vida: Atributo de vida do campeão.
    dano_ataque: Atributo de dano de ataque.
    poder_habilidade: Poder de habilidade.
    armadura: Armadura do campeão.
    resistencia_magica: Resistência mágica do campeão.
    velocidade_ataque: Velocidade de ataque.
   # **Habilidade**
    id_habilidade (PK): Identificador único da habilidade.
    id_campeao (FK): Chave estrangeira que referencia o id_campeao.
    nome: Nome da habilidade.
    descricao: Descrição da habilidade.
    tipo: Tipo de habilidade (e.g., ativa, passiva).
    dano: Dano causado pela habilidade.
  # **Loja**
    id_loja (PK): Identificador único da loja.
    nome: Nome da loja.
    localizacao: Localização no mapa.
  # **Item**
    id_item (PK): Identificador único do item.
    id_loja (FK): Chave estrangeira que referencia o id_loja.
    nome: Nome do item.
    tipo_item: Categoria do item (e.g., lutador, mago, tanque, etc.).
    atributo_bonus: Atributos adicionais concedidos pelo item.
    preco: Preço do item.
 # **Objetivo**
    id_objetivo (PK): Identificador único do objetivo.
    tipo_objetivo: Tipo do objetivo (e.g., minion, torre, monstro da jungle, etc.).
    recompensa_gold: Gold concedido ao ser abatido.
    boost_atributo: Boost de atributos fornecido (aplicável a monstros únicos).
 # **PaginaRunas**
    id_pagina (PK): Identificador único da página de runas.
    id_invocador (FK): Chave estrangeira que referencia o id_invocador.
    nome: Nome da página de runas.
    categoria: Categoria da página (e.g., Precisão, Dominação, Feitiçaria, Inspiração).
 # **Feitiço**
    id_feitico (PK): Identificador único do feitiço.
    id_invocador (FK): Chave estrangeira que referencia o id_invocador.
    nome: Nome do feitiço.
    descricao: Descrição do feitiço.
## 2. Relacionamentos 
  | Entidade Relacionada  | Tipo de Relacionamento | Cardinalidade |
  | ------------- | ------------- | ------------- |
  | Invocador - Campeao  | 	Um para Muitos  | 	(1,1) → (1,n) |
  | Campeao - Habilidade | 	Um para Muitos  | (1,1) → (4,4) |
  | Campeao - Loja | 	Um para Muitos  | (1,n) → (1,n) |
  | Loja - Item  | Muitos para Muitos  | (1,n) → (1,n) |
  | Campeao - Objetivo | Content Cell  | (1,n) → (0,n) |








  

# Azure Cognitive Search: Configuração de Pesquisa com AI Search

Este repositório contém o passo a passo para configurar e utilizar o Azure Cognitive Search com indexação e consulta de dados. O serviço Azure Cognitive Search pode ser extremamente útil para empresas que precisam de soluções robustas de pesquisa e queiram integrar capacidades de inteligência artificial em suas consultas. 

## Passos para Configuração

### 1. Criar uma Conta no Azure

Para começar, você precisará de uma conta no [Azure](https://azure.microsoft.com/). Se ainda não tiver uma, siga as instruções do site para criar uma conta gratuita.

### 2. Criar um Serviço de Azure Cognitive Search

1. **Acesse o Portal do Azure**: Vá até o [Portal do Azure](https://portal.azure.com/).
2. **Crie um Novo Serviço de Pesquisa**: 
   - Na barra de pesquisa do portal, procure por "Azure Cognitive Search".
   - Selecione **Criar**.
   - Escolha a **associação de assinatura** e o **grupo de recursos**.
   - Defina o **nome do serviço de pesquisa**.
   - Selecione a **região** mais próxima de sua localização.
   - Selecione o **plano de preço** (basic, standard, etc.).
3. **Clique em Criar** para provisionar o serviço.

### 3. Configurar o Índice de Pesquisa

Um índice de pesquisa define a estrutura dos dados que serão armazenados e pesquisados. Para configurar o índice:

1. **Criar o Índice**: 
   - Vá até o serviço de **Azure Cognitive Search** criado.
   - No menu à esquerda, selecione **Índices** e depois **Adicionar índice**.
   - Defina as **propriedades** do índice, como nome, campos e tipos de dados.

Exemplo de índice:
```json
{
  "name": "produtos",
  "fields": [
    { "name": "id", "type": "Edm.String", "key": true },
    { "name": "nome", "type": "Edm.String" },
    { "name": "descricao", "type": "Edm.String" },
    { "name": "preco", "type": "Edm.Double" }
  ]
}

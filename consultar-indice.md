# Consulte o índice
Use o Search Explorer para escrever e testar consultas. Uma maneira fácil de validar a qualidade do seu índice de pesquisa. Você pode usar o Search Explorer para escrever consultas e revisar resultados em JSON. 

1️⃣ Na página inicial do seu Azure Aí Search, selecione *Explorador de Pesquisa* na parte superior da tela.

![explorador de pesquisa](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/create-cognitive-search-solution/5-exercise-screenshot-7.png)

2️⃣Observe como o índice selecionado é o índice de café que você criou. *Abaixo do índice* selecionado, *altere a visualização para a visualização JSON.*

![Alterar visualização ](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/create-cognitive-search-solution/search-explorer-query.png)

##### No campo do editor de consultas JSON, copie e cole:

        {
        "search": "locations:'Chicago'",
        "count": true
        }
3️⃣Selecione **Pesquisar** . A consulta de pesquisa retorna todos os documentos no índice de pesquisa, incluindo uma contagem de todos os documentos no campo **@odata.count** . O índice de pesquisa deve retornar um documento JSON contendo os resultados da pesquisa.

4️⃣ Agora vamos **filtrar por localização** No campo **do editor de consultas JSON** , copie e cole:

    {
    "search": "locations:'Chicago'",
    "count": true
    }

5️⃣ Selecione **Pesquisar** . A consulta pesquisa todos os documentos no índice e filtra revisões com localização em Chicago. Você deveria ver **3** no **@odata.countcampo.**

6️⃣ Agora vamos **filtrar por sentimento.** No campo do editor de consultas JSON , copie e cole:

    {
     "search": "sentiment:'negative'",
     "count": true
    }

7️⃣Selecione **Pesquisar**. A consulta pesquisa todos os documentos no índice e filtra revisões com sentimento negativo. Você deveria ver **1** no **@odata.countcampo.**

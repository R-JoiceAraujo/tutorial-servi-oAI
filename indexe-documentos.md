# Indexe os documentos 📄 

Depois de ter os documentos armazenados, você pode usar o Azure AI Search para extrair insights dos documentos.

1️⃣ No portal Azure, navegue até o seu recurso Azure AI Search. Na página *Visão Geral, selecione **Importar dados*.
![importar dados](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/create-cognitive-search-solution/azure-search-wizard-1.png)

2️⃣ Na página *Conectar aos seus dados, na lista **Fonte de Dados, selecione **Azure Blob Storage*. Complete os campos com os seguintes dados:

* *Fonte de Dados*: Azure Blob Storage;
* ⁠*Nome da fonte de dados*: coffee-customer-data;
* ⁠*Dados a serem extraídos:* Conteúdo e metadados;
* ⁠*Modo de análise*: Padrão
* ⁠*String de conexão:* Selecione Escolha uma conexão existente. Selecione sua conta de armazenamento, selecione o recipiente de revisões de café e clique em Selecionar.
* ⁠*Autenticação de identidade gerenciada:* Nenhuma
* ⁠*Nome do contêiner*: esta configuração é preenchido automaticamente depois que você escolhe uma conexão existente.
* ⁠*Pasta Blob:* Deixe isso em branco.
* ⁠*Descrição:* Avaliações para as quartas cafeterias.

3️⃣Selecione *Próximo: Adicionar habilidades cognitivas (Opcional).*

4️⃣Na seção *Anexar Serviços Cognitivos*, selecione seu recurso de serviços Azure AI.

5️⃣Na seção *Adicionar enriquecimentos*:

* Mude o nome do *Skillset* para coffee-skillset.
* ⁠Selecione a caixa de seleção *Ativar OCR e mesclar todo o texto no campo merged_content.*✅
* Certifique-se de que o campo de *dados de origem* esteja definido como *merged_content*.⁠
* Altere o *nível de granularidade do Enriquecimento* para *Páginas (5000 pedaços de caracteres).*
* ⁠*Não selecione* Ativar enriquecimento incremental.
* ⁠Selecione os seguintes campos enriquecidos: ⁠

|habilidade cognitiva|
|———————|
|Parâmetro| 
|———————|
|Nome do campo| 
|———————|
| Extrair nomes de locais | |——————-| | Localizações |
|extraía frases-chaves| |————| |frases chaves| |————|
|detectar sentimento| |———————-| |sentimento|
|Gere tags a partir de imagens| |——————| |etiquetas de imagem| |————-| |Gere legendas a partir de imagens| |—————-| |imageCaption|


6️⃣Em *Salvar enriquecimentos em uma loja de conhecimento*, selecione:

* Projeções de imagem
* Documentos
* Páginas
* Frases-chave
* Entidades
* Detalhes da imagem
* Referências de imagens

7️⃣Selecione *projeções de blob do Azure: Documento.* Não mude o container. 

8️⃣ Selecione *Próximo: Personalize o índice de destino.* Altere  o *nome do Índice* para *coffee-index.*

9️⃣Certifique-se de que a Chave esteja definida para *tometadata_storage_path. O nome **LeaveSuggester* está em branco e o *modo de pesquisa é preenchido automaticamente*.

🔟Selecione *filtrável* para todos os campos que já estão selecionados por padrão. Selecione *Próximo: Crie um indexador.*

![filtrar](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/create-cognitive-search-solution/6a-azure-cognitive-search-customize-index.png)

1️⃣1️⃣ *Altere o nome* do Indexer para *coffee-indexer.*
Deixe o *Cronograma* definido como *Uma Vez.*

1️⃣2️⃣ Expanda as opções *Avançadas. Certifique-se de que a opção **Base-64 Encode Keys* esteja *selecionada*.

1️⃣3️⃣ Selecione *Enviar* para criar a fonte de dados, o conjunto de habilidades, o índice e o indexador.

1️⃣4️⃣ Retorne à sua página de recursos do *Azure AI Search.* No painel esquerdo, em *Gerenciamento de Pesquisa,* selecione *Indexadores. Selecione o **indexador de café* recém-criado. Aguarde um minuto e selecione *&orarr; Atualizar* até que o *Status indique sucesso.*

1️⃣5️⃣ Selecione o nome do indexador para ver mais detalhes. 
![indexar](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/create-cognitive-search-solution/6a-search-indexer-success.png)

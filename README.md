# Criação AI Cognitive Search: Primeiros passos

### Crie um recurso do Azure AI Search

<img src="https://adatis.co.uk/wp-content/uploads/CogSearchIcon-1.png" width=100px>

1. Entre no [portal do Azure](https://portal.azure.com/).

2. Clique no botão **+ Criar um recurso** , pesquise **Azure AI Search e crie um recurso Azure AI Search com as seguintes configurações:**

   * **Assinatura**: sua assinatura do Azure .
   * **Grupo de recursos** : selecione ou crie um grupo de recursos com um nome exclusivo .
   * **Nome do serviço** : um nome exclusivo .
   * **Localização** : Escolha qualquer região disponível.
   * **Nível de preços** : Básico.

3. Selecione **Review + create** e depois de ver a resposta **Validation Success** , selecione **Create** .
4. Após a conclusão da implantação, selecione **Ir para o recurso**. De uma olhadinha na página **Visão geral** do A zure AI Search, você pode adicionar índices, importar dados e pesquisar índices criados.
   
### Crie um recurso de serviços de IA do Azure

<img src="https://nightingalehq.ai/knowledgebase/glossary/what-are-azure-cognitive-services/cognitive-services_hud40d85c6e795b5b7851567b819b90865_77246_1200x675_fill_q75_box_smart1.jpg" width=150px>

Você precisará provisionar um recurso de **serviços de IA do Azure** que esteja no mesmo local que seu recurso do Azure AI Search. Sua solução de pesquisa usará esse recurso para enriquecer os dados no armazenamento de dados com insights gerados por IA.

1. Retorne à página inicial do portal do Azure. Clique no botão **＋ Criar um recurso** e pesquise os **serviços de IA do Azure** . Selecione **criar** um plano de **serviços de IA do Azure** . Para criar o recurso, configure-o com as seguintes informações:

   * **Assinatura** : sua assinatura do Azure .
   * **Grupo de recursos** : O mesmo grupo de recursos que seu recurso do Azure AI Search .
   * **Região** : o mesmo local do recurso do Azure AI Search .
   * **Nome** : Um nome exclusivo .
   * **Nível de preços**: Padrão S0
   * Ao marcar esta caixa, confirmo que li e compreendi todos os termos abaixo : Selecionado✅

2. Selecione **Revisar + criar** . Depois de ver a resposta **Validation Passed**, selecione **Create** .

## Crie uma conta de armazenamento
<img src="https://cdn-icons-png.flaticon.com/256/6780/6780849.png" width=100px>

1. Retorne à página inicial do portal do Azure e selecione o botão **+ Criar um recurso** .Procure conta de armazenamento e crie um recurso de **conta de armazenamento** com as seguintes configurações:
   
   * **Assinatura** : sua assinatura do Azure .
   * **Grupo de recursos** : O mesmo grupo de recursos que os recursos do Azure AI Search e dos serviços Azure AI .
   * **Nome da conta de armazenamento**: um nome exclusivo .
   * **Localização** : Escolha qualquer localização disponível .
   * Padrão **de desempenho**
   * **Redundância** : armazenamento localmente redundante (LRS)

2. Clique em **Revisar** e em **Criar** . Aguarde a conclusão da implantação e vá para o recurso implantado.
3. Na conta de Armazenamento do Azure que você criou, no painel de menu esquerdo, selecione **Configuração** (em **Configurações** ).
4. Altere a configuração de Permitir acesso anônimo de Blob para **Habilitado** e selecione **Salvar** .

### Carregar documentos para o armazenamento do Azure

1. No painel do menu esquerdo, selecione **Containers **.
2. Selecione **+ Contêiner**.
   
![containers]()
3. insira as seguintes configurações e clique em **Criar**:

   * **Nome** : Coffee-Reviews
   * **Nível de acesso público** : Container (acesso de leitura anônimo para containers e blobs)
   * **Avançado** : sem alterações .

4. Em uma nova guia do navegador, baixe as [avaliações de café compactadas](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html#upload-documents-to-azure-storage:~:text=Em%20uma%20nova,de%20avalia%C3%A7%C3%B5es%20.) em https://aka.ms/mslearn-coffee-reviewse extraia os arquivos para a pasta de avaliações .
5. No portal do Azure, selecione o contêiner de avaliações de café . No contêiner, selecione **Carregar(upload)**.
   
   ![upload-container](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/create-cognitive-search-solution/storage-blob-3.png)

6. No painel **Carregar blob** , selecione **Selecionar um arquivo**.
   
7. Na janela do Explorer, selecione **todos** os arquivos na pasta de avaliações , selecione **Abrir** e, em seguida, selecione **Carregar** .
   ![upload-blob](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/media/create-cognitive-search-solution/6a-azure-container-upload-files.png)

8. Depois que o upload for concluído, você poderá fechar o painel **Upload blob** . Seus documentos estão agora em seu contêiner de armazenamento de avaliações de café .

   

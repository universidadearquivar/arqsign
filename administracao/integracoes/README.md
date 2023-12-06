# 🧩 Integrações

A ArqSign conta com sua própria API de Integração. Isso quer dizer que clientes e parceiros podem integrar as funcionalidades da Plataforma ArqSign à suas soluções. A API de Integração permite a comunicação com outros aplicativos/softwares de forma automática, ou seja, sem o conhecimento ou intervenção do usuário final.

<figure><img src="../../.gitbook/assets/integracoes1.png" alt=""><figcaption><p>Clique na imagem para ampliar.</p></figcaption></figure>

***

## API Key – Chave de acesso

Para realizar a integração da plataforma a outras ferramentas via API é necessária uma Chave de Acesso, que o usuário pode obter clicando em “Gerar”. A chave gerada será apresentada no campo “API AppKey” e poderá ser utilizada para realizar a integração.

<figure><img src="../../.gitbook/assets/integracoes6.png" alt=""><figcaption><p>Clique na imagem para ampliar.</p></figcaption></figure>

{% hint style="danger" %}
<mark style="color:red;">**Sempre que clicar no botão “Gerar” será gerada uma nova chave de acesso e todas as integrações feitas utilizando a chave anterior serão desconfiguradas. Sugerimos cuidado ao criar chaves de acesso.**</mark>
{% endhint %}

***

## Serviços de Integração ArqSign

Ao clicar neste link, a aplicação irá abrir a página api.arqsign.com com os métodos disponíveis até o momento.

> [Clique aqui para acessar os Serviços de Integração da plataforma ArqSign.](https://api.arqsign.com/index.html)

<figure><img src="../../.gitbook/assets/integracoes2.png" alt=""><figcaption><p>Clique na imagem para ampliar.</p></figcaption></figure>

***

## Manual do Usuário e Treinamento

Ao clicar em “Manual do Usuário” o usuário terá acesso ao manual que apresenta todas as características e métodos de API disponíveis da plataforma ArqSign.

> [Clique aqui para ter acesso ao Manual com o Detalhamento Técnico da API de Integração da ArqSign.](https://arquivar.com.br/wp-content/uploads/2022/09/Manual-API-ArqSign.pdf)

<figure><img src="../../.gitbook/assets/integracoes3.png" alt=""><figcaption><p>Clique na imagem para ampliar.</p></figcaption></figure>

Ao clicar em “Treinamento – Integração ArqSign” o usuário terá acesso a um treinamento elaborado pela Universidade Arquivar que apresenta todas as possibilidades de utilização do API da plataforma ArqSign.

> [Clique aqui para ter acesso ao Treinamento Integração ArqSign.](https://cdn.arquivar.com.br/wp-content/uploads/articulate\_uploads/Curso-API-ArqSign/index.html?&\_ga=2.214775511.1134308362.1699443819-2052664689.1687871591#/)

<figure><img src="../../.gitbook/assets/integracoes4.png" alt=""><figcaption><p>Clique na imagem para ampliar.</p></figcaption></figure>

***

## Lista de ID's

Para realizar a integração via API são necessários alguns dados de ID’s, que podem ser obtidos clicando em “Lista de Id’s usuários” e “Lista de Id’s pastas”.

<figure><img src="../../.gitbook/assets/integracoes5.png" alt=""><figcaption><p>Clique na imagem para ampliar.</p></figcaption></figure>

**Lista de Id’s usuários:** Ao clicar neste link a aplicação irá fazer o download de um arquivo .csv com a lista de todos os usuários ativos na conta e seu respectivo ID.

**Lista de Id’s pastas:** Ao clicar neste link a aplicação irá fazer o download de um arquivo .csv com a lista de todas as pastas não excluídas da conta e seu respectivo ID.

***

## Funcionamento da API ArqSign

As funções fundamentais de uma API compreendem a obtenção, o envio, a alteração e a exclusão de informações. Isso ocorre quando um aplicativo de cliente ou parceiro envia uma solicitação ao aplicativo ArqSign, que por sua vez gera uma resposta.

Na plataforma ArqSign a integração por meio de API ocorre em três etapas:

1. A aplicação do cliente chama o método POST/api/v1/processo/enviar-documento-para-assinar para enviar um documento a ser assinado. Com a resposta de sucesso, a API retornará o ID do processo gerado e você deve guardá-lo para usar este ID como parâmetro nos outros métodos.
2. &#x20;A aplicação do cliente chama o método GET/api/v1/processo/{idProcesso}/status-do-processo para monitorar o status do processo gerado na Fase 01. Aconselhamos chamar este método no máximo 1x ao dia, não é necessário chamá-lo o tempo todo, uma vez que o status de um processo somente será concluído após a assinatura do documento por todos os signatários.
3. Assim que o processo estiver com o status “Concluído”, você pode passar para a fase 03, quando chamará o método GET/api/v1/processo/{idprocesso} para obter os dados completos do processo e o arquivo assinado.


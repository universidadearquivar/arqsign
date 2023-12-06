# 🟪 Fluxo ideal considerando alguns métodos disponíveis

As funções fundamentais de uma API compreendem a obtenção, o envio, a alteração e a exclusão de informações. Isso ocorre quando um aplicativo de cliente ou parceiro envia uma solicitação ao aplicativo ArqSign, que por sua vez gera uma resposta.

Na plataforma ArqSign a integração por meio de API ocorre em três etapas:

1. A aplicação do cliente chama o método POST/api/v1/processo/enviar-documento-para-assinar para enviar um documento a ser assinado. Com a resposta de sucesso, a API retornará o ID do processo gerado e você deve guardá-lo para usar este ID como parâmetro nos outros métodos.
2. &#x20;A aplicação do cliente chama o método GET/api/v1/processo/{idProcesso}/status-do-processo para monitorar o status do processo gerado na Fase 01. Aconselhamos chamar este método no máximo 1x ao dia, não é necessário chamá-lo o tempo todo, uma vez que o status de um processo somente será concluído após a assinatura do documento por todos os signatários.
3. Assim que o processo estiver com o status “Concluído”, você pode passar para a fase 03, quando chamará o método GET/api/v1/processo/{idprocesso} para obter os dados completos do processo e o arquivo assinado.

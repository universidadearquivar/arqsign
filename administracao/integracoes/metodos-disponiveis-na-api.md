# 🟪 Métodos disponíveis na API

Todos os métodos que retornam campos de data e hora na API estão no fuso horário UTC+0.

Os métodos de API liberados para uso na plataforma são:

<details>

<summary>POST/api/v1/processo/enviar-documento-para-assinar</summary>

O objetivo deste método é permitir que o usuário envie um documento para ser assinado via plataforma ArqSIGN.

Para mais informações, acesse a página [Detalhes dos métodos](detalhes-dos-metodos/).

</details>

<details>

<summary>GET/api/v1/processo/{idprocesso}</summary>

O objetivo deste método é permitir que o usuário busque os dados completos de um processo, incluindo o documento e o registro de assinatura, caso já exista alguma assinatura no documento.

Para evitar que o método retorne documentos ainda não assinados ou em processo de assinatura, utilize o método de buscar o status do processo para checar se o processo em questão se encontra com o status “Concluído”.

Neste método o usuário irá nos enviar o ID do Processo, e nós retornaremos um JSON completo com as informações do processo.

Para mais informações, acesse a página [Detalhes dos métodos](detalhes-dos-metodos/).

</details>

<details>

<summary>GET/api/v1/processo/{idProcesso}/status-do-processo</summary>

O objetivo deste método é permitir que o usuário busque o status de um processo de assinatura, para que evite buscar o processo como um todo pelo método “GET/api/v1/processo/{idprocesso}” antes que este esteja com status “Concluído”.

Neste método o usuário irá nos enviar o ID do Processo, e nós retornaremos um JSON com o nome e status atual do mesmo.

Para mais informações, acesse a página [Detalhes dos métodos](detalhes-dos-metodos/).

</details>

<details>

<summary>GET/api/v1/processo/{idprocesso}/dados-signatarios</summary>

O objetivo deste método é permitir que o usuário busque os dados dos signatários que possuem ação de assinar eletronicamente em um processo de assinatura.

Neste método o usuário irá nos enviar o ID do Processo, e nós retornaremos um JSON completo com as informações do processo e dos signatários.

</details>

<details>

<summary>PATCH/api/v1/processo/{idProcesso}/reenviar-processo</summary>

O objetivo deste método é permitir que o usuário reenvie o processo para os destinatários pendentes de assinaturas na ordem atual.&#x20;

O usuário poderá informar para qual destinatário pendente de assinatura deseja reenviar o documento. Caso não informe os destinatários, o serviço reenvia o processo para todos os destinatários participantes do processo com ação de assinar eletronicamente e que estejam pendentes de assinaturas na ordem atual.

Além disso, o usuário poderá editar os destinatários pendentes de assinatura para os quais deseja reenviar o processo.

Neste método o usuário irá nos enviar o ID do Processo, e nós reenviaremos para os destinatários pendentes de assinatura na ordem de assinatura atual, conforme dados informados no JSON.

</details>

<details>

<summary>PATCH/api/v1/processo/{idProcesso}/cancelar-processo</summary>

O objetivo deste método é permitir que o usuário cancele o processo de assinatura que esteja em andamento.

Neste método o usuário irá nos enviar o ID do Processo, e nós cancelaremos o processo informado.

</details>

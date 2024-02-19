# 🟪 Histórico de alterações da API

## 2022

<details>

<summary>1.3.0 - 04/01/2022</summary>

Incluímos mais validações de segurança na API que o e-commerce chama no ArqSign.

</details>

<details>

<summary>1.6.4 - 03/06/2022</summary>

Ajuste na API de Compra: No recebimento dos dados de compra, vindos do e-commerce, quando o país era diferente do Brasil, o sistema obrigava que Tipo Pessoa, CPF/CNPJ e CEP fossem informados. Após o ajuste, estes dados não são mais obrigatórios quando país for diferente do Brasil.

</details>

<details>

<summary>1.8.1 - 16/11/2022</summary>

API > Enviar documento: Sistema permitia envia documento o mesmo e-mail na mesma ordem de assinatura.

</details>

***

## 2023

<details>

<summary>1.9.3 - 23/02/2023</summary>

API para enviar documento para assinar: não estava sendo validado a forma de envio para salvar o contato do signatário.

</details>

<details>

<summary>1.9.4 - 14/03/2023</summary>

Assinar documento: Correção no loop gerado durante a assinatura, com Certificado Digital, de um documento enviado via API.

</details>

<details>

<summary>1.9.7 - 30/03/2023</summary>

\[API] Enviar documento para assinar: Aplicação não valida quando são enviados parâmetros para posição automática e manual para representação visual, retornando status 200.

Assinar documento: Ao assinar um documento pelo Whatsapp, que foi enviado pela API, o sistema plota informação incorreta juntamente com a representação visual, apresentando o número de telefone do signatário no campo e-mail.

Assinar documento: Ao assinar um documento com assinatura eletrônica, que foi enviado pela API, o sistema não plota informação do certificado vinculado a assinatura.

</details>

<details>

<summary>1.9.8 - 04/04/2023</summary>

Correção das descrições dos serviços API.

</details>

<details>

<summary>1.11.1 - 02/05/2023</summary>

API > Enviar documento para assinar: Sistema enviava documento pela API quando não existe representação visual do tipo PJ e existe configuração de Razão Social e Documento PJ como obrigatório.&#x20;

API > Enviar documento para assinar: Sistema validava posição de assinatura para destinatário com ação de receber uma cópia.&#x20;

API > Enviar documento para assinar: Sistema gerava marcação para assinatura na página automática para destinatário com ação de receber uma cópia.

</details>

<details>

<summary>1.12.2 - 25/05/2023</summary>

API: Sistema não aplica representação visual no documento para destinatários que deveriam ter representação em página automática.

</details>

<details>

<summary>1.12.3 - 26/05/2023</summary>

API > Enviar Documento para Assinar: Sistema não enviava o documento com definição e página automática.

</details>

<details>

<summary>1.13.0 - 27/06/2023</summary>

Integrações : Incluídos os links do manual e de treinamento da API ArqSign.

</details>

<details>

<summary>1.13.3 - 02/08/2023</summary>

API > Notificação: Aplicação estava apresentando o nome da conta no lugar do nome do documento, na notificação enviada para assinatura do documento.

</details>

<details>

<summary>1.13.4 - 18/08/2023</summary>

API ArqSign > Dados do Processo: Sistema apresentava informação de recusa da assinatura para todos os signatários. O correto é apresentar a informação nos dados do signatário quem recusou a assinatura do documento.

</details>

<details>

<summary>1.13.5 - 19/09/2023</summary>

O sistema exibia a senha do certificado no payload do endpoint api/v1/certificados/validar-certificado-selecionado.

</details>

<details>

<summary>1.14.0 - 03/10/2023</summary>

API > Enviar Documento para Assinar: Sistema não desconsiderava posição manual quando informado valor no parâmetro de página automática.

</details>

<details>

<summary>1.15.2 - 02/11/2023</summary>

API e-commerce - Comprar Créditos: Ajustado o serviço e comprar créditos (/api/v1/compras/comprar-creditos) para receber os dados fiscais e endereço da conta.

</details>

<details>

<summary>1.15.3 - 13/11/2023</summary>

API > Validar Email CTG: Sistema retornava erro 404 para alguns domínios.

</details>

<details>

<summary>1.15.6 - 13/12/2023</summary>

Na tela do menu Integrações da Plataforma ArqSign:

1. Removido o link: Treinamento
2. Alterado a palavra "Manual do Usuário" para "Documentação API"
3. Alterado o link de "Documentação API" para o link: https://arquivar.gitbook.io/manual-arqsign/administracao/integracoes.

</details>

***

## 2024

<details>

<summary>1.17.0 - 07/02/2024</summary>

Assinar Documento: Sistema apresentava erro ao tentar assinar documento que foi enviado pela API.

O sistema plotava a representação visual em posicionamento incorreta em documentos enviados pela API com posição manual.&#x20;

</details>


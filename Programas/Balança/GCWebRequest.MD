# GCWebRequest - configuração da balança

O GCWebRequest faz a comunicação entre a balança conectada ao computador e o GCWeb. Este guia reúne o download, a instalação, os testes e a validação usados nas franquias Maria Pitanga.

## Download

Instalador mais recente:

- https://cdn.gcweb.app.br/p/out/GCWebRequest_Setup.exe

Baixe o instalador diretamente no computador conectado à balança.

## Materiais disponíveis neste repositório

- `Aplicativos de Teste/Conexão Balança Teste.exe`: teste principal da porta COM e da leitura.
- `Aplicativos de Teste/Linguagem Balança - AppTest.jar`: teste alternativo; requer Java.
- `Drivers/ADAPTADOR SERIAL-USB Hl-340.exe`: driver para adaptadores compatíveis com HL-340.
- `../../Documentação/Documentação GCWebRequest - Balança.docx`: manual ilustrado.
- `../../Vídeos/Instalação Maria Pitanga_v1.0.mp4`: vídeo da instalação.

## Configuração padrão Maria Pitanga

| Configuração | Valor inicial |
| --- | --- |
| Modelo | `TOLEDO PRIX 3` |
| Baud rate | `4800` |
| Porta | COM identificada no Windows, frequentemente `COM3` |

Confirme os parâmetros técnicos se o equipamento da unidade for diferente.

## Pré-requisitos

- Permissão para instalar programas e configurar tarefas agendadas.
- Balança ligada e conectada.
- Cabo serial ou adaptador USB reconhecido pelo Windows.
- Acesso à tela 19200 do GCWeb.
- Java quando a ferramenta `.jar` ou uma versão antiga do GCWebRequest exigir.

## 1. Identificar a porta COM

1. Abra o **Gerenciador de Dispositivos**.
2. Expanda **Portas (COM e LPT)**.
3. Localize a balança ou o adaptador serial USB.
4. Anote a porta apresentada, por exemplo `COM3`.

Se nenhuma porta aparecer, reconecte o adaptador, teste outra USB e confira dispositivos com alerta amarelo. Instale `Drivers/ADAPTADOR SERIAL-USB Hl-340.exe` somente se o adaptador for compatível.

## 2. Instalar o GCWebRequest

1. Baixe o instalador pelo link deste documento.
2. Execute `GCWebRequest_Setup.exe` como administrador.
3. Conclua as etapas do instalador.

A versão mais recente deve instalar o Java necessário e criar a tarefa do GCWebRequest no Agendador de Tarefas. Confira esses itens antes de configurá-los manualmente.

## 3. Configurar a tarefa agendada, se necessário

Esta etapa se aplica a versões antigas ou quando a instalação automática não criar a tarefa.

1. Abra o **Agendador de Tarefas**.
2. Acesse **Biblioteca do Agendador de Tarefas > Microsoft**.
3. Selecione **Importar Tarefa**.
4. Procure o XML em `C:\Program Files\GCWeb\GCWebRequest`.
5. Em **Alterar Usuário ou Grupo**, informe o usuário que utiliza o Windows.
6. Clique em **Verificar Nomes**, confirme e salve a tarefa.
7. Não execute a tarefa antes do teste da balança.

## 4. Testar a balança

1. Feche o GCWebRequest e outros programas que possam usar a porta serial.
2. Execute `Aplicativos de Teste/Conexão Balança Teste.exe`.
3. Configure a balança **Toledo**, a porta COM identificada e baud rate `4800`.
4. Clique em **Ativar**.
5. Coloque um item sobre a balança e clique em **Ler Peso**.
6. Compare o resultado com o visor da balança.
7. Clique em **Desativar** e feche o aplicativo.

Se precisar de um segundo diagnóstico, execute `Linguagem Balança - AppTest.jar`.

> Apenas um programa pode usar a porta COM por vez. Feche a ferramenta de teste antes de iniciar o GCWebRequest.

## 5. Executar e atualizar

1. No Agendador de Tarefas, localize a tarefa do GCWebRequest.
2. Clique com o botão direito e selecione **Executar**.
3. Autorize a execução se o Windows solicitar.
4. Confirme o ícone do GCWebRequest próximo ao relógio.
5. Clique com o botão direito no ícone e selecione **Verificar Atualização**.
6. Aguarde a conclusão.

## 6. Configurar o aplicativo

1. Abra as configurações pelo ícone do GCWebRequest.
2. Informe a porta COM identificada.
3. Defina baud rate `4800`.
4. Selecione `TOLEDO PRIX 3`.
5. Clique em **Salvar Configurações**.
6. Clique em **Recarregar Aplicação**.

## 7. Validar no GCWeb

1. Confirme que o GCWebRequest continua em execução.
2. Abra a tela 19200.
3. Acesse o fluxo que consulta o peso.
4. Coloque um produto sobre a balança.
5. Compare o peso do GCWeb com o visor.
6. Reinicie o computador e repita o teste.

A instalação está concluída quando a ferramenta de teste e a tela 19200 leem o peso corretamente, e o GCWebRequest inicia novamente com o Windows.

## Solução de problemas

### A porta COM não aparece

- Confira cabo, alimentação e conexão USB.
- Teste outra porta USB.
- Procure alertas no Gerenciador de Dispositivos.
- Instale o driver HL-340 apenas em adaptador compatível.

### A porta aparece, mas o teste não lê

- Confirme a COM, o baud rate `4800` e o modelo.
- Feche o GCWebRequest e outros programas antes do teste.
- Desative a conexão no aplicativo antes de fechá-lo.
- Reinicie a balança e repita.

### O teste funciona, mas a tela 19200 não

- Feche a ferramenta de teste para liberar a porta.
- Confirme o GCWebRequest na área de notificação.
- Revise porta, baud rate e modelo.
- Salve e use **Recarregar Aplicação**.
- Verifique atualizações e reinicie a tarefa agendada.

### O GCWebRequest não inicia com o Windows

- Confirme se a tarefa existe e está habilitada.
- Confira o usuário associado à tarefa.
- Revise o caminho em `C:\Program Files\GCWeb\GCWebRequest`.
- Execute a tarefa manualmente e registre qualquer erro.

### O peso está instável ou incorreto

- Nivele a balança e retire objetos encostados no prato.
- Aguarde o visor estabilizar.
- Verifique cabos, conectores e adaptadores.
- Compare a ferramenta de teste com o visor.

## Informações para o atendimento

Em caso de falha, registre:

- unidade da franquia;
- versão do Windows;
- modelo da balança;
- cabo ou adaptador utilizado;
- porta COM e baud rate;
- resultado da ferramenta de teste;
- resultado na tela 19200;
- mensagem de erro e horário.

Não inclua senhas, certificados ou dados pessoais nas evidências.

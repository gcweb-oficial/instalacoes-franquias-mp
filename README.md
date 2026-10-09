# Instalações das franquias Maria Pitanga

<img src="Documentação/assets/logo-gcweb.png" alt="Logotipo do GCWeb" width="180">

Este repositório centraliza os materiais usados na preparação e validação das instalações do GCWeb nas franquias Maria Pitanga. Ele reúne programas auxiliares, drivers, ferramentas de teste, manuais ilustrados e um vídeo de apoio para configurar a impressão e a leitura da balança no PDV.

> Este material apoia a instalação, mas não substitui a conferência dos equipamentos, dos dados da unidade e das permissões do Windows.

## Comece pelo guia de implantação

O documento principal para conduzir uma nova implantação é:

**[Abrir o Guia Operacional de Implantação da Franquia](Documentação/GUIA_IMPLANTACAO_FRANQUIA.md)**

Use o guia como roteiro da implantação. Ele organiza a sequência de preparação e configuração da franquia no GCWeb, incluindo cadastro do estabelecimento e grupo, delivery, parâmetros fiscais e demais etapas operacionais.

Os outros arquivos deste repositório complementam o guia com:

- manuais ilustrados para impressora e balança;
- programas, bibliotecas e drivers necessários;
- ferramentas para testar a comunicação com os equipamentos;
- vídeo de apoio para acompanhar a instalação.

## O que há no repositório

### `Documentação/`

- `GUIA_IMPLANTACAO_FRANQUIA.md`: roteiro principal da implantação e ponto de partida para quem executará a configuração da unidade.
- `CHECKLIST_IMPLANTACAO_FRANQUIA.md`: marcadores resumidos para categorizar e acompanhar todas as configurações da implantação.
- `Documentação GCWebPrinter - Impressora.docx`: instalação do certificado, inicialização automática, seleção da impressora, configuração do arquivo `hosts` e validação do serviço.
- `Documentação GCWebRequest - Balança.docx`: identificação da porta COM, instalação do GCWebRequest, teste da balança e validação no GCWeb.

### `Programas/GCWebPrinter - Maria Pitanga/`

Pacote do GCWebPrinter usado na comunicação entre o GCWeb e a impressora da franquia. Contém o executável principal, bibliotecas, certificados e arquivos de configuração.

Copie e mantenha todo o conteúdo da pasta em conjunto. O `GCWebPrinter.exe` depende dos demais arquivos do diretório. O `GCWebPrinter_old.exe` deve ser usado somente como contingência e com orientação do suporte.

### `Programas/Balança/`

- `GCWebRequest.MD`: guia operacional de download, instalação, testes e solução de problemas.
- `Aplicativos de Teste/Conexão Balança Teste.exe`: valida a porta COM e a leitura do peso.
- `Aplicativos de Teste/Linguagem Balança - AppTest.jar`: teste alternativo que depende do Java.
- `Drivers/ADAPTADOR SERIAL-USB Hl-340.exe`: driver para adaptadores compatíveis com HL-340.

Instale o driver HL-340 somente quando o adaptador for compatível e o Windows não reconhecer corretamente a porta serial.

### `Vídeos/`

- `Instalação Maria Pitanga_v1.0.mp4`: demonstração em vídeo do processo de instalação.

### `LICENSE`

Termos de licença e uso do conteúdo deste repositório.

## Ordem recomendada para a instalação

Use o `GUIA_IMPLANTACAO_FRANQUIA.md` como checklist principal. Para a parte local de equipamentos e aplicativos, siga esta ordem:

1. Confirmar computador, impressora, balança, cabos e adaptadores da unidade.
2. Assistir ao vídeo para conhecer o fluxo completo.
3. Configurar o GCWebPrinter conforme o manual da impressora.
4. Acessar `https://www.gcwebmfe.com:8080` e confirmar a mensagem `DataSnapServer`.
5. Identificar a porta COM da balança no Gerenciador de Dispositivos.
6. Instalar e configurar o GCWebRequest conforme o guia da balança.
7. Testar a leitura com uma ferramenta de `Programas/Balança/Aplicativos de Teste/`.
8. Validar a impressão e a leitura do peso na tela 19200 do GCWeb.
9. Reiniciar o computador e confirmar a inicialização automática dos aplicativos.

## Checklist antes de começar

- Acesso de administrador ao Windows.
- Acesso ao GCWeb e à tela 19200.
- Impressora instalada e visível no Windows.
- Balança ligada, nivelada e conectada.
- Porta COM identificada.
- Cabo ou adaptador serial USB reconhecido.
- Java instalado quando a ferramenta `.jar` ou uma versão antiga do GCWebRequest exigir.
- Navegador disponível para testar o GCWebPrinter.

## Critérios de conclusão

A instalação somente deve ser considerada concluída quando:

- o GCWebPrinter iniciar sem erro;
- o endereço local exibir `DataSnapServer`;
- uma impressão real for concluída na impressora correta;
- a ferramenta de teste conseguir ler o peso;
- o GCWebRequest permanecer em execução;
- a tela 19200 receber o peso corretamente;
- ambos os aplicativos voltarem a funcionar após reiniciar o Windows.

## Cuidados importantes

- Faça backup antes de alterar `GCWebPrinter.ini`, `Configuracao.xml` ou outro arquivo de configuração.
- Não publique nem envie separadamente arquivos `.key`, `.pem`, `.crt` ou `.der`; trate-os como arquivos sensíveis do pacote.
- Não substitua o executável atual pelo `GCWebPrinter_old.exe` sem orientação.
- O nome da impressora e a porta COM podem variar entre computadores.
- Certificados, drivers, arquivo `hosts` e tarefas agendadas normalmente exigem permissão de administrador.
- Ao trocar a balança de porta USB, identifique novamente a COM e repita o teste.

## Solução rápida de problemas

### O GCWebPrinter não responde

- Confirme se o aplicativo está aberto ou minimizado.
- Confira o certificado em **Autoridades de Certificação Raiz Confiáveis**.
- Revise a entrada `127.0.0.1 www.gcwebmfe.com` no arquivo `hosts`.
- Verifique bloqueios de firewall ou antivírus na porta `8080`.
- Teste novamente `https://www.gcwebmfe.com:8080`.

### A balança não retorna peso

- Confirme a porta COM no Gerenciador de Dispositivos.
- Feche outros programas que estejam usando a porta.
- Confira o padrão inicial: baud rate `4800` e modelo `TOLEDO PRIX 3`.
- Teste a balança fora do GCWeb antes de validar a tela 19200.
- Consulte `Programas/Balança/GCWebRequest.MD`.

## Manutenção do repositório

Ao adicionar uma nova versão:

1. Preserve a versão anterior até concluir a validação.
2. Identifique claramente a versão e a finalidade.
3. Atualize este README e o guia relacionado.
4. Não inclua arquivos temporários nem configurações particulares de uma franquia.
5. Valide o fluxo em ambiente controlado antes de disponibilizá-lo.

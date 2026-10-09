# Checklist de implantação de franquia

Checklist resumido para acompanhar a implantação de uma franquia Maria Pitanga no GCWeb.

**Referência detalhada:** [Guia Operacional de Implantação](GUIA_IMPLANTACAO_FRANQUIA.md)  
**Atualização:** outubro de 2026

> Os itens identificados como **condicionais** devem ser marcados como concluídos ou não aplicáveis.

## 1. Abertura e controle

- [ ] Primeiro contato — Jamile
- [ ] Responsável da franquia definido
- [ ] Responsável GCWeb definido
- [ ] Data de implantação definida
- [ ] Franquia registrada na Planilha de Implantação
- [ ] Estabelecimento registrado na planilha
- [ ] CNPJ registrado na planilha
- [ ] Nome do contato registrado na planilha
- [ ] E-mail do responsável registrado na planilha
- [ ] Telefone do responsável registrado na planilha
- [ ] Data da implantação registrada na planilha
- [ ] Número de TEF registrado na planilha
- [ ] Recursos contratados confirmados
- [ ] Pendências iniciais identificadas
- [ ] Evidências da implantação organizadas

## 2. Dados e documentos

- [ ] CNPJ
- [ ] Razão social
- [ ] Nome fantasia
- [ ] Endereço
- [ ] Telefone e celular
- [ ] Contato responsável
- [ ] Inscrição estadual
- [ ] Inscrição municipal
- [ ] Regime tributário
- [ ] Dados fiscais
- [ ] Certificado PFX
- [ ] Senha do certificado
- [ ] Série da NFC-e
- [ ] CSC
- [ ] ID do CSC
- [ ] Usuários solicitados
- [ ] Recursos de delivery confirmados
- [ ] Recursos de TEF confirmados
- [ ] Recursos de Pix confirmados
- [ ] Recursos de fidelidade confirmados
- [ ] Integração com Ordem de Compra confirmada

## 3. Cliente da franquia — tela 12360

- [ ] Cliente da franquia cadastrado
- [ ] Dados cadastrais conferidos
- [ ] Dados fiscais conferidos
- [ ] Grupo de cliente definido
- [ ] Grupo MP aplicado
- [ ] Grupo Internacional aplicado, quando necessário
- [ ] Código do cliente registrado

## 4. Estabelecimento e grupo — telas 11630 e 11635

- [ ] Estabelecimento consultado pelo CNPJ
- [ ] Dados do estabelecimento conferidos
- [ ] Padrão de nome fantasia aplicado
- [ ] Grupo de estabelecimento criado
- [ ] Estabelecimento vinculado ao grupo
- [ ] Usuário responsável vinculado
- [ ] Tabela de preço criada
- [ ] Famílias criadas
- [ ] PDV criado
- [ ] Caixa criado
- [ ] Caixa/banco criado
- [ ] Cadastros automáticos conferidos

## 5. Vínculo entre cliente e estabelecimento

- [ ] Parâmetro de sistema localizado
- [ ] Tabela `TBESTABELECIMENTO`
- [ ] Campo `VINCULO_ESTB_CLIENTE`
- [ ] Cliente vinculado ao estabelecimento
- [ ] Grupo de cliente conferido
- [ ] Grupo de estabelecimento conferido
- [ ] Vínculo validado para Ordem de Compra

## 6. Usuários e perspectiva

- [ ] Tales vinculado
- [ ] Deivid vinculado
- [ ] João Batista vinculado
- [ ] Simoneide vinculada
- [ ] Hilgner vinculado
- [ ] Jamile vinculada
- [ ] GCWeb vinculado
- [ ] Alves vinculado
- [ ] Permissões dos usuários conferidas
- [ ] Mudança por Perspectiva validada — tela 19200
- [ ] Franquia visível para os usuários autorizados

## 7. PDV — tela 19020

- [ ] Série configurada
- [ ] Documentos padrão configurados
- [ ] Descontos por operador configurados
- [ ] Classificação de sangria configurada
- [ ] Classificação de suprimento configurada
- [ ] Combos copiados de PDV compatível
- [ ] Combos copiados revisados
- [ ] Perfil do PDV conferido
- [ ] Perfil Interestadual aplicado para loja fora do Ceará
- [ ] Habilitação de Ordem de Compra configurada

## 8. Formas de pagamento e TEF

- [ ] Dinheiro
- [ ] Crédito
- [ ] Débito
- [ ] Pix
- [ ] Fidelidade
- [ ] Vale Colaborador
- [ ] Vouchers
- [ ] Cartão Voucher
- [ ] iFood
- [ ] 99Food
- [ ] CRÉDITO TEF ELGIN vinculado — condicional
- [ ] DÉBITO TEF ELGIN vinculado — condicional
- [ ] Credenciamento TEF aberto — condicional
- [ ] Quantidade de terminais TEF conferida — condicional
- [ ] Transação TEF testada — condicional
- [ ] Pagamento Pix testado — condicional

## 9. Pedidos e Ordem de Compra

- [ ] Integração de pedidos habilitada
- [ ] Integração com Ordem de Compra habilitada
- [ ] Cliente da tela 12360 conferido
- [ ] `VINCULO_ESTB_CLIENTE` conferido
- [ ] Perfil Interestadual conferido, quando aplicável
- [ ] Pedido de teste integrado
- [ ] Ordem de Compra de teste gerada
- [ ] Cliente correto vinculado à OC
- [ ] Itens e valores da OC conferidos
- [ ] Resultado do teste registrado

## 10. Delivery — condicional

- [ ] Delivery contratado
- [ ] Modelo de taxa definido
- [ ] Taxa por bairro configurada
- [ ] Taxa por quilometragem configurada
- [ ] Faixas e valores configurados
- [ ] Bairros cadastrados — tela 21120
- [ ] Banner configurado
- [ ] Imagem de fundo configurada
- [ ] Cores configuradas
- [ ] Horários configurados
- [ ] Latitude configurada
- [ ] Longitude configurada
- [ ] Produtos do delivery definidos
- [ ] Complementos definidos
- [ ] Dados publicados conferidos
- [ ] Pedido de delivery testado

## 11. Certificado e NFC-e — tela 21460

- [ ] Certificado PFX cadastrado
- [ ] Senha do PFX validada
- [ ] Modelo 65 configurado
- [ ] Série da NFC-e validada
- [ ] CSC configurado
- [ ] ID do CSC configurado
- [ ] Generator ajustado
- [ ] Última numeração fiscal conferida
- [ ] Emissão de NFC-e testada
- [ ] NFC-e autorizada
- [ ] DANFCE conferido
- [ ] Contingência fiscal conferida
- [ ] Resultado fiscal registrado

## 12. Fidelidade — tela 12620 — condicional

- [ ] Fidelidade contratada
- [ ] Plano de fidelidade criado
- [ ] Conversão configurada
- [ ] Validade configurada
- [ ] Regra de pontuação configurada
- [ ] Regras de resgate configuradas
- [ ] Estabelecimento vinculado
- [ ] Acúmulo de pontos testado
- [ ] Resgate de pontos testado

## 13. Produtos e preços iniciais

- [ ] Produtos iniciais entregues pela equipe GCWeb
- [ ] Produtos existentes conferidos
- [ ] Produtos vinculados ao estabelecimento
- [ ] Aba Estabelecimentos (Venda) conferida — tela 27150
- [ ] Tabela de preço vinculada
- [ ] Preços iniciais conferidos
- [ ] Canais de venda conferidos
- [ ] Complementos conferidos
- [ ] Taras conferidas
- [ ] Sem Tara aplicado, quando necessário
- [ ] Produto de teste vendido

## 14. Tributação — tela 27080

- [ ] Famílias comercializadas identificadas
- [ ] Dados Contábeis/Fiscais acessados
- [ ] Regra tributária copiada ou cadastrada
- [ ] Regra vinculada ao estabelecimento
- [ ] Operação fiscal validada
- [ ] CFOP validado
- [ ] CST de ICMS validado
- [ ] CST de PIS/COFINS validado
- [ ] CST de IPI validado
- [ ] Regras conferidas com a contabilidade
- [ ] Tributação do produto de teste validada

## 15. Colaboradores — tela 19200

- [ ] Colaboradores cadastrados
- [ ] Cargos cadastrados
- [ ] Administrador definido
- [ ] Usuário vinculado
- [ ] Cliente vinculado
- [ ] Colaborador vinculado
- [ ] Perspectiva vinculada
- [ ] Permissões conferidas
- [ ] Acesso do administrador testado
- [ ] Acesso dos operadores testado

## 16. GCWebPrinter e impressora

- [ ] Pasta completa do GCWebPrinter copiada
- [ ] Certificado do GCWebPrinter instalado
- [ ] Certificado em Autoridades de Certificação Raiz Confiáveis
- [ ] Entrada do arquivo `hosts` configurada
- [ ] `127.0.0.1 www.gcwebmfe.com`
- [ ] Impressora instalada no Windows
- [ ] Impressora selecionada no GCWebPrinter
- [ ] GCWebPrinter configurado para iniciar com o Windows
- [ ] GCWebPrinter aberto ou minimizado
- [ ] `https://www.gcwebmfe.com:8080` acessado
- [ ] Resposta `DataSnapServer` confirmada
- [ ] Impressão de teste realizada
- [ ] Impressão pela tela 19200 validada

## 17. GCWebRequest e balança — condicional

- [ ] Balança ligada e nivelada
- [ ] Cabo ou adaptador reconhecido
- [ ] Driver HL-340 instalado, quando compatível
- [ ] Porta COM identificada
- [ ] Baud rate `4800`
- [ ] Modelo `TOLEDO PRIX 3`
- [ ] Java instalado, quando necessário
- [ ] GCWebRequest instalado
- [ ] Tarefa agendada criada
- [ ] Usuário da tarefa conferido
- [ ] GCWebRequest atualizado
- [ ] Porta configurada no GCWebRequest
- [ ] Modelo configurado no GCWebRequest
- [ ] Aplicação recarregada
- [ ] Leitura no aplicativo de teste validada
- [ ] Porta COM liberada após o teste
- [ ] Peso validado na tela 19200
- [ ] Inicialização após reiniciar o Windows validada

## 18. Treinamento e validação operacional

- [ ] Abertura de caixa testada
- [ ] Venda de produto testada
- [ ] Formas de pagamento testadas
- [ ] Impressão testada
- [ ] Leitura da balança testada — condicional
- [ ] Emissão fiscal testada
- [ ] Cancelamento testado
- [ ] Sangria testada
- [ ] Suprimento testado
- [ ] Delivery testado — condicional
- [ ] Fidelidade testada — condicional
- [ ] Pedido integrado testado
- [ ] Ordem de Compra testada
- [ ] Treinamento do administrador concluído
- [ ] Treinamento dos operadores concluído
- [ ] Dúvidas da franquia registradas

## 19. Aceite e entrega

- [ ] Cadastros revisados
- [ ] Recursos contratados validados
- [ ] Testes operacionais concluídos
- [ ] Teste fiscal autorizado
- [ ] Pendências resolvidas
- [ ] Pendências remanescentes formalizadas
- [ ] Responsáveis pelas pendências definidos
- [ ] Data efetiva atualizada na Planilha de Implantação
- [ ] Evidências organizadas
- [ ] Responsável pela validação registrado
- [ ] Aceite da franquia obtido
- [ ] Implantação concluída

## 20. Pós-implantação — Igor Dev

- [ ] Solicitação de produto recebida
- [ ] Produto pesquisado no cadastro central
- [ ] Duplicidade descartada
- [ ] Novo produto criado, quando necessário
- [ ] Produto vinculado ao estabelecimento — tela 27150
- [ ] Preço atualizado
- [ ] Canal de venda atualizado
- [ ] Complementos atualizados
- [ ] Tara atualizada
- [ ] Alteração validada
- [ ] Atendimento registrado

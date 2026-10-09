<img src="assets/logo-gcweb.png" alt="Logotipo do GCWeb" width="180">

# Guia operacional de implantação de franquia

Passo a passo para preparar, configurar, validar e entregar uma franquia Maria Pitanga no GCWeb.

**Projeto:** GCWeb | Maria Pitanga  
**Atualização:** setembro de 2026

## Como utilizar este guia

Execute as etapas na ordem apresentada. Utilize os pontos de controle e o checklist final deste guia para acompanhar as configurações e validações.

A **Planilha de Implantação** possui uma finalidade específica: registrar, de forma resumida, quais franquias estão sendo implantadas. Ela não substitui o checklist operacional nem o registro detalhado de pendências e evidências.

Antes de avançar para a etapa seguinte:

1. confirme a conclusão das atividades;
2. identifique eventuais pendências e seus responsáveis;
3. registre as evidências da validação no controle operacional adotado pela equipe.

## Responsáveis principais

| Atividade | Responsável |
| --- | --- |
| Primeiro contato da implantação | Jamile |
| Manutenção de produtos e preços após implantação/treinamento | Igor Dev |
| Demais configurações e validações | Equipe responsável pela implantação |

# 1. Iniciar a implantação

## Primeiro contato

Jamile realiza o primeiro contato da implantação com a franquia para alinhar o processo, os responsáveis e a entrega das informações necessárias.

## Registrar a franquia na Planilha de Implantação

Acesse a [Planilha de Implantação das Franquias](https://docs.google.com/spreadsheets/d/1J9dRvZFcnoKSOyeDCtEcSKidP_HquddA/edit?gid=1391387779#gid=1391387779) e inclua a unidade que está entrando em implantação.

A planilha é utilizada somente como registro das franquias em implantação. Preencha os seguintes campos:

| Campo | Informação esperada |
| --- | --- |
| Estabelecimento | Identificação da unidade |
| CNPJ | CNPJ da franquia |
| Nome do Contato | Pessoa de contato da unidade |
| E-mail do Responsável | E-mail para contato |
| Telefone do Responsável | Telefone para contato |
| Dt.Implantação | Data prevista ou realizada da implantação |
| Número de TEF | Quantidade de terminais TEF da unidade |

Além desse registro resumido:

- reunir CNPJ, razão social, nome fantasia, endereço, contatos, inscrições e regime tributário;
- confirmar os recursos contratados: delivery, NFC-e, TEF, Pix, fidelidade e integração de pedidos com Ordem de Compra;
- solicitar certificado PFX e senha, dados fiscais, usuários e responsáveis;
- controlar informações ausentes, pendências e evidências fora dessa planilha, conforme o processo interno da equipe.

**Ponto de controle:** confirmar que a franquia foi incluída na planilha e que os dados mínimos para iniciar os cadastros estão disponíveis.

# 2. Cadastrar o cliente da franquia

## Tela 12360 - Cadastro de Clientes

Antes de vincular a franquia ao estabelecimento, é necessário cadastrá-la como cliente:

1. Acessar a tela 12360.
2. Cadastrar o cliente correspondente à franquia.
3. Conferir os dados cadastrais e fiscais.
4. Adicionar o cliente ao grupo adequado:
   - **Grupo MP**, para lojas enquadradas na operação Maria Pitanga;
   - **Internacional**, quando essa classificação se aplicar à unidade.
5. Gravar e registrar o código do cliente no controle operacional da implantação.

Esse cadastro é obrigatório para que o cliente possa ser vinculado ao estabelecimento pelo parâmetro de sistema.

# 3. Cadastrar o estabelecimento e o grupo

## Telas 11630 e 11635

- Na tela 11630, buscar os dados pelo CNPJ.
- Conferir endereço, telefone, celular, inscrições e regime tributário.
- Aplicar o padrão definido para o nome fantasia.
- Na tela 11635, cadastrar o grupo e vinculá-lo ao estabelecimento.
- Vincular o usuário responsável pelo cadastro.
- Após gravar, conferir a criação automática de:
  - tabela de preço;
  - famílias;
  - PDV;
  - caixa;
  - caixa/banco.

## Vincular o estabelecimento ao cliente

Configurar o parâmetro de sistema:

| Tabela | Campo |
| --- | --- |
| `TBESTABELECIMENTO` | `VINCULO_ESTB_CLIENTE` |

No parâmetro, vincular o cliente cadastrado na tela 12360 ao respectivo estabelecimento.

Esse vínculo deve ser validado antes da configuração da integração com Ordem de Compra. Sem ele, a geração correta da OC pode ser comprometida.

**Ponto de controle:** confirmar que cliente, grupo de cliente, estabelecimento e grupo de estabelecimento estão relacionados corretamente.

# 4. Configurar usuários e acesso à perspectiva

Adicionar ao grupo do estabelecimento os usuários padrão:

- Tales;
- Deivid;
- João Batista;
- Simoneide;
- Hilgner;
- Jamile;
- GCWeb;
- Alves.

Na tela 19200, confirmar que a franquia aparece na **Mudança por Perspectiva** para os usuários que precisam acessar a unidade.

Se a franquia não aparecer, revisar:

- vínculo do usuário;
- estabelecimento;
- grupo de estabelecimento;
- permissões;
- acesso à perspectiva.

# 5. Configurar o PDV e a Ordem de Compra

## Tela 19020

- Conferir série, documentos padrão, descontos por operador e classificações de sangria e suprimento.
- Copiar os combos de um PDV já validado e compatível com o mesmo tipo de operação.
- Revisar os combos copiados antes de concluir a configuração.
- Selecionar as formas de pagamento utilizadas pela unidade:
  - Dinheiro;
  - Crédito;
  - Débito;
  - Pix;
  - Fidelidade;
  - Vale Colaborador;
  - Vouchers;
  - Cartão Voucher;
  - iFood;
  - 99Food.
- Se houver TEF, vincular **CRÉDITO TEF ELGIN** e **DÉBITO TEF ELGIN** e abrir o credenciamento.

## Integração de pedidos com Ordem de Compra

A integração de pedidos com Ordem de Compra deve ser habilitada em cada nova implantação:

1. Confirmar que o cliente da franquia está cadastrado na tela 12360.
2. Confirmar o parâmetro `TBESTABELECIMENTO.VINCULO_ESTB_CLIENTE`.
3. Habilitar a utilização de Ordem de Compra no cadastro do PDV.
4. Habilitar a integração de pedidos com Ordem de Compra.
5. Para lojas localizadas fora do Ceará, configurar o perfil do PDV como **Interestadual**.
6. Executar um teste de geração da OC e confirmar se o vínculo foi aplicado corretamente.
7. Registrar o resultado no controle operacional da implantação.

**Ponto de controle:** não considerar a integração concluída apenas pela configuração. É necessário gerar e conferir uma Ordem de Compra de teste.

# 6. Configurar delivery, quando aplicável

- Definir taxa por bairro ou quilometragem, com faixas e valores.
- Cadastrar bairros ausentes pela tela 21120.
- Configurar banner, fundo, cores, horários, latitude e longitude.
- Definir produtos e complementos do delivery.
- Validar os dados publicados antes de liberar o canal.

# 7. Configurar certificado e NFC-e

## Tela 21460

- Cadastrar o arquivo PFX e sua senha.
- Para NFC-e, configurar espécie 65, série validada, CSC e ID do CSC.
- Ajustar o generator conforme a última NFC-e da série para evitar duplicidade.
- Executar um teste fiscal autorizado antes da produção.
- Registrar a autorização ou a pendência no controle operacional da implantação.

# 8. Configurar fidelidade

## Tela 12620

- Criar o plano somente quando o recurso estiver contratado.
- Cadastrar conversão, validade, regra de pontuação e resgates aprovados pela franquia.
- Vincular o estabelecimento.
- Validar acúmulo e resgate antes da liberação.

# 9. Vincular a tributação

## Tela 27080

- Em cada família comercializada, acessar **Dados Contábeis / Fiscais**.
- Copiar ou cadastrar a regra para o estabelecimento.
- Validar operação, CFOP e CSTs de ICMS, PIS/COFINS e IPI com a contabilidade.
- Não liberar a venda de produtos sem a tributação aplicável à unidade.

# 10. Criar colaboradores

Na aba **Loja** da tela 19200:

- cadastrar colaboradores e cargos;
- indicar o administrador;
- validar usuário, cliente, colaborador, perspectiva e permissões;
- confirmar que cada colaborador acessa somente as operações autorizadas.

# 11. Executar a validação final

Antes do aceite, conferir:

- [ ] Primeiro contato realizado por Jamile.
- [ ] Franquia registrada na Planilha de Implantação.
- [ ] Cliente da franquia cadastrado na tela 12360.
- [ ] Cliente incluído no grupo correto: Grupo MP ou Internacional.
- [ ] Estabelecimento e grupo cadastrados.
- [ ] Parâmetro `TBESTABELECIMENTO.VINCULO_ESTB_CLIENTE` configurado.
- [ ] Usuários padrão vinculados ao grupo do estabelecimento.
- [ ] Perspectiva disponível para os usuários autorizados.
- [ ] PDV configurado e combos revisados.
- [ ] Ordem de Compra habilitada.
- [ ] Integração de pedidos com OC testada.
- [ ] Perfil **Interestadual** aplicado ao PDV de lojas fora do Ceará.
- [ ] Delivery validado, quando contratado.
- [ ] Certificado e NFC-e testados.
- [ ] Fidelidade validada, quando contratada.
- [ ] Produtos e preços iniciais conferidos e entregues pela equipe GCWeb, com taras quando controlado por balança.
- [ ] Tributação revisada.
- [ ] Colaboradores e permissões conferidos.
- [ ] Pendências, evidências e responsáveis registrados.

## Aceite da implantação

A implantação somente deve ser considerada concluída após:

1. validar os cadastros e os recursos contratados;
2. executar os testes operacionais e fiscais aplicáveis;
3. resolver ou formalizar todas as pendências;
4. atualizar a Planilha de Implantação;
5. registrar o responsável pela validação;
6. obter o aceite da franquia.

# 12. Manter produtos e preços após a implantação

## Responsável: Igor Dev

## Tela 27150

Na primeira implantação, a equipe GCWeb entrega os produtos e preços iniciais já configurados. O cadastro e os vínculos realizados por Igor acontecem **após a implantação e o treinamento**, conforme a necessidade da operação.

No atendimento pós-implantação:

- receber a solicitação ou a lista de produtos e preços por canal;
- verificar se cada produto já existe no cadastro central;
- criar um novo produto somente após confirmar que não existe equivalente;
- vincular cada produto ao estabelecimento na aba **Estabelecimentos (Venda)**;
- informar preços, canais, complementos e taras;
- utilizar **Sem Tara** quando aplicável;
- registrar a conclusão ou as inconsistências no controle operacional adotado pela equipe.

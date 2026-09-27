# Histórias de Usuário e Critérios de Aceitação (BDD)

### RF_01: Criação de Novo Projeto
**História:** Como pesquisador, quero criar um projeto de pesquisa no sistema, para registrar a pesquisa e dar início às atividades.
**Cenário (BDD):** Dado que o professor está autenticado, quando acessa a área de projetos e salva os dados, então o sistema registra com status "Ativo".

### RF_02: Edição dos Dados de um Projeto
**História:** Como pesquisador, quero editar informações sobre os meus projetos, para que acompanhem as mudanças de escopo.
**Cenário (BDD):** Dado que o professor acessa as configurações, quando altera a descrição e atualiza, então o sistema salva e exibe mensagem de sucesso.

### RF_03: Finalização de um Projeto
**História:** Como pesquisador, quero finalizar projetos concluídos, para encerrar atividades e manter histórico.
**Cenário (BDD):** Dado que o projeto cumpriu objetivos, quando o professor confirma a finalização, então o status muda para "Finalizado" e bloqueia interações.

### RF_04: Exclusão Definitiva de Projeto
**História:** Como pesquisador, quero excluir um projeto, para remover pesquisas cadastradas por engano.
**Cenário (BDD):** Dado a necessidade de remoção, quando seleciona "Excluir" e confirma a senha, então o projeto é apagado.

### RF_05: Criação de Subprojeto Vinculado
**História:** Como pesquisador, quero gerenciar subprojetos, para dividir um projeto grande em partes menores.
**Cenário (BDD):** Dado que está na aba de subprojetos, quando preenche os dados e adiciona, então o sistema cria o vínculo hierárquico.

### RF_06: Remoção de Subprojeto
**História:** Como pesquisador, quero remover subprojetos, para manter a estrutura atualizada.
**Cenário (BDD):** Dado um subprojeto sem resultados, quando clica em remover, então ele é excluído.

### RF_07: Envio de Convite para Novo Membro
**História:** Como pesquisador, quero convidar novos membros por e-mail, para delegar acessos.
**Cenário (BDD):** Dado que insere um e-mail válido e papel, quando clica em "Convidar", então dispara um e-mail com link exclusivo.

### RF_08: Revogação de Acesso (Com Resultado)
**História:** Como pesquisador, quero remover acesso de estudante que encerrou atividades, para revogar permissões sem perder histórico.
**Cenário (BDD):** Dado que um estudante tem resultados, quando removido, então o sistema revoga edições mas mantém tarefas entregues.

### RF_09: Revogação de Acesso (Sem Resultado)
**História:** Como pesquisador, quero remover membro inativo, para revogar permissões.
**Cenário (BDD):** Dado que não há resultados cadastrados, quando removido, então o sistema o apaga do projeto.

### RF_10: Criação e Atribuição de Tarefa
**História:** Como pesquisador, quero gerenciar tarefas com prazos e responsáveis, para organizar o fluxo de trabalho.
**Cenário (BDD):** Dado que preenche os dados da tarefa, quando salva, então o sistema cria com status "A Fazer" e notifica o estudante.

### RF_11: Atualização de Prazo de Tarefa
**História:** Como pesquisador, quero editar informações de tarefas, para reorganizar o fluxo.
**Cenário (BDD):** Dado que a tarefa está atribuída, quando edita a data final, então o sistema salva e notifica o responsável.

### RF_12: Avaliação de Entrega com Revisão
**História:** Como pesquisador, quero acessar um campo de avaliação para aprovar ou solicitar revisão, para validar resultados.
**Cenário (BDD):** Dado uma tarefa "Aguardando Avaliação", quando insere feedback e solicita revisão, então o status muda para "Em Revisão".

### RF_13: Listagem de Documentos Entregues
**História:** Como pesquisador, quero categorizar e visualizar arquivos de um projeto, para distingui-los.
**Cenário (BDD):** Dado que acessa a aba Documentos, quando carregada, então apresenta todos os arquivos já entregues.

### RF_14: Escolher Documento para Publicação
**História:** Como pesquisador, quero gerar relatórios e publicações, para dar visibilidade externa.
**Cenário (BDD):** Dado que está na aba Documentos, quando passa o cursor sobre um arquivo, então apresenta pop-up "Publicar".

### RF_15: Modal de Publicação
**História:** Como pesquisador, quero gerenciar metadados de um arquivo, para prepará-lo para visualização.
**Cenário (BDD):** Dado que clica no pop-up, quando carregado, então apresenta o modal de publicação.

### RF_16: Publicação de Resultado
**História:** Como pesquisador, quero publicar resultados, para promover atividades acadêmicas.
**Cenário (BDD):** Dado a tela modal preenchida, quando clica em publicar, então o documento é publicado.

### RF_17: Filtro de Demandas Pendentes
**História:** Como estudante, quero acessar tarefas atribuídas, para ter clareza e cumprir prazos.
**Cenário (BDD):** Dado que acessa "Minhas Tarefas", quando clica no filtro, então ordena pelas tarefas mais urgentes.

### RF_18: Submissão de Entrega (Primeiro Envio)
**História:** Como estudante, quero enviar arquivos de uma tarefa, para receber avaliação.
**Cenário (BDD):** Dado uma atividade "A Fazer" no prazo, quando faz upload e envia, então altera o status para "Entregue".

### RF_19: Substituição de Entrega
**História:** Como estudante, quero reenviar arquivos, para corrigir falhas antes do vencimento.
**Cenário (BDD):** Dado uma atividade "Entregue" no prazo, quando faz novo upload, então substitui a entrega antiga.

### RF_20: Bloqueio de Upload Fora do Prazo
**História:** Como estudante, quero consultar avaliações, para aplicar correções.
**Cenário (BDD):** Dado o término da vigência, quando tenta acessar, então o sistema altera para "Aguardando avaliação" e bloqueia uploads.

### RF_21: Interação no Fórum da Tarefa
**História:** Como estudante, quero enviar mensagens na tarefa, para tirar dúvidas com o orientador.
**Cenário (BDD):** Dado uma dúvida, quando digita e envia no fórum interno, então registra com data/hora no histórico.

### RF_22: Bloqueio de Interação no Fórum
**História:** Como administrador, quero gerenciar interações, para evitar discussões em tarefas passadas.
**Cenário (BDD):** Dado o encerramento do prazo, quando verificado pelo sistema, então bloqueia novas interações no fórum.

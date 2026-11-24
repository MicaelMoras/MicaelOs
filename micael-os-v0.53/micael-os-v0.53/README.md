# MICAEL OS 0.53 — Ajustes em Estudos e Pomodoro

## Exclusão de matérias

- Ao excluir uma matéria, o aplicativo também remove as sessões de estudo vinculadas ao seu ID.
- Os registros relacionados saem do histórico de Estudos, das estatísticas do Pomodoro, dos ciclos arquivados e do planejamento associado.
- Se o Pomodoro estiver usando a matéria excluída, a sessão provisória é descartada e o vínculo é limpo para não recriar registros órfãos.

## Limpeza inicial do histórico

- Na primeira abertura desta atualização, o histórico antigo de sessões de estudo e Pomodoro é zerado uma única vez.
- Matérias cadastradas, configurações do Pomodoro e os demais dados do MICAEL OS são preservados.
- A limpeza é identificada por uma marca de migração no armazenamento local e não se repete nas próximas aberturas.

## Sessões de estudo e Pomodoro

- Sessões em andamento ou pausadas ficam provisórias e não entram no tempo estudado, nas metas ou nas estatísticas.
- É possível pausar e retomar a sessão atual, inclusive depois de reabrir o aplicativo.
- **Salvar** registra os minutos completos estudados, mesmo antes do fim do Pomodoro.
- **Descartar** ou **Reiniciar** remove a sessão provisória sem somar seus minutos ao histórico.
- **Desfazer último registro** remove a sessão salva mais recentemente e atualiza o histórico, as estatísticas e o progresso da matéria.
- Sessões concluídas automaticamente pelo Pomodoro continuam sendo registradas normalmente.

## Dados e compatibilidade

- Mantém a chave local `personal-os-v1` e o armazenamento local do navegador.
- Recomenda-se exportar um backup JSON antes de substituir a versão anterior.


## Ajuste visual do formulário de matérias

- Os campos de frequência e tempo planejado usam altura fixa e alinhamento uniforme.
- Removidas as descrições extensas abaixo desses campos para deixar o formulário mais compacto.
- Removidos os controles de incremento/decremento nativos do campo numérico, mantendo a edição direta do valor.

## Recorrência diária em Estudos e Rotina

- Frequência **Diário** agora se repete automaticamente todos os dias, sem arquivar nem remover a matéria ou atividade na virada do dia.
- Em Estudos, a meta de minutos é reiniciada por data; o histórico de sessões anteriores continua preservado e as estatísticas seguem acumulando o tempo real.
- Em Rotina, cada data tem sua própria marcação de conclusão. A atividade permanece ativa nos dias seguintes.
- O editor de progresso de atividades diárias mostra os últimos sete dias para consultar e ajustar cada marcação.
- Uma migração única recupera matérias e atividades diárias arquivadas automaticamente por versões anteriores, mas respeita registros que tenham sido removidos manualmente.
- Frequências **Uma vez**, **Dias úteis**, **Semanal**, **Quinzenal**, **Mensal** e **Anual** mantêm o comportamento anterior.

## Correção de rotinas diárias duplicadas

- Uma migração única reúne atividades diárias com o mesmo nome e categoria em uma única rotina ativa.
- As marcações diárias dos registros reunidos são associadas à rotina mantida; registros do mesmo dia são consolidados sem duplicar a conclusão.
- Os ciclos antigos permanecem no histórico e nos relatórios, sem recriar rotinas ativas duplicadas.
- O indicador da página Rotina foi renomeado para **Histórico arquivado**, deixando claro que representa ciclos anteriores preservados, e não atividades em andamento.


## Reinicialização do histórico de Rotina (v0.57)

- Na primeira abertura desta versão, os ciclos arquivados de Rotina são zerados.
- As marcações de conclusão usadas nos testes também são removidas do histórico e dos relatórios de Rotina.
- As atividades que continuam ativas na rotina são preservadas, assim como todas as demais áreas, configurações e dados do aplicativo.
- A limpeza é executada uma única vez por meio da marca `routineTestHistoryResetV057`.

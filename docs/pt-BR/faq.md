# Perguntas frequentes (FAQ)

- **Visão geral e idiomas**: [Visão geral em português (Brasil)](../readme/README.pt-BR.md) | [English Overview](../../README.md)
- **Guias**: [Início rápido](quick-start.md) | [Backup e recuperação](recovery.md) | [Permissões e solução de problemas](permissions-troubleshooting.md) | **FAQ**
- **Idioma / Language**: **Português (Brasil)** | [English](../en/faq.md)

Respostas práticas para usar o **ContactMerge+ Cleaner** com segurança no iPhone, indicando o comportamento verificado e os limites de versão.

## Backups e correspondência de duplicados (`q01`–`q06`)

<a id="q01"></a>
### 1. Preciso de um backup `.vcf` antes de mesclar, ou o `Recovery History` já é suficiente?

Exportar um arquivo `.vcf` é opcional (o app não exige uma exportação antes de mesclar), mas manter um backup independente e datado antes da sua primeira limpeza ou de limpezas maiores é fortemente recomendado. O `Recovery History` é apenas um registro local limitado no dispositivo (no máximo 3 registros de mesclagem e no máximo 3 registros de exclusão por cerca de 30 dias), não consegue restaurar Notas de contatos não principais e não conta com backup na nuvem do desenvolvedor. A sincronização de contas (iCloud ou Google) não é um backup independente, pois as mesclagens podem ser sincronizadas entre dispositivos. Garanta que o backup cubra a conta real onde seus contatos estão salvos e contenha os registros esperados, e evite reimportações repetidas de `.vcf` ou restaurações completas do aparelho às cegas. Veja [Backup e recuperação](recovery.md) e [Backup Contacts Before Merge on iPhone (em inglês)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone).

<a id="q02"></a>
### 2. O que significa `Ready to merge`, e ainda assim devo revisar a pré-visualização?

`Ready to merge` significa que cada par de cartões no grupo passou por verificações rigorosas com base em evidências fortes entre todos os pares. Ainda assim, abra sempre a pré-visualização antes de confirmar: nomes ou números iguais, por si sós, não provam que dois cartões representam a mesma pessoa, e o app não consegue ler as Notas dos contatos. Selecione seu cartão principal, consulte o app **Contatos** da Apple para verificar se há Notas nos cartões não principais, confira os campos esperados na pré-visualização e só então confirme (ou inclua grupos `Ready to merge` em uma mesclagem em lote do Pro confirmada). Veja [Início rápido](quick-start.md) e [How to Merge Contacts Safely (em inglês)](https://contactmerge.app/guides/merge-contacts-safely).

<a id="q03"></a>
### 3. Por que um grupo aparece marcado como `Needs review`, e posso mesclá-lo em lote?

`Needs review` indica evidências mais fracas ou conflitantes — como um número residencial compartilhado, nomes diferentes, datas de aniversário conflitantes ou sobreposição parcial. Trata-se de uma verificação de segurança, e não de um erro no escaneamento. Os grupos em `Needs review` devem ser inspecionados e confirmados manualmente, um de cada vez, e não podem entrar na mesclagem em lote do Pro (não há como forçar grupos ambíguos na mesclagem em lote). Se tiver dúvida ou se representarem pessoas distintas, deixe os cartões sem mesclar. Veja [Início rápido](quick-start.md).

<a id="q04"></a>
### 4. Devo mesclar quando os nomes são diferentes — ou quando dois cartões têm exatamente o mesmo nome?

Nenhum dos dois casos é automático. Diferenças no nome (como apelido versus nome completo) não significam automaticamente pessoas diferentes, enquanto nomes idênticos ainda podem pertencer a dois parentes ou colegas de trabalho distintos. Esta documentação não afirma regras exatas de uso de maiúsculas/minúsculas ou normalização de texto na correspondência em tempo de execução. Na pré-visualização, compare os dados efetivamente exibidos ali (como nomes, números de telefone e endereços de e-mail, quando presentes) — nunca presuma que um campo ou uma Nota esteja vazio no cartão de contato apenas porque não aparece na pré-visualização. Abra os cartões originais no app **Contatos** da Apple para verificar dados de empresa/empregador, outras informações adicionais de identidade e eventuais Notas que queira preservar; se sair para consultar ou editar cartões lá, volte e verifique novamente os candidatos atuais e a pré-visualização antes de confirmar (não presuma que telas abertas se atualizam automaticamente). Veja [Início rápido](quick-start.md).

<a id="q05"></a>
### 5. Duas pessoas diferentes compartilham um telefone residencial ou comercial. O que devo fazer?

**Não** os mescle. Familiares que dividem um telefone fixo, parceiros que compartilham um número de emergência ou colegas de trabalho que usam a linha principal da recepção costumam aparecer como candidatos — geralmente em `Needs review`. A mesclagem combina pessoas diferentes em um único cartão. Deixe pessoas distintas sem mesclar e confirme apenas quando todos os cartões representarem a mesma pessoa. Veja [Início rápido](quick-start.md).

<a id="q06"></a>
### 6. Por que datas de aniversário conflitantes sinalizaram um grupo para revisão?

Datas de aniversário conflitantes entre cartões (mencionadas em registros históricos de lançamento e suporte da versão 1.3.6 ao lado de conflitos de nome) servem como um sinal prático para inspeção manual, e não como um limite exato publicado de algoritmo. Datas diferentes podem indicar dois parentes que compartilham dados de contato ou um erro de digitação em um cartão antigo. Verifique ambos os cartões na pré-visualização e no app **Contatos** da Apple antes de decidir. Veja [Início rápido](quick-start.md).

## Contas, transferências e app Contatos da Apple (`q07`–`q11`)

<a id="q07"></a>
### 7. Como o app funciona com a sincronização de contatos do iCloud ou do Google?

Os contatos são processados localmente no seu iPhone, sem envio para servidores do desenvolvedor e sem backup na nuvem do desenvolvedor. No entanto, a sincronização do iCloud/Google e os backups do sistema iOS são mecanismos independentes controlados pelas suas configurações; por isso, as mesclagens confirmadas podem ser sincronizadas entre dispositivos conectados. Nunca desative e reative a sincronização, não remova contas, não toque em `"Delete from My iPhone"` nem exclua contatos sincronizados de origem para tentar resolver problemas — excluir contatos de contas de e-mail ou nuvem pode apagá-los permanentemente em todos os dispositivos (consulte o [guia de contas da Apple (em inglês)](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios) e o [aviso de exclusão da Apple (em inglês)](https://support.apple.com/en-us/111793)). Identifique sua conta e faça um backup primeiro; se tiver dúvida, pare e procure o [Suporte oficial (em inglês)](https://contactmerge.app/support). Veja [iCloud Duplicate Contacts After Sync (em inglês)](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync).

<a id="q08"></a>
### 8. Por que surgiram duplicados após configurar um novo iPhone ou usar o Migrar para iOS?

Configurar um iPhone novo, usar o Migrar para iOS (Move to iOS), importar arquivos ou conectar várias contas frequentemente expõe duplicados antigos vindos de diferentes origens — isso não significa que seu telefone esteja com defeito nem comprova uma única causa garantida. Aguarde o término da migração e da sincronização inicial em segundo plano antes de escanear (isso não garante a remoção dos duplicados por si só, mas evita alterações no meio da sincronização), faça um backup independente e revise as pré-visualizações conforme o [Início rápido](quick-start.md). Veja [Duplicate Contacts After Setting Up a New iPhone (em inglês)](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone) e [Move to iOS Duplicate Contacts (em inglês)](https://contactmerge.app/guides/move-to-ios-duplicate-contacts).

<a id="q09"></a>
### 9. A opção `View Duplicates` da Apple não aparece — qual é a diferença do ContactMerge+ Cleaner?

No app **Contatos** da Apple, `View Duplicates` (exibir duplicados) aparece abaixo de `My Card` (meu cartão) quando disponível, enquanto a opção manual `Link Contacts` (vincular contatos) apenas unifica a visualização sem mesclar os cartões subjacentes (e edições no cartão unificado podem se propagar para as contas de origem; veja o [guia de duplicados da Apple (em inglês)](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios)). A ausência de `View Duplicates` no sistema é algo separado das permissões do app — não existe um limite garantido de 1.000 contatos, tempo fixo de espera nem solução segura de "mesclar tudo" de uma só vez. Conceda acesso aos Contatos no ContactMerge+ Cleaner para escanear localmente e inspecionar as pré-visualizações. Veja [Permissões e solução de problemas](permissions-troubleshooting.md).

<a id="q10"></a>
### 10. Contatos duplicados podem ter o mesmo número com e sem código do país?

Sim — um cartão pode armazenar um número local enquanto outro inclui o código de país (como `+55` ou `+1`), o que o aviso nativo de duplicados da Apple pode não sinalizar como correspondência exata. Sem afirmar regras exatas de normalização telefônica do algoritmo, o ContactMerge+ Cleaner permite comparar os números completos na pré-visualização da mesclagem. Verifique se ambos pertencem à mesma pessoa e se o formato esperado será mantido antes de confirmar. Veja [iOS View Duplicates and Country Code Formatting (em inglês)](https://contactmerge.app/guides/ios-view-duplicates-country-code).

<a id="q11"></a>
### 11. O ContactMerge+ Cleaner funciona com listas grandes de contatos?

Você pode escanear agendas grandes localmente mesmo quando o aviso `View Duplicates` da Apple não aparece, revisando os resultados em `Ready to merge` e `Needs review`. Porém, o app não promete velocidades específicas de escaneamento nem capacidade ilimitada. Aguarde o fim da sincronização em segundo plano, crie um backup independente e datado e teste a mesclagem de um único grupo primeiro. Veja [Permissões e solução de problemas](permissions-troubleshooting.md) e [View Duplicates Missing on a Large Contact List (em inglês)](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list).

## Desfazer, Histórico de recuperação e Notas dos contatos (`q12`–`q14`)

<a id="q12"></a>
### 12. Onde fica o `Undo Last Contact Merge` e o que ele cobre?

O `Undo Last Contact Merge` atua apenas sobre a única mesclagem mais recente. Na captura aprovada do simulador Release em inglês datada de `2026-11-03`, ele aparece perto do topo dos resultados do escaneamento em `Duplicate Contacts`, acima de `Ready to merge`. Como essa informação se baseia nessa captura datada do simulador (e não em um teste em tempo real na versão instalada no seu aparelho), o estado de ativação, os rótulos e os avisos podem variar, além de não ser uma restauração completa (Notas de cartões não principais não podem ser restauradas, e IDs/vínculos originais do sistema podem não retornar). Veja [Backup e recuperação](recovery.md).

<a id="q13"></a>
### 13. Quais são os limites do `Recovery History` e como faço para abri-lo?

O `Recovery History` salva **no máximo 3 registros de mesclagem e no máximo 3 registros de exclusão** por **cerca de 30 dias no seu dispositivo** (limites separados por tipo, e não 6 registros garantidos). Entradas mais antigas ou excedentes não podem ser restauradas, e a recuperação não é garantida após desinstalar o app ou perder o aparelho. **Caminho não verificado**: seu ponto de entrada e as etapas de seleção de registros não aparecem nas capturas aprovadas, por isso não adivinhamos caminhos de menu — entre em contato com o [Suporte oficial (em inglês)](https://contactmerge.app/support) para obter ajuda na sua versão. Veja [Backup e recuperação](recovery.md).

<a id="q14"></a>
### 14. Por que verificar as Notas no app Contatos da Apple — e o que mais limita a recuperação?

O ContactMerge+ Cleaner não consegue ler as Notas dos contatos: Notas de cartões não principais **não** são copiadas durante as mesclagens nem podem ser restauradas via `Undo Last Contact Merge` ou `Recovery History`. A ausência de Notas na pré-visualização nunca significa que o cartão não tenha Notas — inspecione-as e copie-as no app **Contatos** da Apple antes de mesclar. Após visualizar ou editar contatos fora do app, volte e verifique novamente os candidatos atuais e a pré-visualização (telas abertas podem não atualizar automaticamente). Os IDs/vínculos do sistema podem não ser restaurados e, por precaução conservadora, edições posteriores ou atualizações de sincronização podem impedir uma recuperação limpa. Veja [Backup e recuperação](recovery.md).

## Grátis vs. Pro, compras e suporte (`q15`–`q18`)

<a id="q15"></a>
### 15. O que está incluído na versão Grátis (Free) vs. Pro?

A versão **Free** inclui escanear, visualizar todos os grupos candidatos e mesclar um grupo por vez com até 3 contatos nesse grupo (sem mesclagem em lote de vários grupos). O **Pro** é um desbloqueio por compra única na App Store, **sem assinatura**, pelo preço regional exibido pela Apple. O Pro desbloqueia grupos com mais de 3 contatos e a mesclagem em lote para grupos `Ready to merge` confirmados (`Needs review` continua sendo revisado manualmente, um por vez). Veja [Início rápido](quick-start.md).

<a id="q16"></a>
### 16. Como restauro minha compra do Pro?

O Pro é uma compra não consumível. Confirme que seu iPhone está conectado à **mesma Conta Apple (Apple Account)** usada na compra original e consulte o guia da Apple: [If you can't find or use your in-app purchases (em inglês)](https://support.apple.com/en-us/108096). Como o caminho exato da interface de restauração dentro do app não é verificado aqui, não adivinhamos rótulos de menus de configurações ou atualização, não recomendamos comprar novamente nem garantimos restauração automática. Se o Pro continuar bloqueado, fale com o [Suporte oficial (em inglês)](https://contactmerge.app/support) ou com o Suporte da Apple. Veja [Permissões e solução de problemas](permissions-troubleshooting.md).

<a id="q17"></a>
### 17. Como funcionam os reembolsos da Apple — e existe alguma assinatura para cancelar?

O Pro é uma compra única, não uma assinatura — não siga instruções de cancelamento de assinatura para este app. A Apple processa as cobranças da App Store e decide a elegibilidade para reembolso de acordo com o país ou a região; **os reembolsos não são garantidos**. As solicitações de reembolso são feitas pelo processo oficial da Apple em [reportaproblem.apple.com (em inglês)](https://reportaproblem.apple.com) (veja o [guia de reembolso da Apple (em inglês)](https://support.apple.com/en-us/118223)), e o desenvolvedor não pode garantir a aprovação. Veja [Permissões e solução de problemas](permissions-troubleshooting.md).

<a id="q18"></a>
### 18. Como verifico as permissões, protejo minha privacidade e entro em contato com o suporte com segurança?

Verifique as permissões de Contatos nas configurações de privacidade do iOS (em inglês: `Settings > Privacy & Security > Contacts`; veja o [guia de acesso aos Contatos da Apple (em inglês)](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios)); o acesso limitado apenas restringe a visibilidade do app sem excluir contatos, embora não haja garantia de suporte para todos os fluxos de acesso limitado. O processamento é local, sem envio para servidores do desenvolvedor (separado da sua sincronização do iCloud/Google e dos backups do iOS; consulte a [Política de Privacidade (em inglês)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)). Ao acionar o [Suporte oficial (em inglês)](https://contactmerge.app/support), informe as versões do app e do iOS, se é um controle da Apple ou tela do app, o tipo de conta (sem ID), a contagem aproximada e o comportamento esperado versus observado — nunca publique listas de contatos, arquivos `.vcf`, dados pessoais reais, senhas ou comprovantes de pagamento publicamente. Veja [Permissões e solução de problemas](permissions-troubleshooting.md).

## Status da documentação

Verificado em 8 de novembro de 2026. As telas, os rótulos e o comportamento podem variar dependendo da versão instalada do app e da versão do iOS.

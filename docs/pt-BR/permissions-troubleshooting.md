# Permissões e solução de problemas

- **Visão geral e idiomas**: [Visão geral em português (Brasil)](../readme/README.pt-BR.md) | [English Overview](../../README.md)
- **Guias**: [Início rápido](quick-start.md) | [Backup e recuperação](recovery.md) | **Permissões e solução de problemas** | [FAQ](faq.md)
- **Idioma / Language**: **Português (Brasil)** | [English](../en/permissions-troubleshooting.md)

Este guia aborda as configurações de permissão de Contatos no iPhone, como o **ContactMerge+ Cleaner** difere dos recursos nativos de duplicados da Apple, o cuidado seguro com contas sincronizadas e transferências de aparelho, dúvidas sobre compra e reembolso, e como acionar o suporte com segurança.

## Permissão de Contatos no iPhone

- **Necessária para escanear e mesclar**: O ContactMerge+ Cleaner precisa de acesso aos Contatos para encontrar e mesclar duplicados no seu iPhone. O processamento dos contatos ocorre localmente no dispositivo — sua agenda não é enviada para servidores do desenvolvedor, e o desenvolvedor não oferece um serviço de backup na nuvem (isso é separado de qualquer sincronização de contatos do iCloud/Google ou de backups do sistema iOS controlados pelas suas próprias configurações).
- **Acesso total vs. acesso limitado no iOS**: Dependendo da versão do iOS, a Apple permite controlar quais contatos um app pode acessar — incluindo acesso total ou acesso limitado a contatos selecionados — nas configurações de privacidade e Contatos do iOS (em inglês: `Settings > Privacy & Security > Contacts`; consulte o guia da Apple: [Control access to Contacts on iPhone (em inglês)](https://support.apple.com/guide/iphone/control-access-to-contacts-iph9536aa9a5/ios)).
- **Se o escaneamento estiver bloqueado ou faltarem contatos**:
  - Verifique o nível de permissão de Contatos concedido ao ContactMerge+ Cleaner nas configurações do iOS. O acesso incompleto ou limitado pode restringir quais contatos o app consegue visualizar — isso **não** exclui seus contatos, embora não haja garantia de que o app ofereça suporte a todos os fluxos de acesso limitado.
  - Se a opção parecer indisponível ou continuar apresentando comportamento inesperado após conferir as configurações do iOS, entre em contato com o [Suporte oficial (em inglês)](https://contactmerge.app/support).
- **O que não fazer**: Nunca desative e reative a sincronização de contas, não remova contas, não exclua contatos nem reimporte arquivos `.vcf` para tentar resolver problemas de permissão.

## ContactMerge+ Cleaner vs. ferramentas nativas de duplicados da Apple

O app **Contatos** da Apple inclui recursos integrados de duplicados e vinculação que funcionam de maneira diferente do ContactMerge+ Cleaner (consulte o guia da Apple: [Merge or hide duplicate contacts on iPhone (em inglês)](https://support.apple.com/guide/iphone/merge-or-hide-duplicate-contacts-iph2ab28320d/ios)):

- **`View Duplicates` no app Contatos da Apple**: Quando disponível, a Apple exibe um aviso `View Duplicates` (exibir duplicados) abaixo de `My Card` (meu cartão) para revisar e mesclar duplicados detectados. Se o aviso `View Duplicates` da Apple não aparecer — por exemplo, quando os números usam formatos diferentes de código de país ou em algumas agendas grandes —, diferencie esse comportamento do sistema de um problema de permissão do app. Esta documentação não afirma quais são as regras internas de detecção da Apple, não garante um limite específico de quantidade de contatos (como 1.000 contatos), nem promete um tempo fixo de espera ou uma solução genérica de "mesclar tudo".
- **Contatos vinculados / unificados vs. cartões mesclados**: Vincular contatos manualmente (`Link Contacts`) no app **Contatos** da Apple unifica a forma como os cartões são exibidos em uma única visualização sem mesclar os cartões de origem subjacentes, e as edições feitas em um cartão unificado podem se propagar para as contas conectadas.
- **Como o ContactMerge+ Cleaner se diferencia**: O ContactMerge+ Cleaner escaneia localmente no seu dispositivo e separa os candidatos em `Ready to merge` e `Needs review` para que você possa inspecionar uma pré-visualização da mesclagem primeiro (enquanto verifica o app **Contatos** da Apple para conferir as Notas). Ele não promete velocidades específicas de escaneamento, limites de tamanho da lista de contatos nem reparo automático de danos anteriores na agenda.
- Guias oficiais relacionados na web:
  - [iOS View Duplicates and Country Code Formatting (em inglês)](https://contactmerge.app/guides/ios-view-duplicates-country-code)
  - [View Duplicates Missing on a Large Contact List (em inglês)](https://contactmerge.app/guides/view-duplicates-missing-large-contact-list)

## Migração, sincronização de contas e como evitar exclusões acidentais

Configurar um novo iPhone, usar o Migrar para iOS (Move to iOS), importar arquivos ou conectar múltiplas contas (como iCloud e Google) frequentemente revela duplicados antigos entre contas, sem significar que seu aparelho esteja com defeito:

- **Conclua a sincronização inicial e faça um backup primeiro**: Espere até que a migração do dispositivo ou a sincronização inicial das contas termine antes de avaliar os duplicados (isso não garante a eliminação automática dos duplicados por si só, mas evita confusão no meio da sincronização). Identifique qual conta armazena seus contatos e faça um backup independente e datado antes de alterar qualquer coisa.
- **Revise com cuidado**: Inspecione as pré-visualizações de mesclagem (especialmente os grupos em `Needs review`) e salve quaisquer Notas de contatos não principais no app **Contatos** da Apple primeiro; se você sair do app para visualizar ou editar contatos, volte e confira novamente os candidatos atuais e a pré-visualização antes de confirmar.
- **Prevenção obrigatória contra exclusões**: Remover uma conta dos Contatos funciona de forma diferente de excluir contatos individuais, e apagar contatos de uma conta sincronizada de e-mail ou nuvem pode excluí-los permanentemente em todos os dispositivos sincronizados (apenas como contexto informativo, consulte [Add or remove accounts in Contacts on iPhone (em inglês)](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios) e o [aviso da Apple sobre exclusão de contatos (em inglês)](https://support.apple.com/en-us/111793)). **Não** exclua contatos de origem, não toque em `"Delete from My iPhone"`, não desative/reative a sincronização nem reimporte arquivos `.vcf` repetidamente como atalho de limpeza — se tiver dúvida, pare e fale com o [Suporte oficial (em inglês)](https://contactmerge.app/support).
- Guias oficiais por cenário:
  - [Duplicate Contacts After Setting Up a New iPhone (em inglês)](https://contactmerge.app/guides/duplicate-contacts-after-new-iphone)
  - [Move to iOS Duplicate Contacts (em inglês)](https://contactmerge.app/guides/move-to-ios-duplicate-contacts)
  - [iCloud Duplicate Contacts After Sync (em inglês)](https://contactmerge.app/guides/icloud-duplicate-contacts-after-sync)
  - [Backup Contacts Before Merge on iPhone (em inglês)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
  - [How to Merge Contacts Safely (em inglês)](https://contactmerge.app/guides/merge-contacts-safely)

## Desbloqueio do Pro, restauração de compras e reembolsos

- **Desbloqueio único (não é assinatura)**: O Pro é uma compra única não consumível na App Store, com preço regional exibido pela Apple — **não** siga instruções de cancelamento de assinatura para este app. Ele libera grupos com mais de 3 contatos e a mesclagem em lote para grupos `Ready to merge` confirmados (`Needs review` permanece um por vez).
- **Restaurando o Pro**: Certifique-se de que seu iPhone esteja conectado à **mesma Conta Apple (Apple Account)** usada na compra original e consulte o guia oficial da Apple: [If you can't find or use your in-app purchases (em inglês)](https://support.apple.com/en-us/108096). Como o caminho exato do botão de restauração dentro do app não é verificado nesta documentação, não adivinhamos nomes de menus, não recomendamos comprar o Pro novamente nem garantimos restauração automática — se a restauração falhar, entre em contato com o [Suporte oficial (em inglês)](https://contactmerge.app/support) ou com o Suporte da Apple.
- **Solicitações de reembolso**: A cobrança da App Store e a elegibilidade para reembolso são decididas pela Apple de acordo com o país ou a região. Algumas compras podem ser elegíveis para reembolso, mas **os reembolsos não são garantidos**. As solicitações de reembolso utilizam o processo oficial da Apple em [reportaproblem.apple.com (em inglês)](https://reportaproblem.apple.com) (consulte [Request a refund for apps or content that you bought from Apple (em inglês)](https://support.apple.com/en-us/118223)), e o desenvolvedor não pode garantir a aprovação.

## Contato com o suporte e proteção da sua privacidade

- **Suporte**: [Suporte oficial (em inglês)](https://contactmerge.app/support)
- **Detalhes úteis e seguros para informar**: A versão do seu app ContactMerge+ Cleaner, a versão do iOS, o que você esperava versus o que observou, se a tela é um controle de sistema da Apple ou interna ao ContactMerge+ Cleaner, o tipo de conta envolvida (ex.: iCloud ou Google, **sem** informar seu e-mail ou ID da conta) e uma contagem aproximada de contatos, se relevante.
- **Regras rigorosas de privacidade e ocultação de dados**:
  - Nunca envie listas privadas de contatos, arquivos `.vcf` (vCard), senhas, dados de pagamento ou comprovantes de compra em relatos públicos (Issues) — trate quaisquer detalhes de cobrança exclusivamente pelos canais oficiais seguros da Apple ou por um canal privado oficial apropriado de suporte, quando necessário.
  - Oculte todos os nomes reais, números de telefone, endereços de e-mail, fotos, endereços residenciais, notas e IDs antes de compartilhar capturas de tela — utilize dados fictícios de demonstração sempre que possível.

## Links relacionados

- [Início rápido: escaneando e mesclando com segurança](quick-start.md)
- [Backup, Desfazer e Histórico de recuperação](recovery.md)
- [Perguntas frequentes (FAQ)](faq.md)
- [Site oficial (em inglês)](https://contactmerge.app)
- [Política de Privacidade (em inglês)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Status da documentação

Verificado em 8 de novembro de 2026. As telas, os rótulos e o comportamento podem variar dependendo da versão instalada do app e da versão do iOS.

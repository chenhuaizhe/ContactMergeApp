# Backup, Desfazer e Histórico de recuperação

- **Visão geral e idiomas**: [Visão geral em português (Brasil)](../readme/README.pt-BR.md) | [English Overview](../../README.md)
- **Guias**: [Início rápido](quick-start.md) | **Backup e recuperação** | [Permissões e solução de problemas](permissions-troubleshooting.md) | [FAQ](faq.md)
- **Idioma / Language**: **Português (Brasil)** | [English](../en/recovery.md)

Este guia explica as práticas recomendadas de backup antes de mesclar, como funcionam o recurso de desfazer e a recuperação local no dispositivo no **ContactMerge+ Cleaner**, e os limites que você precisa conhecer antes de mesclar contatos.

## Backup independente antes de mesclar

- **Exportação opcional de `.vcf`**: Exportar um arquivo `.vcf` (vCard) é opcional — o ContactMerge+ Cleaner não obriga você a exportar um arquivo antes de mesclar.
- **Backup independente e datado recomendado**: Manter um backup independente e com data antes de mesclar é fortemente recomendado, principalmente antes da sua primeira limpeza ou de uma mesclagem em lote. O ContactMerge+ Cleaner não oferece um serviço de backup na nuvem do desenvolvedor nem exporta automaticamente arquivos externos de backup.
- **Verifique o que o seu backup cobre**: Certifique-se de que o backup cubra a conta de origem real onde seus contatos estão armazenados (como iCloud ou Google, em vez de uma conta vazia) e contenha a quantidade de contatos e os detalhes esperados. A sincronização de contas não é um backup independente, pois as alterações feitas durante a limpeza podem ser sincronizadas com seus outros dispositivos conectados.
- **Evite tentativas destrutivas de restauração**: Não reimporte arquivos `.vcf` repetidamente nem faça uma restauração completa do dispositivo às cegas para corrigir um pequeno problema nos contatos — isso pode multiplicar duplicados ou sobrescrever edições mais recentes.
- **Leitura complementar**: Consulte [Backup Contacts Before Merge on iPhone (em inglês)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone) e [How to Merge Contacts Safely (em inglês)](https://contactmerge.app/guides/merge-contacts-safely).

## Verifique e salve as Notas dos contatos no app Contatos da Apple

As Notas importantes em contatos não principais (os outros cartões mesclados ao cartão principal) **não** são lidas nem copiadas durante uma mesclagem. Antes de confirmar qualquer mesclagem:

- **Inspecione as Notas no app Contatos da Apple, e não na pré-visualização**: O ContactMerge+ Cleaner não consegue ler as Notas dos contatos. Nunca presuma que um contato não possui Notas só porque nenhuma aparece na pré-visualização do ContactMerge+ Cleaner — abra o app **Contatos** da Apple para verificar esses cartões e copie manualmente quaisquer Notas importantes para o contato principal (ou outro local seguro) antes de mesclar.
- **Verifique novamente após sair do app**: Se você sair do ContactMerge+ Cleaner para visualizar ou editar contatos no app **Contatos** da Apple, retorne depois e confira novamente os candidatos duplicados atuais e a pré-visualização da mesclagem antes de confirmar. Não presuma que uma lista de candidatos ou pré-visualização já aberta será atualizada ou iniciará um novo escaneamento automaticamente.
- **As Notas não podem ser restauradas depois**: Como o ContactMerge+ Cleaner não consegue ler Notas, as Notas de cartões não principais não podem ser restauradas posteriormente por meio de `Undo Last Contact Merge` ou `Recovery History`.

## Revertendo alterações recentes no app

O ContactMerge+ Cleaner inclui dois recursos de recuperação local no dispositivo com limites estritos de escopo:

- **`Undo Last Contact Merge` (mesclagem mais recente)**:
  - Atua somente sobre a única mesclagem mais recente.
  - **Localização verificada na captura de demonstração**: Para procurar a opção de desfazer após sua última mesclagem, abra ou retorne à tela de resultados do escaneamento `Duplicate Contacts` e verifique perto do topo da tela, acima da seção `Ready to merge`, em busca de `Undo Last Contact Merge` (localização exibida na captura de demonstração em simulador de `2026-11-03`).
  - **Avisos de verificação e versão**: Essa localização do controle foi verificada a partir da captura de tela do simulador Release em inglês datada de `2026-11-03`, e não por meio de um teste em tempo real na versão instalada no seu aparelho. Os textos e o layout da tela podem variar conforme a versão do app ou do iOS, e este guia não afirma quando o controle fica habilitado na sua sessão, que a reversão completa de ponta a ponta tenha sido testada na sua versão instalada, nem que todas as propriedades subjacentes do contato sejam revertidas (também não pressupõe um aviso específico de confirmação).
- **`Recovery History` (histórico de recuperação)**:
  - Usa um registro de recuperação local salvo pelo app no seu iPhone.
  - Mantém **no máximo 3 registros de mesclagem e no máximo 3 registros de exclusão** (são limites separados por tipo de ação, e não uma garantia de que 6 registros estarão disponíveis a qualquer momento).
  - As entradas permanecem no dispositivo por **cerca de 30 dias**; entradas mais antigas ou que ultrapassem o limite de 3 registros daquele tipo de ação não podem ser restauradas.
  - **Caminho de navegação não verificado**: O ponto de entrada, a navegação entre telas e as etapas de seleção de registros do `Recovery History` não aparecem nas capturas de tela aprovadas; por isso, este guia marca o caminho de navegação como não verificado, em vez de adivinhar nomes de menus para a sua versão instalada do app. Se você não conseguir localizar o `Recovery History`, entre em contato com o [Suporte oficial (em inglês)](https://contactmerge.app/support).

## Limites importantes da recuperação local no dispositivo

Tenha em mente o que `Undo Last Contact Merge` e `Recovery History` **não** oferecem:

- **Não é uma restauração completa do sistema**: As Notas dos contatos não podem ser lidas nem restauradas a partir de cartões não principais, e os identificadores originais do sistema e vínculos entre contatos podem não ser restaurados. O app também não repara danos anteriores arbitrários na agenda causados por outras ferramentas ou importações.
- **Sem backup na nuvem do desenvolvedor; separado da sincronização de contas e dos backups do sistema**:
  - O processamento de contatos e o registro de recuperação permanecem no seu dispositivo dentro do app; o desenvolvedor não envia sua agenda para servidores próprios nem oferece um serviço de backup na nuvem.
  - **A sincronização de contas e os backups do iOS são separados**: A sincronização de contatos do iOS ou de contas (como iCloud ou Google) e os backups do sistema ou do dispositivo são mecanismos independentes controlados pelas configurações da sua conta e do iOS. Esta documentação **não** garante que uma mesclagem ficará fora da sincronização do iCloud/Google e **não** garante se os backups do sistema incluem ou excluem dados do app.
  - A recuperação não é garantida se você desinstalar o app ou perder ou trocar seu iPhone.
- **Precaução conservadora caso os contatos sejam editados depois**: Como orientação conservadora de segurança (e não como um bloqueio rígido verificado no app), a recuperação não pode ser garantida se os contatos afetados forem editados ou sobrescritos por sincronização posteriormente (no app **Contatos** da Apple, em outro app, em outro dispositivo ou via sincronização de conta). Evite editar contatos mesclados se você ainda puder querer desfazer essa mesclagem.
- **Nunca tente resolver problemas excluindo contatos de origem ou removendo contas**: Excluir contatos armazenados em uma conta sincronizada de e-mail ou nuvem pode apagá-los permanentemente em todos os seus dispositivos (veja o [aviso sobre exclusão de contatos da Apple (em inglês)](https://support.apple.com/en-us/111793) e o [guia de gerenciamento de contas da Apple (em inglês)](https://support.apple.com/guide/iphone/add-or-remove-accounts-iph7edacccf9/ios)). Não toque em `"Delete from My iPhone"`, não desative e reative a sincronização da conta nem remova contas para tentar corrigir uma mesclagem — em caso de dúvida, pare e procure o suporte primeiro.

## Obtendo suporte com segurança

- Entre em contato pelo [Suporte oficial (em inglês)](https://contactmerge.app/support) informando a versão do app ContactMerge+ Cleaner, a versão do iOS, se você está vendo uma tela do app Contatos da Apple ou uma tela do ContactMerge+ Cleaner, o tipo de conta relevante (como iCloud ou Google, sem compartilhar o ID da sua conta) e o que você esperava versus o que aconteceu.
- **Proteja sua privacidade**: Nunca publique listas de contatos, arquivos `.vcf`, senhas, dados de pagamento ou comprovantes de compra em relatos públicos (Issues). Oculte todos os nomes reais, números de telefone, endereços de e-mail, fotos, endereços residenciais, notas e IDs antes de compartilhar qualquer captura de tela — ou utilize apenas dados fictícios de demonstração.

## Links relacionados

- [Início rápido: escaneando e mesclando com segurança](quick-start.md)
- [Permissões e solução de problemas](permissions-troubleshooting.md)
- [Perguntas frequentes (FAQ)](faq.md)
- [Site oficial (em inglês)](https://contactmerge.app)
- [Política de Privacidade (em inglês)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Status da documentação

Verificado em 8 de novembro de 2026. As telas, os rótulos e o comportamento podem variar dependendo da versão instalada do app e da versão do iOS.

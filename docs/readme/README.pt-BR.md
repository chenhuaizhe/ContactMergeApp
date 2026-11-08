# ContactMerge+ Cleaner — Documentação do produto e suporte

Documentação pública oficial do produto e guias de suporte do **ContactMerge+ Cleaner** para iPhone. Este repositório contém apenas documentação para usuários — não é um repositório de código-fonte do aplicativo.

O ContactMerge+ Cleaner processa seus contatos localmente no dispositivo, não envia sua agenda para servidores do desenvolvedor, e o desenvolvedor não oferece um serviço de backup na nuvem. (A sincronização de contatos do iOS ou de contas — como iCloud ou Google — e os backups do sistema ou do dispositivo são mecanismos separados, controlados pelas configurações da sua própria conta e do iOS.)

- **Site**: [Site oficial (em inglês)](https://contactmerge.app)
- **App Store**: [Baixar na App Store (em inglês)](https://apps.apple.com/us/app/contactmerge-contacts-cleaner/id6738980785)
- **Suporte**: [Suporte oficial (em inglês)](https://contactmerge.app/support)
- **Idiomas**: [English](../../README.md) | [Deutsch](README.de.md) | [Français](README.fr.md) | [Italiano](README.it.md) | [Español](README.es.md) | **Português (Brasil)** | [日本語](README.ja.md) | [한국어](README.ko.md) | [简体中文](README.zh-Hans.md) | [繁體中文](README.zh-Hant.md)

## Início rápido em 4 passos

1. **Faça um backup e conceda permissão aos Contatos**: Mantenha um backup independente e datado antes de limpezas importantes (a exportação de `.vcf` é opcional), aguarde a conclusão de qualquer transferência de celular ou sincronização inicial e permita o acesso aos Contatos quando o iOS solicitar.
2. **Escaneie**: Execute um escaneamento para encontrar possíveis grupos de contatos duplicados no seu iPhone.
3. **Revise a pré-visualização, escolha o contato principal e verifique as Notas no app Contatos**: Abra um grupo de duplicados, revise a pré-visualização da mesclagem (`Merge Preview`), escolha o contato principal que será mantido como cartão base e consulte o app **Contatos** da Apple para verificar se há Notas que você deseja salvar.
4. **Verifique novamente e confirme com cuidado**: Se você saiu do app para visualizar ou editar contatos no app **Contatos** da Apple, volte e confira novamente os candidatos duplicados atuais e a pré-visualização antes de prosseguir. Confirme apenas quando os cartões pertencerem claramente à mesma pessoa e a pré-visualização mantiver os campos esperados.

<img src="../../assets/scan-results-demo.png" alt="Demonstração em simulador com interface em inglês (não é uma captura localizada em português; capturada em 2026-11-03) dos resultados do escaneamento em Duplicate Contacts com contatos fictícios exibindo Undo Last Contact Merge, Ready to merge e Needs review; telas e textos podem variar conforme a versão do app ou do iOS" width="420">

*Demonstração em simulador com contatos fictícios (interface em inglês, não é uma captura localizada em português; capturada em 2026-11-03). As telas, o layout e os textos podem variar de acordo com a versão instalada do app ou a versão do iOS.*

## Principais limites de segurança

- **`Ready to merge` vs. `Needs review`**:
  - `Ready to merge` (prontos para mesclar) significa que cada par de contatos do grupo passou por verificações rigorosas de correspondência com base em evidências fortes entre todos os pares. Mesmo assim, sempre confira a pré-visualização antes de confirmar — ter o mesmo nome ou número de telefone, por si só, não prova que dois cartões pertencem à mesma pessoa.
  - `Needs review` (requer revisão) indica evidências mais fracas ou conflitantes (como um telefone residencial compartilhado pela família, nomes diferentes, datas de aniversário conflitantes ou sobreposição parcial). Trata-se de uma proteção de segurança, e não de um erro; inspecione cada grupo em `Needs review` manualmente, um de cada vez (eles não podem entrar na mesclagem em lote do Pro), e nunca mescle cartões que representem pessoas diferentes.
- **Verifique e salve as Notas no app Contatos da Apple antes de mesclar**:
  - As Notas em contatos não principais (os outros cartões que serão mesclados) **não** são lidas nem copiadas para o contato principal, e não podem ser restauradas posteriormente.
  - Como o ContactMerge+ Cleaner não consegue ler Notas, nunca presuma que um contato não tem Notas só porque nenhuma aparece na pré-visualização da mesclagem. Inspecione e copie as Notas importantes diretamente no app **Contatos** da Apple antes de mesclar; se você visualizar ou editar contatos lá, retorne ao ContactMerge+ Cleaner e verifique novamente os candidatos duplicados atuais e a pré-visualização antes de confirmar (não presuma que telas abertas se atualizam automaticamente).
- **Desfazer e recuperação local no dispositivo**:
  - `Undo Last Contact Merge` (desfazer a última mesclagem de contatos) atua apenas sobre a única mesclagem mais recente (veja [Backup, Desfazer e Histórico de recuperação](../pt-BR/recovery.md) para consultar a localização verificada na tela do simulador e os avisos sobre versões).
  - `Recovery History` (histórico de recuperação) é um registro de recuperação local salvo pelo app que mantém **no máximo 3 registros de mesclagem e no máximo 3 registros de exclusão** por **cerca de 30 dias no dispositivo** (seu caminho exato de navegação dentro do app não é verificado nesta documentação; consulte [Backup, Desfazer e Histórico de recuperação](../pt-BR/recovery.md)).
  - **Não é uma restauração completa do sistema**: As Notas de cartões não principais não podem ser restauradas, e os identificadores e vínculos originais do sistema podem não ser restaurados. O desenvolvedor não oferece um serviço de backup na nuvem (isso é separado da sua própria sincronização do iCloud/Google ou dos backups do sistema iOS, portanto as mesclagens podem ser sincronizadas nas suas contas). Como precaução conservadora, a recuperação não é garantida após edições posteriores nos contatos, desinstalação do app ou perda do dispositivo.
- **Backup independente e segurança das contas**: Exportar um arquivo `.vcf` é opcional, mas recomenda-se manter um backup independente e datado que cubra suas contas reais de contatos antes da primeira limpeza (a sincronização de contas não equivale a um backup independente). Nunca exclua contatos de origem, não toque em `"Delete from My iPhone"` nem desative/remova contas como tentativa de solução de problemas.

## Grátis (Free) vs. Pro

- **Free**: Escaneie seus contatos, visualize todos os grupos de duplicados e mescle um grupo de duplicados por vez (com até 3 contatos dentro desse grupo). A mesclagem em lote de vários grupos não está incluída.
- **Pro**: Desbloqueio por compra única na App Store, sem assinatura; o preço regional é exibido diretamente pela Apple. Desbloqueia grupos com mais de 3 contatos e a mesclagem em lote para grupos `Ready to merge` após confirmação (os grupos `Needs review` são sempre revisados individualmente, um por vez).
- **Restauração de compra e cobrança**: Para restaurar uma compra Pro existente na mesma Conta Apple (Apple Account) ou entender o processo de reembolso da Apple (a Apple decide a elegibilidade conforme o país ou a região, e as solicitações usam o processo oficial da Apple em [reportaproblem.apple.com (em inglês)](https://reportaproblem.apple.com); a elegibilidade não é garantida e o desenvolvedor não pode garantir a aprovação), consulte o [FAQ](../pt-BR/faq.md#q16) ou entre em contato com o [Suporte oficial (em inglês)](https://contactmerge.app/support).

## Guias de operação

- [Início rápido: escaneando e mesclando com segurança](../pt-BR/quick-start.md)
- [Backup, Desfazer e Histórico de recuperação](../pt-BR/recovery.md)
- [Permissões e solução de problemas](../pt-BR/permissions-troubleshooting.md)
- [Perguntas frequentes (FAQ)](../pt-BR/faq.md)

## Suporte oficial e privacidade

- **Suporte**: [Suporte oficial (em inglês)](https://contactmerge.app/support)
- **Privacidade**: [Política de Privacidade (em inglês)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)
- **Aviso de privacidade e ocultação de dados**: Nunca compartilhe listas privadas de contatos, arquivos `.vcf` (vCard), senhas, dados de pagamento ou comprovantes de compra em relatos públicos (Issues). Oculte todos os nomes reais, números de telefone, endereços de e-mail, fotos, endereços residenciais, notas e IDs de conta antes de enviar qualquer captura de tela — use dados fictícios de demonstração sempre que possível.

## Status da documentação

Verificado em 8 de novembro de 2026. As telas, os rótulos e o comportamento podem variar dependendo da versão instalada do app e da versão do iOS.

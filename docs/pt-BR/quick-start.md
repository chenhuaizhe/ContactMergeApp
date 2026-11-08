# Início rápido: escaneando e mesclando com segurança

- **Visão geral e idiomas**: [Visão geral em português (Brasil)](../readme/README.pt-BR.md) | [English Overview](../../README.md)
- **Guias**: **Início rápido** | [Backup e recuperação](recovery.md) | [Permissões e solução de problemas](permissions-troubleshooting.md) | [FAQ](faq.md)
- **Idioma / Language**: **Português (Brasil)** | [English](../en/quick-start.md)

Este guia mostra como encontrar, verificar e mesclar contatos duplicados no seu iPhone usando o **ContactMerge+ Cleaner**.

O ContactMerge+ Cleaner processa seus contatos localmente no dispositivo, não envia sua agenda para servidores do desenvolvedor e não oferece um serviço de backup na nuvem do desenvolvedor. (A sincronização de contatos do iOS ou de contas — como iCloud ou Google — e os backups do sistema ou do dispositivo são mecanismos separados, controlados pelas configurações da sua própria conta e do iOS.) Informações sobre o produto e downloads estão disponíveis no [Site oficial (em inglês)](https://contactmerge.app).

## Antes de começar

- **Crie um backup independente e datado (recomendado)**: Exportar um arquivo `.vcf` (vCard) é opcional (você não é obrigado a exportar um arquivo antes de mesclar), mas manter um backup independente e com data é fortemente recomendado, especialmente antes da sua primeira limpeza. Certifique-se de que o backup cubra as contas reais onde seus contatos estão armazenados e contenha os registros que você espera. A sincronização de contas (como iCloud ou Google) não é um backup independente, pois as mesclagens podem ser sincronizadas entre dispositivos conectados. Consulte [Backup, Desfazer e Histórico de recuperação](recovery.md) e [Backup Contacts Before Merge on iPhone (em inglês)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone).
- **Aguarde a conclusão de transferências e sincronizações iniciais**: Se você configurou recentemente um novo iPhone, usou o Migrar para iOS (Move to iOS) ou adicionou uma conta de e-mail ou nuvem, espere até que a sincronização em segundo plano termine antes de escanear e mesclar (aguardar evita alterações no meio da sincronização, embora não garanta por si só a remoção de duplicados já existentes).

## Passo a passo para mesclar contatos

1. **Conceda permissão aos Contatos**: Permita o acesso aos Contatos quando o iOS solicitar. Se nenhum aviso aparecer ou a visibilidade parecer incompleta, consulte [Permissões e solução de problemas](permissions-troubleshooting.md).
2. **Escaneie sua agenda**: Execute um escaneamento no ContactMerge+ Cleaner para visualizar os grupos candidatos de contatos duplicados.
3. **Abra um grupo e revise a pré-visualização**: Toque em um grupo de duplicados, inspecione a pré-visualização da mesclagem (`Merge Preview`) e escolha qual cartão de contato deve permanecer como contato principal (cartão base).
4. **Verifique as Notas no app Contatos da Apple e confira os campos antes de confirmar**:
   - Notas importantes em contatos não principais (os outros cartões que serão mesclados) **não** são lidas nem copiadas para o contato principal, e não podem ser restauradas depois.
   - **Verifique as Notas no app Contatos da Apple, e não na pré-visualização**: O ContactMerge+ Cleaner não consegue ler as Notas dos contatos. Nunca presuma que um contato não tem Notas apenas porque nenhuma aparece na pré-visualização do ContactMerge+ Cleaner — abra o app **Contatos** da Apple para inspecionar esses cartões e copiar quaisquer Notas importantes para o contato principal antes de mesclar.
   - **Verifique novamente após consultar ou editar fora do app**: Se você sair do ContactMerge+ Cleaner para visualizar ou editar contatos no app **Contatos** da Apple, volte em seguida e confira novamente os candidatos duplicados atuais e a pré-visualização da mesclagem antes de confirmar. Não presuma que uma lista de candidatos ou pré-visualização já aberta será atualizada ou reescaneada automaticamente.
   - **Confirme a identidade e os campos esperados**: Confirme a mesclagem somente quando os cartões pertencerem claramente à mesma pessoa na vida real e a pré-visualização mantiver os campos que você espera.

### Exemplo: resultados do escaneamento e pré-visualização da mesclagem

<img src="../../assets/scan-results-demo.png" alt="Demonstração em simulador com interface em inglês (não é uma captura localizada em português; capturada em 2026-11-03) dos resultados do escaneamento em Duplicate Contacts com contatos fictícios exibindo Undo Last Contact Merge, Ready to merge e Needs review; telas e textos podem variar conforme a versão do app ou do iOS" width="420">

*Resultados do escaneamento — Demonstração em simulador com contatos fictícios (interface em inglês, não é uma captura localizada em português; capturada em 2026-11-03). As telas, o layout e os textos podem variar de acordo com a versão instalada do app ou a versão do iOS.*

<img src="../../assets/merge-preview-demo.png" alt="Demonstração em simulador com interface em inglês (não é uma captura localizada em português; capturada em 2026-11-03) de Merge Preview com contatos fictícios exibindo motivos de correspondência, o aviso Check and preserve notes in Contacts e a seleção de contato principal, enquanto a segunda linha de contato fica abaixo da área visível de rolagem; telas e textos podem variar conforme a versão do app ou do iOS" width="420">

*Pré-visualização da mesclagem e seleção do contato principal — Demonstração em simulador com contatos fictícios (interface em inglês, não é uma captura localizada em português; capturada em 2026-11-03; a segunda linha de contato aparece abaixo da área visível de rolagem, de modo que os dois cartões não ficam visíveis ao mesmo tempo). As telas, o layout e os textos podem variar de acordo com a versão instalada do app ou a versão do iOS.*

## Entendendo as categorias: `Ready to merge` vs. `Needs review`

O ContactMerge+ Cleaner organiza os grupos candidatos de duplicados em duas seções com base nas evidências de correspondência disponíveis (esta documentação descreve práticas seguras de revisão, sem afirmar limites internos exatos de execução ou regras exatas de normalização):

- **`Ready to merge` (prontos para mesclar)**:
  - Cada par de contatos no grupo passou por verificações rigorosas de correspondência com base em evidências fortes entre todos os pares.
  - **A revisão da pré-visualização continua indispensável**: Compartilhar nome ou número de telefone, por si só, não prova que dois cartões representam a mesma pessoa. Sempre inspecione a pré-visualização e verifique o app **Contatos** da Apple em busca de Notas antes de confirmar.
  - Elegível para a mesclagem em lote do Pro após sua confirmação.
- **`Needs review` (requer revisão)**:
  - Os cartões apresentam evidências mais fracas ou conflitantes — por exemplo, um telefone compartilhado da casa ou do trabalho, variações de nome, datas de aniversário conflitantes ou sobreposição parcial.
  - Ver `Needs review` é uma proteção conservadora, e não um erro de escaneamento: diferenças de nome não significam automaticamente duas pessoas distintas, enquanto números compartilhados ou nomes iguais ainda podem pertencer a familiares ou colegas de trabalho diferentes.
  - Deve ser inspecionado e confirmado manualmente, um grupo por vez. Os grupos em `Needs review` nunca são incluídos na mesclagem em lote do Pro, e não há opção para forçar grupos ambíguos na mesclagem em lote. Se dois cartões representarem pessoas diferentes, deixe-os sem mesclar.

## Recursos da versão Grátis (Free) vs. Pro

- **Free**:
  - Escaneie e visualize todos os grupos de duplicados detectados.
  - Mescle um grupo de duplicados por vez, com até 3 contatos dentro desse grupo (a mesclagem em lote de vários grupos não está incluída).
- **Pro**:
  - Desbloqueio por compra única na App Store, sem assinatura; a Apple exibe o preço regional correspondente à sua loja.
  - Desbloqueia a mesclagem de grupos com mais de 3 contatos e a mesclagem em lote para grupos `Ready to merge` após confirmação (os grupos em `Needs review` continuam exigindo revisão manual, um de cada vez).
  - Nenhuma das versões promete velocidades específicas de escaneamento nem capacidade ilimitada de lista de contatos.
  - Para restauração de compras ou informações sobre o processo de reembolso da Apple, consulte o [FAQ](faq.md#q15) ou entre em contato com o [Suporte oficial (em inglês)](https://contactmerge.app/support).

## Guias relacionados e suporte

- [Backup, Desfazer e Histórico de recuperação](recovery.md)
- [Permissões e solução de problemas](permissions-troubleshooting.md)
- [Perguntas frequentes (FAQ)](faq.md)
- [How to Merge Contacts Safely (em inglês)](https://contactmerge.app/guides/merge-contacts-safely)
- [Backup Contacts Before Merge on iPhone (em inglês)](https://contactmerge.app/guides/backup-contacts-before-merge-iphone)
- [Suporte oficial (em inglês)](https://contactmerge.app/support)
- [Política de Privacidade (em inglês)](https://github.com/chenhuaizhe/ContactMergeApp/blob/main/privacy-policy.md)

## Status da documentação

Verificado em 8 de novembro de 2026. As telas, os rótulos e o comportamento podem variar dependendo da versão instalada do app e da versão do iOS.

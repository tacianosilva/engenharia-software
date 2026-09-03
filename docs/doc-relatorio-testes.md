**Relatório de Testes de Módulo/Sistema**  
Responsabilidade do Testador

**Legenda**

**Teste** : Código ou identificação do Teste.  
**Descrição**: Descrição dos passos e detalhes do teste a ser executado.  
**Especificação**: Informações sobre a função testada e se ela de acordo com a especificação do caso de uso.  
**Resultado**: Resultado do teste, modificações sugeridas ou resultados do teste. No caso de erro ou problema na execução do teste descrever o erro em detalhes e adicionar print's das telas.

**US001 – Manter Produto**

| Teste | Descrição | Especificação | Resultado |
| :---- | :---- | :---- | :---- |
| Teste 01: Incluir Produto | A1 \- Incluir Produto		 A1.1. O ator preenche os dados; 			 A1.2. O ator seleciona a opção Cadastrar; 			 A1.3. O sistema salva os dados; 			 A1.4. O sistema exibe uma mensagem de acordo com a \[MSG001\]; A1.5. Fim do fluxo. | A função implementada não segue os passos A1.4. A implementação não está de acordo com a especificação do User Story. 		 | O produto é inserido, contudo a mensagem \[MSG001\] não foi exibida. 		 |
| Teste 02: Excluir Produto | A3 – Excluir Produto 	 A3.1 \- O ator executa o fluxo de Listar Produtos 			 A3.2 \- O ator seleciona o Produto e os dados referentes ao mesmo, são carregados na tela; A3.3 – O ator clica no botão Excluir; 	 A3.3 \- O sistema solicita confirmação para exclusão \[MSG05\]; 			 A3.4 \- O ator confirma a exclusão; 			 A3.5 \- O sistema exclui o registro e exibe uma mensagem de acordo com a 	\[MSG03\]; (E2). 			 A3.6 – Fim do fluxo. (P2) | Especificação OK.	 | OK. |
| Teste 03: Alterar Produto | A2 – Alterar Produto 			 A2.1 \- O ator executa o 			fluxo. (A4) 			 A2.2 \- O ator seleciona o Produto e os dados referentes ao mesmo, são carregados no campos para edição; 			 A2.3 \- O ator edita os campos e clica no botão Editar; 			 A2.4 \- O sistema salva os 	dados alterados no banco de dados; 			 A2.5 \- O sistema exibe uma mensagem de acordo com a \[MSG04\]. 			 A2.6 \- Fim do fluxo. (P2) | A função não implementa o passo A2.4, ou seja não altera o Produto. Na execução da função aparece uma mensagem sobre a regra de negócio RN001 que não aparece na especificação. | O Produto não é alterado mesmo preenchendo e seguindo todos os passos. Não é apresentada nenhuma mensagem de erro referente a alteração. 		 Ao tentar alterar um produto que tem compras (RN001) é exibida a mensagem MSG002. 			“Produto não pode ser alterado”. |

**Relatório de Bugs e Providências**  
Responsabilidade do Gerente

| Teste | Providência | Tarefas/Tipo |
| :---- | :---- | :---- |
| Teste 01 – Incluir Produto | Corrigir a implementação do fluxo do user story.	 | Tarefa: Bug de Implementação. |
| Teste 03 – Alterar Produto | Corrigir a especificação do fluxo do US e sua implementação. | Tarefa: Corrigir a análise do US.  Tarefa: Bug de Implementação. |


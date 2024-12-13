# Código Limpo: Diretrizes e Boas Práticas - Na minha opinião

Código é limpo quando pode ser facilmente compreendido por qualque pessoal independendi da senioridade dela. 
Com a compreensão vêm a legibilidade, capacidade de mudança, extensibilidade e manutenibilidade.

## Regras Gerais
- Sempre comente seu codigo e idente-o.
- Mantenha a simplicidade. O simples é sempre melhor. Reduza a complexidade sempre.
- Deixe o ambiente mais limpo do que o encontrou.
- Sempre encontre a causa raiz.

## Regras de Design
- Mantenha dados configuráveis em níveis altos.
- Prefira `switch/case` ao invés de `if/else`.
- Separe o código relacionado a multi-threading.
- Evite configurações excessivas.
- Utilize injeção de dependência sempre que julgar necessario.
- Siga a **Lei de Deméter**: uma classe deve conhecer apenas suas dependências diretas.

## Dicas de Compreensibilidade
- Seja consistente. Se algo é feito de uma maneira específica, aplique o mesmo padrão a casos semelhantes.
- Use variáveis explicativas.
- Encapsule condições de fronteira. Estas condições são difíceis de rastrear; concentre o processamento delas em um único local.
- Prefira objetos de valor dedicados a tipos primitivos.
- Evite dependências lógicas. Não escreva métodos que funcionem corretamente apenas se algo específico ocorrer na mesma classe.
- Evite condicionais negativas.

## Regras para Nomes
- Escolha nomes descritivos e inequívocos.
- Faça distinções significativas.
- Use nomes pronunciáveis.
- Use nomes pesquisáveis.
- Substitua números "mágicos" por constantes nomeadas.
- Evite codificação nos nomes. Não adicione prefixos ou informações sobre tipos.

## Regras para Funções
- Mantenha funções pequenas.
- Realize apenas uma tarefa por função.
- Use nomes descritivos.
- Prefira um número reduzido de argumentos.
- Evite efeitos colaterais.
- Não use argumentos de controle. Divida o método em várias funções independentes que possam ser chamadas sem depender de um argumento.

## Regras para Comentários
- Explique-se diretamente no código sempre que possível.
- Não seja redundante.
- Não adicione ruídos óbvios.
- Não use comentários em chaves de fechamento.
- Não comente código inativo. Remova-o.
- Utilize comentários para explicar a intenção.
- Use para clarificar trechos complexos do código.
- Utilize para alertar sobre possíveis consequências.

## Estrutura do Código Fonte
- Separe conceitos verticalmente.
- Código relacionado deve aparecer próximo e de forma densa verticalmente.
- Declare variáveis próximas ao local de uso.
- Funções dependentes devem estar próximas.
- Funções semelhantes devem estar próximas.
- Coloque funções em direção descendente no arquivo.
- Mantenha linhas curtas.
- Não use alinhamento horizontal.
- Use espaços em branco para associar elementos relacionados e separar elementos menos relacionados.
- Não quebre a indentação.

## Objetos e Estruturas de Dados
- Oculte a estrutura interna.
- Prefira estruturas de dados.
- Evite estruturas híbridas (meio objeto, meio dados).
- Mantenha objetos pequenos.
- Realize apenas uma tarefa por objeto.
- Utilize um número reduzido de variáveis de instância.
- Classes base não devem conhecer detalhes de suas derivadas.
- É melhor ter várias funções pequenas do que passar código para uma função decidir o comportamento.
- Prefira métodos não estáticos a métodos estáticos.

## Testes
- Um `assert` por teste.
- Leitura clara.
- Rápidos.
- Independentes.
- Repetíveis.

## Maus Odores no Código
- **Rigidez**: O software é difícil de modificar. Uma pequena mudança causa uma cascata de alterações.
- **Fragilidade**: O software quebra em diversos locais devido a uma única alteração.
- **Imobilidade**: Não é possível reutilizar partes do código em outros projetos devido aos riscos e ao esforço elevado.
- Complexidade desnecessária.
- Repetição desnecessária.
- **Opacidade**: O código é difícil de entender.

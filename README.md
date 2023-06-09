# 120-respostas-frontend

Esse repositório tem como finalidade responder as 120 questões que estão disponiveis no seguinte repositório: https://github.com/rubenmarcus/120-perguntas-frontend

IMPORTANTE: Essas Perguntas/Respostas tem o intuito de ser uma base para entrevistas e candidatos se nivelarem, em entrevistas de emprego. Não são necessariamente o fator decisivo da senioridade de cada candidato, outros fatores como experiência em projetos, em liderança, documentação, saber caso de uso de tecnologia e conceitos, as vezes pode contar muito mais do que saber decor respostas para perguntas.

## Junior

#### 1. O que é SQL injection?

SQL injection é um tipo de ataque que explorar vulnerabilidades em aplicativos web que usam SQL (Structured Query Language) para se comunicar com um banco de dados. Basicamente, o ataque ocorre quando um invasor manipula intencionalmente as entradas de um formulário da web para inserir código SQL malicioso que pode ser executado no banco de dados subjacente.

Em outras palavras, o ataque de injeção SQL ocorre quando um invasor usa uma entrada de dados mal-intencionada para enganar um aplicativo web a enviar comandos SQL que podem permitir que o invasor acesse, modifique ou exclua dados armazenados no banco de dados. Esse tipo de ataque pode ser muito prejudicial, pois pode resultar em roubo de informações confidenciais, perda de dados, corrupção de dados ou danos ao banco de dados.

Para evitar ataques de injeção SQL, é importante implementar boas práticas de segurança, como a validação rigorosa de entradas do usuário, uso de parâmetros de consulta parametrizados, limitação de privilégios de acesso ao banco de dados e monitoramento regular do sistema em busca de atividades suspeitas.

#### 2. O que é escopo em JavaScript?

Escopo em JavaScript se refere à visibilidade e acessibilidade de variáveis, funções e objetos em diferentes partes do código. Em outras palavras, é o contexto em que uma variável ou função é declarada e onde ela pode ser usada.

Existem dois tipos principais de escopos em JavaScript: escopo global e escopo local.

O escopo global é aquele que se aplica a todo o código e qualquer variável ou função declarada fora de qualquer função é definida no escopo global.

Já o escopo local é aquele que se aplica a um bloco de código limitado, geralmente dentro de uma função. Qualquer variável ou função declarada dentro de um bloco de código dentro de uma função é definida dentro do escopo local daquela função e só pode ser acessada dentro dessa função.

Quando você faz referência a uma variável em um programa JavaScript, o interpretador do JavaScript procura primeiro no escopo local da função atual e, se não encontrar a variável lá, ele procura no escopo global. Se a variável não for encontrada em nenhum dos escopos, ocorrerá um erro.

É importante ter uma compreensão clara do escopo em JavaScript, pois isso pode afetar a forma como você declara e usa variáveis e funções em seu código, além de ajudar a evitar problemas de conflito de nomes e outros erros comuns.

#### 3. Explique o CSS “box model” e os componentes de layout que o compõem.

O modelo de caixa (box model) é um conceito fundamental do CSS que descreve como os elementos HTML são renderizados como caixas retangulares em uma página web. O modelo de caixa é composto de quatro componentes principais:

- Conteúdo (Content): é o próprio conteúdo HTML do elemento, como o texto ou imagem.
- Padding: é uma área transparente ao redor do conteúdo. O padding é usado para criar espaço entre o conteúdo e a borda da caixa.
- Border: é uma linha que circunda a caixa. A borda é usada para separar visualmente um elemento de seus vizinhos.
- Margin: é uma área transparente ao redor da borda. O margin é usado para criar espaço entre as caixas e é usado para controlar a distribuição do layout.
- Cada um desses componentes afeta o tamanho total da caixa, que é a soma do conteúdo, do padding, da borda e do margin. A ordem em que esses componentes são aplicados é importante, pois afeta a aparência visual do elemento na página.

Por exemplo, se você definir o tamanho de uma caixa usando a propriedade width, o tamanho total da caixa será afetado pelo padding e pela borda. Se você quiser que o tamanho da caixa inclua o padding e a borda, você pode usar a propriedade box-sizing e definir seu valor como border-box.

É importante entender o modelo de caixa do CSS para criar layouts eficazes e bem estruturados em uma página web. Ele permite que você controle como o espaço é distribuído entre os elementos da página e ajuda a garantir que o layout seja consistente e previsível em diferentes dispositivos e navegadores.

#### 4. Como JavaScript e jQuery são diferentes?

JavaScript e jQuery são duas ferramentas diferentes, mas que estão relacionadas. JavaScript é uma linguagem de programação amplamente usada para desenvolver aplicativos da web, enquanto jQuery é uma biblioteca de JavaScript que fornece uma série de funcionalidades para simplificar o desenvolvimento de aplicativos web.

JavaScript é uma linguagem de programação de script que pode ser usada em vários contextos, desde aplicativos da web até desenvolvimento de jogos, automação de planilhas, aplicativos móveis e muito mais. É uma linguagem flexível que pode ser usada em conjunto com outras ferramentas e bibliotecas para criar aplicativos da web altamente interativos.

jQuery, por sua vez, é uma biblioteca de JavaScript que simplifica a seleção de elementos HTML em uma página web e permite que você manipule esses elementos de forma fácil e eficiente. Ele inclui um conjunto de funções que permitem adicionar, remover ou modificar elementos HTML, manipular eventos do usuário, criar animações e muito mais.

Embora o JavaScript possa fazer muitas coisas que o jQuery faz, o jQuery é mais fácil de usar em muitas situações, pois possui uma sintaxe simplificada que é mais fácil de entender. O jQuery também é otimizado para funcionar em diferentes navegadores e sistemas operacionais, o que significa que você pode criar aplicativos da web que funcionem em diferentes dispositivos e plataformas com mais facilidade.

#### 5. O que é é um Callback Hell?

Callback Hell, também conhecido como Pyramid of Doom, é um termo usado para descrever um padrão de programação em que há uma grande quantidade de callbacks aninhados uns dentro dos outros em uma função JavaScript. Esse padrão ocorre quando um código assíncrono é executado em sequência, com cada etapa dependendo do resultado da etapa anterior.

Por exemplo, imagine que você precisa carregar uma lista de usuários de um servidor e, em seguida, carregar as informações de cada usuário individualmente. Para fazer isso usando callbacks, você teria que fazer várias chamadas aninhadas, o que pode levar a um código confuso e difícil de ler e manter.

Exemplo de Callback Hell:

```
loadUsers(function(users) {
  loadUserInfo(users[0], function(userInfo) {
    showUserInfo(userInfo);
    loadUserInfo(users[1], function(userInfo) {
      showUserInfo(userInfo);
      loadUserInfo(users[2], function(userInfo) {
        showUserInfo(userInfo);
        // ... e assim por diante
      });
    });
  });
});
```

Este exemplo mostra como o Callback Hell pode se tornar rapidamente confuso e difícil de seguir. Cada função de callback é aninhada em outra, resultando em um código com várias camadas de indentação, o que torna difícil de ler e depurar.

Existem maneiras de evitar o Callback Hell, como usar Promises, Async/await e outras técnicas de programação assíncrona. O uso dessas técnicas pode tornar o código mais legível, mais fácil de entender e manter.

#### 6. O que é Cross-Site Scripting (XSS)?

Cross-Site Scripting (XSS) é um tipo de vulnerabilidade de segurança da web que permite que um atacante injete código malicioso em uma página da web visualizada por outros usuários. Isso geralmente é feito inserindo código de script em um campo de entrada, como uma caixa de pesquisa ou formulário de comentário, que é armazenado no banco de dados do aplicativo da web e exibido para outros usuários que visitam a página.

O código malicioso pode ser usado para roubar informações do usuário, como senhas, cookies ou outras informações confidenciais, ou pode ser usado para redirecionar o usuário para um site malicioso, instalar malware em seu dispositivo ou executar outras ações maliciosas.

Existem dois tipos de XSS:

- Reflected XSS - Neste tipo de ataque, o código malicioso é injetado em uma página da web como parte de uma solicitação HTTP, como uma consulta de pesquisa. O servidor web retorna a página com o código malicioso, que é executado no navegador do usuário, permitindo que o atacante execute ações maliciosas.
- Stored XSS - Neste tipo de ataque, o código malicioso é injetado em uma página da web e armazenado no banco de dados do aplicativo da web. Quando outros usuários acessam a página, o código malicioso é executado em seus navegadores, permitindo que o atacante execute ações maliciosas.

Para evitar ataques XSS, os desenvolvedores de aplicativos da web devem validar e filtrar todos os dados de entrada, especialmente campos de formulário, antes de armazená-los em um banco de dados ou exibi-los para outros usuários. Os navegadores modernos também fornecem proteções contra XSS, como a execução automática do código malicioso ou a exibição de avisos ao usuário.

#### 7. O que é Flux?

Flux é uma arquitetura de aplicativo de front-end criada pelo Facebook para lidar com os desafios de gerenciamento de estado em aplicativos de grande escala. A arquitetura Flux é uma variação do padrão de arquitetura MVC (Model-View-Controller) e enfatiza o gerenciamento unidirecional de dados em um aplicativo.

Na arquitetura Flux, os dados fluem em uma única direção através de um pipeline claro de etapas: ação, despacho, loja e visualização. Aqui está uma visão geral de cada uma dessas etapas:

- `Action`: As `actions` são objetos que contêm informações sobre as mudanças que ocorrem em seu aplicativo. As `actions` são geradas pelos usuários (por exemplo, um usuário pode clicar em um botão) ou por outras partes do seu aplicativo.
- `Dispatcher`: Quando uma `Action` é gerada, ela é enviada ao `Dispatcher` Flux, que é responsável por garantir que todas as `stores` Flux sejam atualizadas com as informações da `action`. O `dispatcher` Flux garante que todas as `stores` Flux recebam a ação na ordem correta e que as alterações sejam propagadas em todo o aplicativo.
- `Store`: A `Store` Flux é responsável por manter o estado do aplicativo. A `Store` Flux recebe as ações do `dispatcher` Flux e atualiza seu estado em conformidade. A `Store` Flux, em seguida, emite um evento que notifica a `view` de que o estado mudou.
- `View`: A `view` é responsável por renderizar a interface do usuário com base no estado do aplicativo. A `view` recebe atualizações da `Store` Flux sempre que o estado do aplicativo muda e é responsável por exibir as informações ao usuário.

Ao utilizar a arquitetura Flux, os desenvolvedores podem criar aplicativos de front-end escaláveis e fáceis de manter, mantendo o gerenciamento de estado consistente e previsível. Flux é uma arquitetura flexível e pode ser implementada em várias bibliotecas e frameworks JavaScript, como React e Angular.

#### 8. O que é Sass?

Sass (Syntactically Awesome Style Sheets) é uma linguagem de extensão do CSS que adiciona funcionalidades adicionais, como variáveis, aninhamento de seletores, mixins e operações matemáticas. Ele foi criado para tornar a escrita de estilos CSS mais fácil, modular e eficiente.

Com Sass, os desenvolvedores podem definir variáveis para valores CSS que são usados ​​em todo o documento, reduzindo a repetição de código e facilitando a atualização de estilos em todo o site. O aninhamento de seletores permite que os desenvolvedores agrupem seletores relacionados em um bloco de código, tornando o CSS mais fácil de entender e manter. Os mixins são blocos de código reutilizáveis ​​que podem ser chamados em qualquer lugar do documento, ajudando a reduzir a repetição de código e a simplificar a manutenção. As operações matemáticas permitem que os desenvolvedores realizem cálculos simples no CSS, como adicionar ou subtrair valores, o que pode ajudar a criar layouts mais dinâmicos e responsivos.

Sass é compilado em CSS para que possa ser usado em navegadores da web. Existem duas sintaxes para escrever em Sass: a sintaxe original, chamada "Sass", que usa indentação em vez de chaves para separar blocos de código, e a sintaxe mais recente, chamada "SCSS", que se parece mais com a sintaxe do CSS tradicional. Sass pode ser usado com várias ferramentas de compilação, como Gulp, Grunt, Webpack e outras.

Em resumo, Sass é uma linguagem de folha de estilos CSS que adiciona funcionalidades adicionais e recursos que podem ajudar a tornar a escrita de estilos CSS mais eficiente e modular.

#### 9. O que é encapsulamento?

Encapsulamento é um conceito importante em programação orientada a objetos (POO) que se refere à prática de ocultar o estado interno de um objeto e expor apenas a interface pública para interagir com ele. Em outras palavras, o encapsulamento é o processo de "encapsular" ou "empacotar" dados e comportamentos relacionados em uma única unidade, geralmente chamada de classe.

O encapsulamento permite que os desenvolvedores ocultem os detalhes internos de uma classe ou objeto de outras partes do código, reduzindo assim a complexidade do sistema e facilitando a manutenção. Ao expor apenas uma interface pública bem definida, os desenvolvedores podem controlar como os usuários de uma classe ou objeto podem acessar e modificar seus dados internos.

Além disso, o encapsulamento também ajuda a garantir a integridade dos dados em um objeto ou classe, tornando mais difícil para outros partes do código modificarem o estado interno de um objeto de forma inadequada. Isso ajuda a garantir que o objeto ou classe funcione corretamente e evita que bugs e erros ocorram.

Em resumo, encapsulamento é um conceito-chave da POO que se refere a ocultar o estado interno de um objeto e expor apenas uma interface pública para interagir com ele. O encapsulamento ajuda a reduzir a complexidade do sistema, facilitar a manutenção e garantir a integridade dos dados em um objeto ou classe.

#### 10. Qual o ponto de se usar Redux?

Redux é uma biblioteca de gerenciamento de estado previsível e fácil de usar, frequentemente usada com bibliotecas como React para construir aplicativos de página única (SPA). O ponto principal de se usar Redux é separar a lógica de gerenciamento de estado do restante do aplicativo. Isso ajuda a simplificar o código e tornar o aplicativo mais fácil de entender, manter e testar.

Algumas razões pelas quais os desenvolvedores podem escolher usar Redux em seus aplicativos incluem:

- 1. Gerenciamento de estado centralizado: O Redux fornece um armazenamento centralizado para todos os dados do aplicativo. Isso ajuda a manter o estado do aplicativo organizado e fácil de acessar e gerenciar.
- 2. Previsibilidade do estado: O Redux segue um padrão de fluxo unidirecional de dados, o que significa que o estado do aplicativo só pode ser atualizado através de ações previsíveis e imutáveis. Isso torna o estado do aplicativo mais fácil de prever e depurar.
- 3. Facilidade de depuração: Como o estado do aplicativo é mantido em um local centralizado, o Redux permite que os desenvolvedores monitorem e depurem o estado do aplicativo com mais facilidade.
- 4. Escalabilidade: O Redux é altamente escalável e pode ser facilmente integrado com outras bibliotecas e ferramentas. Isso torna mais fácil para os desenvolvedores construir aplicativos maiores e mais complexos.

Em resumo, o Redux é usado para gerenciar o estado do aplicativo em um local centralizado e previsível, o que torna o código mais fácil de entender, manter e depurar. Ele também oferece escalabilidade e integração fácil com outras bibliotecas e ferramentas.

#### 11. Explique a diferença de null e undefined em JavaScript

Em JavaScript, `null` e `undefined` são dois valores primitivos especiais que indicam a ausência de valor. No entanto, eles têm algumas diferenças importantes:

- `undefined` é um valor primitivo que é atribuído automaticamente a uma variável quando ela é declarada, mas não inicializada com um valor. Também é o valor retornado quando se tenta acessar uma propriedade de objeto ou variável que não existe. É importante notar que `undefined` é diferente de uma variável que não está definida, que lança um erro de referência.
- `null` é um valor primitivo que representa a ausência intencional de valor. É geralmente usado para indicar que uma variável ou propriedade de objeto não possui valor ou deve ser redefinida para um valor vazio.

A principal diferença entre os dois é que `undefined` é atribuído automaticamente pelo JavaScript, enquanto `null` é um valor que deve ser definido explicitamente pelo desenvolvedor. Em outras palavras, `undefined` é uma falta de valor devido a um erro ou falta de inicialização, enquanto `null` é uma intencional falta de valor.

Além disso, `undefined` é geralmente usado como um sinal de que algo não está definido ou não está acessível, enquanto `null` é usado para indicar que algo intencionalmente não tem valor.

#### 12. Liste as vantagens da arquitetura de microsserviços

A arquitetura de microsserviços é uma abordagem de desenvolvimento de software em que um aplicativo é dividido em um conjunto de serviços independentes e pequenos, cada um executando seu próprio processo e se comunicando com outros serviços por meio de uma interface bem definida. Algumas das principais vantagens da arquitetura de microsserviços incluem:

- 1. Escalabilidade: A arquitetura de microsserviços permite que cada serviço seja dimensionado independentemente, o que significa que a capacidade de processamento de um serviço pode ser facilmente ajustada para atender a demanda do aplicativo.
- 2. Resiliência: Com a arquitetura de microsserviços, falhas em um serviço não afetam todo o aplicativo. Isso torna o aplicativo mais resistente a falhas e mais fácil de manter em execução.
- 3. Desenvolvimento independente: Como cada serviço é independente, é possível que equipes diferentes desenvolvam serviços diferentes ao mesmo tempo, sem afetar o desenvolvimento de outros serviços.
- 4. Facilidade de implantação: A implantação de microsserviços é geralmente mais fácil do que a implantação de um aplicativo monolítico. Isso ocorre porque cada serviço pode ser implantado e atualizado independentemente, sem afetar os outros serviços.
- 5. Flexibilidade tecnológica: Com a arquitetura de microsserviços, é possível usar diferentes tecnologias e linguagens de programação para cada serviço, dependendo dos requisitos específicos.
- 6. Facilidade de manutenção: Como cada serviço é independente, a manutenção e atualização de um serviço não afeta o restante do aplicativo. Isso torna o aplicativo mais fácil de manter e atualizar ao longo do tempo.
- 7. Menor acoplamento: A arquitetura de microsserviços promove um baixo acoplamento entre serviços, o que significa que as mudanças em um serviço não afetam outros serviços do aplicativo. Isso torna o aplicativo mais modular e mais fácil de escalar e manter.

#### 13. Quais são as vantagens do NoSQL sobre o RDBMS tradicional?` \

NoSQL ("Not Only SQL") é uma categoria de bancos de dados não relacionais que se diferenciam dos bancos de dados relacionais (RDBMS) tradicionais em vários aspectos. Algumas das principais vantagens do NoSQL sobre o RDBMS tradicional incluem:

- 1. Escalabilidade horizontal: O NoSQL foi projetado para dimensionar horizontalmente, ou seja, adicionar mais servidores para lidar com mais dados e mais solicitações. Isso permite que os aplicativos cresçam com mais facilidade e menos custo do que o RDBMS tradicional, que geralmente requer mais recursos para dimensionar verticalmente.
- 2. Flexibilidade de esquema: Os bancos de dados NoSQL geralmente não possuem um esquema rígido, o que significa que os dados podem ser adicionados sem a necessidade de modificar a estrutura do banco de dados. Isso torna mais fácil lidar com dados não estruturados ou semiestruturados, que não se encaixam facilmente em um esquema relacional.
- 3. Desempenho: O NoSQL é geralmente mais rápido do que o RDBMS tradicional para operações simples de leitura/gravação, especialmente quando há muitos registros e as consultas precisam ser executadas em várias tabelas em um banco de dados relacional.
- 4. Escalabilidade geográfica: Bancos de dados NoSQL são mais adequados para aplicativos distribuídos que podem ter usuários em diferentes locais geográficos. Bancos de dados NoSQL possuem recursos de replicação que permitem que os dados sejam replicados em diferentes regiões, tornando mais fácil lidar com altos níveis de tráfego.
- 5. Custo: NoSQL é frequentemente menos dispendioso do que o RDBMS tradicional para armazenamento de grandes volumes de dados, especialmente quando as empresas precisam lidar com grandes volumes de dados.

#### 14. O que é programação reativa?

Programação reativa é um paradigma de programação que se concentra na criação de sistemas que são altamente responsivos, resilientes e escaláveis. É baseado em uma abordagem declarativa para a programação de fluxos de dados assíncronos, onde os desenvolvedores definem como os dados fluem e são transformados em vez de programar explicitamente cada etapa.

Em um sistema reativo, os dados fluem por meio de fluxos de eventos assíncronos, e os componentes do sistema respondem a esses eventos de forma reativa, ou seja, automaticamente e imediatamente. Isso torna o sistema mais flexível, adaptável e tolerante a falhas.

Um exemplo comum de programação reativa é o uso de Observables, que são objetos que representam fluxos de dados e permitem que os desenvolvedores reajam a esses fluxos de forma assíncrona. Os Observables podem ser combinados e transformados em tempo real, permitindo a criação de sistemas altamente responsivos e escaláveis.

A programação reativa é especialmente útil para aplicativos que precisam lidar com grandes quantidades de dados, como aplicativos de streaming de mídia, aplicativos IoT e aplicativos de jogos em tempo real. No entanto, a programação reativa pode ser usada em qualquer aplicativo que precisa lidar com eventos assíncronos e responder a eles de forma rápida e eficiente.

#### 15. O que são os reducers no Redux?

Em Redux, reducers são funções puras responsáveis por atualizar o estado da aplicação em resposta a uma ação. Eles recebem como parâmetros o estado atual e a ação a ser executada, e retornam um novo estado que reflete as mudanças feitas pela ação.

Os reducers devem ser funções puras, ou seja, não podem ter efeitos colaterais e não podem modificar o estado diretamente. Em vez disso, eles devem criar uma cópia do estado atual e modificá-la para refletir as mudanças necessárias. Dessa forma, os reducers garantem que o estado da aplicação seja sempre previsível e consistente.

Os reducers são definidos usando a sintaxe switch/case, onde cada case representa uma ação específica e contém a lógica para atualizar o estado da aplicação para essa ação. Por exemplo:

```
function myReducer(state = initialState, action) {
  switch (action.type) {
    case 'INCREMENT':
      return {
        ...state,
        count: state.count + 1
      }
    case 'DECREMENT':
      return {
        ...state,
        count: state.count - 1
      }
    default:
      return state
  }
}
```

Neste exemplo, o reducer myReducer atualiza o estado da aplicação em resposta às ações 'INCREMENT' e 'DECREMENT', incrementando e decrementando o valor da propriedade count, respectivamente. O reducer também retorna o estado atual se a ação não for reconhecida.

Os reducers são uma parte fundamental do Redux e permitem que as mudanças no estado da aplicação sejam rastreadas de forma consistente e previsível.

#### 16. Qual o papel do HTML na indexação de páginas por buscadores?

O HTML desempenha um papel fundamental na indexação de páginas por buscadores, pois é o principal meio de comunicação entre o conteúdo da página e os mecanismos de busca.

Os buscadores usam bots, também conhecidos como spiders ou crawlers, para percorrer as páginas da web e indexar seu conteúdo. Esses bots seguem as ligações encontradas nas páginas e analisam o conteúdo, incluindo o HTML, para entender do que se trata a página e como ela deve ser classificada nos resultados de busca.

O HTML é usado para fornecer informações sobre o conteúdo da página, incluindo o título da página, cabeçalhos, parágrafos, listas, links e outras informações importantes. Os mecanismos de busca usam essas informações para determinar o assunto da página e classificá-la adequadamente nos resultados de busca.

Além disso, o HTML também pode ser usado para fornecer informações adicionais aos mecanismos de busca, como metadados, que descrevem o conteúdo da página de maneira mais detalhada e podem ajudar a melhorar a classificação nos resultados de busca.

Portanto, ao criar uma página da web, é importante usar HTML semântico e bem estruturado para que os mecanismos de busca possam entender e classificar adequadamente o conteúdo da página nos resultados de busca. Isso pode aumentar a visibilidade da página e atrair mais tráfego orgânico.

#### 17. Cite 3 conceitos da Programação Orientada a Objetos aplicada ao JavaScript

A Programação Orientada a Objetos (POO) é uma abordagem de programação que enfatiza a criação de objetos que possuem comportamentos e características. Aqui estão três conceitos da POO que podem ser aplicados ao JavaScript:

- Classes: As classes são uma maneira de definir objetos em POO. No JavaScript, as classes são definidas usando a palavra-chave class e podem ter propriedades e métodos. Os objetos são criados a partir dessas classes usando o operador new.
- Herança: A herança é um conceito em POO que permite que uma classe herde propriedades e métodos de outra classe. No JavaScript, a herança é implementada usando a palavra-chave extends. A classe que herda é chamada de subclasse e a classe que é herdada é chamada de superclasse.
- Polimorfismo: O polimorfismo é um conceito em POO que permite que objetos de diferentes classes sejam tratados de maneira semelhante. Isso é possível porque esses objetos implementam os mesmos métodos com a mesma assinatura. No JavaScript, o polimorfismo pode ser alcançado usando a herança e a sobrescrita de métodos na subclasse.

#### 18. Quais os beneficios do TypeScript?

TypeScript é um superset da linguagem JavaScript que adiciona recursos de tipagem estática, interfaces, classes e outros recursos de programação orientada a objetos à linguagem. Aqui estão alguns benefícios do TypeScript:

- 1. Tipagem estática: O TypeScript adiciona recursos de tipagem estática à linguagem, permitindo que o compilador verifique o tipo das variáveis em tempo de compilação. Isso pode ajudar a evitar erros de digitação, tornar o código mais legível e facilitar a manutenção do código.
- 2. Melhor suporte para programação orientada a objetos: O TypeScript adiciona recursos de programação orientada a objetos à linguagem JavaScript, como classes, interfaces, herança e polimorfismo. Isso torna mais fácil escrever e manter código em projetos maiores e mais complexos.
- 3. Maior escalabilidade: O TypeScript é altamente escalável e pode ser usado em projetos de grande porte. Ele oferece recursos avançados de modularidade, como namespaces e módulos, que ajudam a organizar e dividir o código em partes menores e mais gerenciáveis.
- 4. Melhor integração com ferramentas de desenvolvimento: O TypeScript é compatível com várias ferramentas de desenvolvimento, como IDEs, editores de código e depuradores. Ele oferece recursos avançados de edição de código, como o preenchimento automático de código, refatoração e detecção de erros em tempo real.
- 5. Maior compatibilidade: O TypeScript é compatível com JavaScript e pode ser usado em projetos que usam JavaScript existente. Ele também pode ser usado em vários ambientes, incluindo navegadores da web, Node.js e outros.

#### 19. O que é uma interface no TypeScript?

No TypeScript, uma interface é um recurso que permite definir um contrato ou um conjunto de regras que devem ser seguidas por um objeto. Ela define a estrutura dos dados que um objeto deve ter, mas não implementa nenhuma funcionalidade. A interface é um recurso de tempo de compilação e não é convertida em código JavaScript quando o código TypeScript é compilado.
As interfaces podem ser usadas para definir tipos personalizados e ajudar na validação de tipos em tempo de compilação. Elas são amplamente utilizadas em programação orientada a objetos e programação funcional.

Por exemplo, suponha que você esteja trabalhando em um projeto que envolve o processamento de vários tipos de dados, como números, strings e booleanos. Você pode definir uma interface para cada tipo de dado e, em seguida, usar essas interfaces para validar os dados recebidos pelo seu código. Se um objeto não seguir a estrutura definida pela interface, um erro será gerado em tempo de compilação.

Aqui está um exemplo de uma interface que define a estrutura de um objeto que contém informações de um usuário:

```
interface User {
  id: number;
  name: string;
  email: string;
}
```

Neste exemplo, a interface User define um objeto que deve ter uma propriedade id do tipo number, uma propriedade name do tipo string e uma propriedade email do tipo string. Você pode usar esta interface para validar objetos que seguem esta estrutura.

#### 20. Qual o significado de Mock?

Mock é um termo que se refere a um objeto simulado que substitui um objeto real em um teste de software. Em outras palavras, é uma réplica falsa de um objeto que pode ser usado para simular o comportamento do objeto real em diferentes cenários de teste.

Os objetos de Mock são usados em testes de unidade para isolar o código em teste de suas dependências externas, como banco de dados, serviços de rede ou bibliotecas de terceiros. Em vez de usar os objetos reais, que podem ser difíceis de configurar ou instáveis, os objetos de Mock são criados para imitar o comportamento desses objetos e fornecer valores predefinidos para os testes.

Por exemplo, em um teste de uma função que acessa um banco de dados, um objeto de Mock pode ser usado para simular o comportamento do banco de dados, em vez de usar o banco de dados real. Isso permite que o teste seja executado rapidamente e de forma isolada, sem depender da disponibilidade ou estabilidade do banco de dados real.

Os objetos de Mock também podem ser usados para testar a interação entre objetos e componentes de um sistema, como uma API REST. Em vez de chamar a API real, que pode ter um custo alto ou efeitos colaterais indesejados, um objeto de Mock pode ser usado para imitar o comportamento da API e fornecer respostas predefinidas para testar a interação entre o cliente e o servidor.

#### 21. O que é o esquema do GraphQL?` \

O esquema do GraphQL é uma definição da estrutura de dados que pode ser consultada e manipulada usando o GraphQL. É uma parte fundamental da linguagem GraphQL e fornece uma descrição clara e concisa dos tipos de dados, campos e relacionamentos disponíveis em um servidor GraphQL.

O esquema é usado para validar as consultas enviadas pelos clientes GraphQL e para fornecer uma documentação completa das operações e dados disponíveis em um servidor GraphQL. Ele define os tipos de dados disponíveis, como objetos, interfaces e enumerações, bem como os campos e argumentos que podem ser usados em consultas.

O esquema do GraphQL também define as consultas, mutações e assinaturas que podem ser usadas para consultar e manipular os dados. Ele fornece uma estrutura consistente para definir operações e tipos de dados, permitindo que os desenvolvedores criem APIs mais flexíveis e fáceis de usar.

Além disso, o esquema do GraphQL é auto-documentado e pode ser consultado para obter informações completas sobre os tipos de dados, campos e operações disponíveis em um servidor GraphQL. Isso facilita a criação de ferramentas de desenvolvimento que podem ser usadas para explorar e testar as APIs GraphQL.

#### 22. O que é o Virtual DOM? Qual sua vantagem?

O Virtual DOM é uma representação virtual da estrutura do DOM (Document Object Model) em memória, usada por algumas bibliotecas e frameworks JavaScript, como React e Vue.js. Essa técnica envolve a criação de uma árvore de objetos JavaScript que representam a estrutura de elementos HTML e suas propriedades em vez de manipular diretamente o DOM real.

A principal vantagem do Virtual DOM é a eficiência na atualização e manipulação do DOM real. Como o DOM é uma estrutura complexa e pode levar muito tempo para atualizar, as bibliotecas e frameworks que usam o Virtual DOM podem aplicar atualizações apenas nas partes que foram alteradas, em vez de atualizar todo o DOM. Isso melhora significativamente o desempenho das aplicações em termos de velocidade e eficiência de renderização.

Outra vantagem é a facilidade de implementação do conceito de unidirecionalidade de dados (one-way data binding) em frameworks que utilizam o Virtual DOM, como o React. Com o Virtual DOM, é possível atualizar e renderizar componentes de forma simples e fácil, permitindo a criação de interfaces de usuário interativas e responsivas.

Além disso, o Virtual DOM também ajuda a separar a lógica de renderização da lógica de negócios da aplicação, tornando o código mais modular e fácil de manter. Isso permite que os desenvolvedores se concentrem mais na lógica de negócios e menos nas atualizações do DOM, tornando o processo de desenvolvimento mais eficiente e menos propenso a erros.

#### 23. O que é e como usar a convenção Block Element Modifier (BEM)?

A convenção Block Element Modifier (BEM) é uma metodologia de nomenclatura para classes de CSS que ajuda a criar estilos de forma consistente e escalável. O objetivo é nomear as classes de forma que sejam fáceis de entender, reutilizar e estender, reduzindo a complexidade do código CSS e melhorando a manutenção.

A convenção BEM utiliza três tipos de entidades:

- Block: É a entidade principal de uma seção da página HTML. Ele representa um componente autônomo e significativo. Um bloco é representado por um nome único em letras minúsculas, separadas por um traço, por exemplo: .menu.
- Element: São as partes do bloco que têm um significado dentro do contexto do bloco. São representados por um nome de classe que começa com o nome do bloco seguido de dois subtraços e o nome do elemento, por exemplo: .menu\_\_item.
- Modifier: São os estados diferentes que um bloco ou elemento pode ter. São representados por um nome de classe que começa com o nome do bloco ou elemento, seguido de dois subtraços e o nome do modificador, por exemplo: .menu--open ou .menu\_\_item--selected.

A estrutura de uma classe BEM geralmente segue o padrão: .block\_\_element--modifier, onde o bloco é obrigatório, o elemento e o modificador são opcionais.

O uso da convenção BEM ajuda a reduzir o acoplamento entre HTML e CSS, pois as classes são nomeadas de forma clara e autoexplicativa, tornando mais fácil para os desenvolvedores entenderem como cada componente se encaixa na estrutura geral do projeto. Além disso, torna mais fácil a manutenção do código, a criação de estilos escaláveis e reutilizáveis, bem como a correção de bugs.

#### 24. JavaScript: Explique como você pode usar funções JavaScript, como forEach, Map ou Reduce.

As funções forEach, map e reduce são importantes para trabalhar com arrays em JavaScript.

A função forEach é usada para iterar sobre um array e executar uma determinada função para cada elemento do array. Sua sintaxe é:

```
array.forEach(function(item, index, array) {
  // código a ser executado para cada elemento
});
```

Onde item é o elemento atual do array, index é a posição desse elemento no array e array é o próprio array. A função passada como parâmetro é executada para cada elemento do array.

A função map é usada para criar um novo array a partir de um array existente, aplicando uma função para cada elemento do array. Sua sintaxe é:

```
const novoArray = array.map(function(item, index, array) {
  // código a ser executado para cada elemento
  return novoItem;
});
```

Onde item é o elemento atual do array, index é a posição desse elemento no array e array é o próprio array. A função passada como parâmetro é executada para cada elemento do array e deve retornar um novo valor para ser adicionado ao novo array.

A função reduce é usada para reduzir um array em um único valor, aplicando uma função para cada elemento do array. Sua sintaxe é:

```
const resultado = array.reduce(function(acumulador, item, index, array) {
  // código a ser executado para cada elemento
  return novoAcumulador;
}, valorInicial);
```

Onde acumulador é o valor acumulado até o momento, item é o elemento atual do array, index é a posição desse elemento no array, array é o próprio array e valorInicial é o valor inicial para o acumulador. A função passada como parâmetro é executada para cada elemento do array e deve retornar um novo valor para ser acumulado.

Por exemplo, se tivermos um array de números, podemos usar a função map para criar um novo array com o dobro de cada número:

```
const numeros = [1, 2, 3, 4, 5];
const numerosDobro = numeros.map(function(numero) {
  return numero * 2;
});
console.log(numerosDobro); // [2, 4, 6, 8, 10]
```

Podemos usar a função reduce para somar todos os números do array:

```
const numeros = [1, 2, 3, 4, 5];
const soma = numeros.reduce(function(acumulador, numero) {
  return acumulador + numero;
}, 0);
console.log(soma); // 15
```

E podemos usar a função forEach para imprimir cada número do array:

```
const numeros = [1, 2, 3, 4, 5];
numeros.forEach(function(numero) {
  console.log(numero);
});
// output:
// 1
// 2
// 3
// 4
// 5
```

#### 26. O que é serverless computing?

Serverless computing é um modelo de computação em nuvem que permite que os desenvolvedores criem e executem aplicativos sem a necessidade de gerenciar servidores ou infraestrutura. Em outras palavras, o servidor é gerenciado por um provedor de nuvem, deixando o desenvolvedor livre para se concentrar apenas na lógica do aplicativo.

Nesse modelo, a aplicação é executada em pequenos trechos de código (funções) que são executados em resposta a eventos específicos. Essas funções são executadas em um ambiente de execução gerenciado pelo provedor de nuvem, que lida com o dimensionamento e a manutenção da infraestrutura necessária para executá-las.

O serverless computing tem várias vantagens, como o fato de permitir que os desenvolvedores se concentrem na lógica do aplicativo, em vez de se preocuparem com a infraestrutura subjacente. Além disso, o modelo permite que os aplicativos sejam altamente escaláveis, pois o provedor de nuvem gerencia automaticamente o dimensionamento da infraestrutura de acordo com a demanda. Também é possível reduzir os custos, já que os desenvolvedores pagam apenas pelo tempo de execução das funções e não precisam pagar por recursos ociosos.

#### 27. Quais são os tipos primitivos do JavaScript?

Os tipos primitivos do JavaScript são:

- Number: utilizado para representar números, tanto inteiros como decimais. Exemplo: 42, 3.14.
- String: utilizado para representar cadeias de caracteres. Exemplo: "Olá mundo!".
- Boolean: utilizado para representar valores lógicos verdadeiro ou falso. Exemplo: true, false.
- Null: utilizado para representar a ausência intencional de qualquer objeto ou valor. É um tipo primitivo, mas não é um objeto.
- Undefined: utilizado para representar uma variável que não foi atribuída a um valor. Também é um tipo primitivo, mas não é um objeto.
- Symbol: um tipo de dado novo a partir do ECMAScript 6 que é usado para criar identificadores únicos.

Esses tipos primitivos são imutáveis, o que significa que uma vez criados, eles não podem ser alterados. Quando você tenta alterar o valor de um tipo primitivo, uma nova cópia do valor é criada em vez de alterar o valor original.

#### 28. Qual a diferença entre inline and inline-block?

Tanto o inline como o inline-block são valores da propriedade CSS display, que definem como um elemento deve ser exibido na página. A diferença entre eles é que:

- `inline`: faz com que o elemento seja exibido em linha com o texto que o cerca. Elementos inline não podem ter uma largura ou altura definida, e o conteúdo deles é ajustado automaticamente de acordo com o conteúdo dentro deles. Exemplos de elementos inline são: `<a>`, `<span>`, `<img>`, entre outros.
- `inline-block`: é semelhante ao inline, mas permite definir largura e altura para o elemento, como um elemento block. O inline-block também permite que outros elementos inline fiquem ao lado dele, o que não é possível com elementos block. Exemplos de elementos inline-block são: `<input>`, `<button>`, `<select>`, entre outros.

#### 29. Qual a diferença entre elementos posicionados como relative, fixed, absolute e static?

Os valores `relative`, `fixed`, `absolute` e `static` são valores possíveis da propriedade CSS position, que define o tipo de posicionamento que um elemento terá na página. A seguir, é explicada a diferença entre cada um deles:

- `static`: é o valor padrão da propriedade position. Um elemento com position: `static` é posicionado de acordo com o fluxo normal do documento. Qualquer outra propriedade de posicionamento (top, bottom, left, right) não terá efeito.
- `relative`: faz com que o elemento seja posicionado em relação à sua posição normal no fluxo do documento. Assim, se um elemento tem position: `relative` e uma propriedade top: 10px, por exemplo, ele será posicionado 10 pixels abaixo de sua posição normal. O espaço que ele ocupava no fluxo do documento permanece reservado, mesmo que o elemento seja movido. Seus filhos são posicionados relativamente a ele.
- `fixed`: faz com que o elemento seja posicionado em relação à janela de visualização do navegador. O elemento permanece no mesmo lugar, mesmo se a página for rolada. A propriedade top, bottom, left e right são usadas para definir a posição do elemento.
- `absolute`: faz com que o elemento seja posicionado em relação ao elemento pai mais próximo que tenha uma posição diferente de `static` (ou seja, `relative`, `fixed`, ou `absolute`). Se não houver nenhum elemento pai com posição diferente de `static`, o elemento será posicionado em relação ao corpo do documento. Como com `fixed`, as propriedades top, bottom, left e right são usadas para definir a posição do elemento.

#### 30. Você pode explicar a diferença entre codificar um site para ser responsivo e usar uma estratégia mobile-first?

Codificar um site para ser responsivo significa que o site foi projetado e desenvolvido para se adaptar a diferentes tamanhos de tela, incluindo desktop, tablet e dispositivos móveis. Isso é alcançado usando técnicas como media queries e grids flexíveis para reorganizar o conteúdo e ajustar o layout do site para atender às diferentes dimensões da tela.

Por outro lado, uma estratégia mobile-first é um processo de design e desenvolvimento em que o site é projetado primeiro para dispositivos móveis e, em seguida, adaptado para tamanhos maiores de tela. Isso significa que o design e layout do site são pensados ​​primeiro para um ambiente móvel, priorizando a simplicidade e a eficiência em detrimento da complexidade. Isso geralmente leva a um site mais rápido e fácil de usar em dispositivos móveis, enquanto ainda é capaz de se adaptar a tamanhos de tela maiores.

## Pleno

#### 1` Mencione qual é a diferença entre PUT e POST?

`PUT` e `POST` são dois dos principais métodos HTTP usados para enviar informações do cliente para o servidor. A diferença entre os dois métodos está relacionada ao objetivo de cada um deles:

- `POST` é usado para enviar dados novos ou atualizados para o servidor. O `POST` é comumente usado para criar novos recursos no servidor, enviar formulários, fazer upload de arquivos, etc. Quando um cliente envia uma solicitação `POST` para o servidor, o servidor cria um novo recurso ou atualiza um recurso existente com os dados enviados.
- `PUT` é usado para atualizar um recurso existente no servidor. O `PUT` é comumente usado para atualizar dados já existentes em um recurso no servidor. Quando um cliente envia uma solicitação `PUT` para o servidor, ele deve fornecer todos os dados necessários para atualizar completamente o recurso.

#### 2. O que são atributos defer e assync em uma tag `<script>`?

Os atributos `defer` e `async` em uma tag `<script>` permitem que o carregamento e a execução de scripts sejam gerenciados de maneira mais eficiente.

O atributo `defer` especifica que o script deve ser executado somente após o carregamento completo da página. Isso significa que o script é carregado em segundo plano enquanto o navegador continua a processar o restante da página, mas a execução do script é adiada até que a página seja completamente carregada. O uso de `defer` é recomendado para scripts que não dependem de outros recursos na página, como estilos ou outros scripts.

O atributo `async`, por outro lado, especifica que o script pode ser executado assim que ele for carregado, mesmo que a página ainda esteja sendo processada. Isso significa que o navegador pode executar o script assim que o download for concluído, sem esperar pelo restante da página. O uso de `async` é recomendado para scripts que não dependem de outros scripts ou recursos na página e que podem ser executados de maneira independente.

#### 3. O que significa SOLID? Quais são seus princípios?

SOLID é um acrônimo que representa cinco princípios da programação orientada a objetos que visam tornar o código mais fácil de entender, modificar e manter. Os princípios SOLID são os seguintes:

- 1. Single Responsibility Principle (Princípio da Responsabilidade Única): cada classe deve ter uma única responsabilidade. Isso significa que uma classe não deve ter mais de uma razão para mudar e deve ser responsável por apenas uma parte da funcionalidade do software.
- 2. Open-Closed Principle (Princípio Aberto-Fechado): as classes devem estar abertas para extensão, mas fechadas para modificação. Isso significa que o comportamento de uma classe deve ser estendido sem a necessidade de alterar seu código-fonte original.
- 3. Liskov Substitution Principle (Princípio da Substituição de Liskov): as classes derivadas devem ser substituíveis por suas classes base. Isso significa que as classes derivadas devem obedecer ao contrato da classe base e não devem alterar o comportamento pré-definido da classe base.
- 4. Interface Segregation Principle (Princípio da Segregação de Interfaces): os clientes não devem ser forçados a depender de interfaces que não usam. Isso significa que as interfaces devem ser projetadas para atender às necessidades específicas dos clientes e não devem conter métodos que os clientes não precisam.
- 5. Dependency Inversion Principle (Princípio da Inversão de Dependência): os módulos de alto nível não devem depender de módulos de baixo nível, ambos devem depender de abstrações. Isso significa que as dependências devem ser abstraídas em interfaces e as classes devem depender dessas interfaces em vez de depender de implementações concretas.

Esses princípios ajudam a produzir um código mais flexível, extensível e manutenível, o que é especialmente importante em projetos maiores e mais complexos. Eles são frequentemente usados em conjunto com padrões de design orientados a objetos para criar software de alta qualidade.

#### 4. O que é coerção em JavaScript?

Coerção (ou Type Coercion) em JavaScript é a conversão automática de valores de um tipo de dado para outro tipo de dado, que ocorre quando operações ou comparações são realizadas em valores de tipos diferentes. Isso pode acontecer implicitamente, sem que o programador esteja ciente, ou explicitamente, através de conversão de tipos utilizando funções como parseInt() ou parseFloat().

Por exemplo, se somarmos uma string com um número, a string será convertida automaticamente em um número: <br/>
`console.log('1' + 2); // 3`

No exemplo acima, a string '1' é convertida para o número 1 e então é realizada a soma com o número 2, resultando em 3.

No entanto, a coerção nem sempre é previsível ou intuitiva, e pode levar a bugs ou comportamentos inesperados no código. Por isso, é importante ter conhecimento sobre como a coerção funciona em JavaScript e evitar situações que possam causar problemas.

#### 5. SASS: O que é um Mixin e como usá-lo?

No Sass, um mixin é uma forma de agrupar declarações de estilo reutilizáveis em um bloco nomeado, que pode ser incluído em outros blocos de estilo. Isso permite que você defina um conjunto de estilos que pode ser reutilizado em várias partes do seu código, evitando a repetição desnecessária de código.

A sintaxe para definir um mixin é a seguinte:

```
@mixin nome-do-mixin {
  // declarações de estilo aqui
}
```

Para usar um mixin em um bloco de estilo, você utiliza a diretiva @include seguida pelo nome do mixin:

```
.classe-do-elemento {
  @include nome-do-mixin;
}
```

Dentro do bloco do mixin, você pode definir qualquer conjunto de declarações de estilo que desejar, incluindo seletores, propriedades, valores, etc. Por exemplo:

```
@mixin borda-arredondada {
  border-radius: 5px;
}
```

Ao incluir o mixin acima em um bloco de estilo, todas as propriedades definidas no mixin serão aplicadas ao elemento selecionado:

```
.botao {
  @include borda-arredondada;
  background-color: #ddd;
  color: #333;
  padding: 10px 20px;
}
```

No exemplo acima, o mixin `borda-arredondada` foi aplicado à classe `.botao`, resultando em um botão com bordas arredondadas de `5px`, além das outras propriedades definidas no bloco.

O uso de mixins pode ser muito útil para evitar a repetição de código em seus estilos, facilitando a manutenção e a organização do seu código. Além disso, os mixins podem aceitar argumentos e parâmetros, permitindo a criação de estilos ainda mais dinâmicos e reutilizáveis.

#### 6. Cite alguns sistemas de grid CSS

- 1. Bootstrap: O sistema de grid do Bootstrap é um dos mais populares e amplamente utilizados. Ele usa classes como col-md-4 para especificar colunas e container e row para organizar as colunas.
- 2. Foundation: O sistema de grid do Foundation é semelhante ao do Bootstrap e usa classes como large-4 para especificar colunas. Também possui classes de utilitário para definir largura, empurrar e puxar.
- 3. Materialize: O Materialize é um framework baseado no Material Design do Google e possui um sistema de grid semelhante ao do Bootstrap, usando classes como col s12 m6 para especificar colunas.
- 4. Gridlex: O Gridlex é um sistema de grid CSS leve que usa apenas uma classe para definir colunas. Ele também possui classes de utilitário para definir o espaçamento entre as colunas.
- 5. Susy: O Susy é um sistema de grid CSS flexível e personalizável que usa mixins do Sass para definir colunas e espaçamento. Ele não usa classes no HTML e permite a criação de layouts complexos e personalizados.

#### 7. Quando devo usar as Arrow functions no ES6?

As arrow functions foram introduzidas no ES6 para simplificar a sintaxe de funções e para resolver alguns problemas de escopo de `this` que ocorriam com as funções regulares. As arrow functions são uma maneira concisa de escrever funções anônimas.

Você pode usar arrow functions sempre que precisar de uma função anônima. As principais vantagens das arrow functions em comparação com as funções regulares são:

- 1. Sintaxe simplificada: A sintaxe das arrow functions é mais curta e mais clara, o que pode tornar o código mais fácil de ler e entender. Por exemplo:

```
// Função regular
const square = function(x) {
  return x * x;
}

// Arrow function
const square = (x) => {
  return x * x;
}
```

- 2. Escopo do `this` simplificado: Em funções regulares, o valor de `this` pode variar dependendo do contexto em que a função é chamada. Nas arrow functions, o valor de `this` é herdado do escopo pai, o que pode tornar o código mais previsível e menos propenso a erros. Por exemplo:

```
// Função regular
const obj = {
  count: 0,
  increment: function() {
    setInterval(function() {
      this.count++; // o valor de this é o objeto global, não o objeto `obj`
    }, 1000);
  }
}

// Arrow function
const obj = {
  count: 0,
  increment: function() {
    setInterval(() => {
      this.count++; // o valor de this é o objeto `obj`
    }, 1000);
  }
}
```

#### 8. Quando devemos usar generators no ES6?

Os generators são uma funcionalidade poderosa do ES6 que permitem que funções gerem um fluxo de valores sob demanda, em vez de retornar um valor único. Eles podem ser usados em várias situações, como:

- 1. Criação de iteradores personalizados: Os generators podem ser usados para criar iteradores personalizados que podem ser usados para iterar sobre coleções de dados de uma maneira personalizada.
- 2. Gerenciamento de fluxo de dados assíncronos: Os generators podem ser usados para simplificar o gerenciamento de fluxo de dados assíncronos em JavaScript. Eles permitem que você escreva código assíncrono de maneira síncrona, o que pode tornar o código mais legível e fácil de entender.
- 3. Gerenciamento de exceções: Os generators permitem que você capture exceções e gerencie erros de maneira mais eficiente do que com callbacks ou promessas. Eles também permitem que você manipule exceções de maneira personalizada, o que pode ajudar a criar um código mais robusto e confiável.

#### 9. Cite algumas características de sistemas reativos

- 1. Responsividade: um sistema reativo deve responder rapidamente a solicitações de entrada e fornecer uma saída oportuna, garantindo que os usuários tenham uma experiência fluida e sem interrupções.
- 2. Elasticidade: um sistema reativo deve ser capaz de se adaptar à carga de trabalho, escalando para lidar com picos de demanda e voltando ao tamanho original quando a demanda diminuir.
- 3. Resiliência: um sistema reativo deve ser capaz de lidar com falhas e se recuperar rapidamente delas, permitindo que o sistema continue a funcionar de forma confiável e consistente.
- 4. Orientado a mensagens: um sistema reativo deve ser orientado a mensagens, permitindo que diferentes partes do sistema se comuniquem de forma assíncrona e desacoplada, o que aumenta a flexibilidade e a escalabilidade do sistema.
- 5. Modelagem de eventos: um sistema reativo deve ser capaz de modelar eventos de entrada e saída em tempo real, permitindo que o sistema responda rapidamente a mudanças no ambiente e nas necessidades do usuário.
- 6. Streaming de dados: um sistema reativo deve ser capaz de lidar com grandes quantidades de dados em tempo real, permitindo que os usuários recebam informações continuamente e sem interrupções.

#### 10. Descreva a diferença entre a programação reativa e a programação imperativa

A programação imperativa é o paradigma de programação mais antigo e amplamente utilizado, em que o programador define passo a passo como a máquina deve executar as instruções para resolver um problema. É baseado em instruções sequenciais e ações com efeitos colaterais. Por exemplo, o código imperativo define como um loop deve ser executado ou como uma função deve alterar o estado global do programa.

Por outro lado, a programação reativa é um paradigma de programação baseado em fluxos de dados e eventos. Em vez de explicitamente definir como as ações devem ser executadas, a programação reativa reage a mudanças de estado e eventos e usa fluxos de dados para propagar essas mudanças. Em outras palavras, a programação reativa é uma forma de programação declarativa, que se concentra mais no que deve ser feito do que em como fazer isso.

A programação reativa é especialmente útil para construir aplicativos com uma grande quantidade de eventos e atualizações de estado em tempo real, como aplicativos de streaming, jogos, aplicativos de negociação em tempo real, etc. É altamente responsiva, escalável e resiliente. Alguns exemplos de bibliotecas e frameworks que implementam a programação reativa são o ReactiveX, o RxJS e o Akka.

#### 11. Qual é a diferença entre Promises e Observables?

Promises e Observables são duas abstrações para trabalhar com operações assíncronas em JavaScript. Embora ambos sejam usados para lidar com código assíncrono, eles têm diferenças significativas em como funcionam e como são usados.

- Promises são objetos que representam um valor que pode estar disponível agora, no futuro ou nunca. Uma Promise pode estar em um dos três estados: pendente, resolvida ou rejeitada. As Promises resolvem o problema de callbacks hell (callback hell é um cenário onde temos várias chamadas de retorno aninhadas que se tornam difíceis de manter e depurar) e permitem que você encadeie várias chamadas assíncronas com clareza. Além disso, as Promises têm métodos para lidar com diferentes estados, como then() e catch().
- Observables são sequências de eventos que podem ser assíncronos e contínuos. Eles são semelhantes a Promises, mas podem retornar vários valores em vez de um único valor. Observables são usados para lidar com eventos que podem ocorrer várias vezes e em um intervalo de tempo não especificado. Eles têm operadores poderosos que permitem filtrar, transformar e combinar eventos.

#### 15. O que é "git cherry-pick"?

O git cherry-pick é um comando do Git que permite "copiar" um ou mais commits específicos de uma branch para outra. Isso é útil quando você quer aplicar um conjunto específico de mudanças em uma branch diferente daquela em que as mudanças foram originalmente feitas.

Para usar o git cherry-pick, primeiro você precisa saber o hash do commit que deseja copiar. Em seguida, você pode executar o comando git cherry-pick seguido do hash do commit:

```
git cherry-pick <hash-do-commit>
```

Você também pode especificar vários hashes de commits, separados por espaços, para aplicar vários commits de uma vez:

```
git cherry-pick <hash-do-commit1> <hash-do-commit2> <hash-do-commit3> ...
```

Quando você executa o comando git cherry-pick, o Git aplica as alterações do commit especificado na branch atual em que você está. Se houver conflitos, o Git informará e você deverá resolvê-los manualmente.

É importante notar que o git cherry-pick cria uma nova confirmação com as mudanças do commit copiado, o que significa que o histórico de confirmações da branch de destino será diferente daquele da branch original.

#### 16. O que é um WebWorker?

Web Worker é uma tecnologia de navegador que permite a execução de scripts JavaScript em segundo plano, sem afetar o desempenho e a capacidade de resposta da interface do usuário. Ele permite que o JavaScript seja executado em uma thread separada do thread principal do navegador, o que evita bloqueios de interface do usuário e melhora a capacidade de resposta do aplicativo.

Os Web Workers são uma forma de processamento paralelo em JavaScript, em que um script pode executar em paralelo com outros scripts sem interferir no desempenho do navegador. Eles podem ser usados para executar cálculos pesados, como processamento de imagem, análise de dados e outras tarefas que podem levar a bloqueios ou lentidão no thread principal do navegador.

Existem três tipos de Web Workers:

- Dedicated Workers: são executados em uma única thread e possuem um único script de origem que é carregado e executado quando o Worker é criado.
- Shared Workers: são executados em uma única thread e compartilham um script de origem entre várias janelas do navegador ou guias que se comunicam com o Worker.
- Service Workers: são executados em segundo plano e são usados para gerenciar cache de rede, push notifications e outras funcionalidades relacionadas a rede.

#### 17. O que é o DOM?

O DOM (Document Object Model) é uma interface de programação de aplicativos (API) para documentos HTML e XML. Ele representa a página da web como um documento estruturado em objetos que podem ser manipulados por linguagens de programação, como JavaScript.

O DOM é uma representação em árvore da estrutura do documento, onde cada elemento da página é um nó na árvore. Com o DOM, é possível alterar dinamicamente o conteúdo e a aparência de uma página da web com base nas interações do usuário ou em eventos do sistema, como a conclusão do carregamento da página.

O DOM também permite que o JavaScript acesse e manipule os elementos da página, incluindo o conteúdo, estilo e atributos dos elementos, bem como as propriedades dos nós da árvore DOM.

#### 18. Qual a diferença de localStorage e sessionStorage?

localStorage e sessionStorage são recursos fornecidos pelo objeto `window` do JavaScript, que permitem o armazenamento de dados no navegador. Eles são semelhantes, mas diferem em alguns aspectos importantes:

- Escopo: <br/>
  O localStorage armazena os dados de forma persistente no navegador, mesmo depois que a página é fechada e reaberta, enquanto o sessionStorage armazena os dados apenas durante a sessão atual do usuário na página. Ou seja, quando a sessão é encerrada, os dados são perdidos.
- Compartilhamento de dados entre abas/janelas do navegador: <br/>
  Se você abrir duas abas do mesmo site e armazenar dados no localStorage, esses dados serão compartilhados entre as duas abas. Já no caso do sessionStorage, os dados não são compartilhados entre as duas abas.
- Limite de armazenamento: <br/>
  Os limites de armazenamento para ambos são definidos pelo navegador e podem variar entre navegadores. Normalmente, localStorage tem um limite de armazenamento maior do que sessionStorage.
- Métodos de armazenamento: <br/>
  Tanto o localStorage quanto o sessionStorage usam os mesmos métodos de armazenamento de chave/valor, ou seja, o `.setItem(key, value)` e o `.getItem(key)`.

Como acessar:
Para acessar tanto o localStorage quanto o sessionStorage, você pode utilizar a API do window, como por exemplo:

```
localStorage.setItem('chave', 'valor');
let valor = localStorage.getItem('chave');

sessionStorage.setItem('chave', 'valor');
let valor = sessionStorage.getItem('chave');
```

Em resumo, se você precisar armazenar dados permanentes que precisam estar disponíveis para o usuário em futuras visitas ao site, use o localStorage. Já se você precisar armazenar dados apenas para a sessão atual do usuário na página, use o sessionStorage.

#### 19. Como evitar callback hells?

No Angular, o uso de Observables pode ajudar a evitar o callback hell, que é um problema comum ao lidar com chamadas assíncronas comuns em aplicações web. Os Observables são usados para trabalhar com fluxos de dados assíncronos em tempo real, permitindo que os desenvolvedores gerenciem eventos em tempo real sem precisar lidar com callbacks aninhados.

Outra maneira de evitar callback hell no Angular é usar Promises. As Promises permitem que os desenvolvedores manipulem fluxos de dados assíncronos de forma mais limpa e organizada, evitando aninhar callbacks. Ao contrário dos callbacks, as Promises podem ser encadeadas para executar uma série de operações em ordem, tornando o código mais legível e mais fácil de entender.

Além disso, o uso de async/await pode simplificar ainda mais o código assíncrono no Angular. Ao usar async/await, os desenvolvedores podem escrever código assíncrono em uma sintaxe síncrona, o que torna o código mais legível e fácil de entender. Isso é especialmente útil ao lidar com chamadas assíncronas em cadeia, onde vários callbacks podem se tornar difíceis de gerenciar e manter.

#### 20. O que é Injeção de Dependencia?

No Angular, a injeção de dependência é um padrão de design que permite que um objeto receba dependências de outros objetos em tempo de execução. É uma técnica que ajuda a manter um código limpo, modular e fácil de testar.

Em termos simples, a injeção de dependência no Angular é o processo de passar uma dependência para um componente, serviço ou diretiva em tempo de execução. Essa dependência é então usada pelo componente para executar uma determinada tarefa.

O Angular fornece um mecanismo de injeção de dependência integrado, que é gerenciado pelo próprio framework. A injeção de dependência no Angular é feita usando os decoradores `@Injectable` e `@Inject`:

- `@Injectable`: é um decorador usado para marcar uma classe como um provedor de serviço que pode ser injetado em outros componentes ou serviços.
- `@Inject`: é um decorador usado para fornecer a dependência necessária para um componente, serviço ou diretiva.

O Angular fornece vários tipos de provedores de serviço que podem ser usados para fornecer dependências, como `ClassProvider`, `ValueProvider`, `FactoryProvider`, `ExistingProvider`, etc. É importante saber escolher o tipo de provedor certo para cada caso.

Por fim, a injeção de dependência no Angular é usada para evitar a criação excessiva de instâncias de objetos, melhorar a modularidade do código e permitir a fácil substituição de dependências em tempo de execução

#### 21. O que é a keyword "new" em JavaScript?

A keyword 'new' em JavaScript é usada para criar uma nova instância de um objeto a partir de uma função construtora. Quando usada com uma função que foi definida com a intenção de ser um construtor (por convenção, essas funções têm a primeira letra maiúscula), a palavra-chave 'new' cria um novo objeto vazio e o associa ao valor 'this' dentro da função construtora. A função construtora pode, então, adicionar propriedades e métodos ao objeto e, eventualmente, retorná-lo para o chamador.

Aqui está um exemplo básico de como usar a palavra-chave 'new':

```
function Pessoa(nome) {
  this.nome = nome;
}

const pessoa1 = new Pessoa('João');
console.log(pessoa1.nome); // saída: 'João'
```

Neste exemplo, criamos uma função construtora chamada 'Pessoa' que aceita um argumento 'nome' e adiciona uma propriedade 'nome' ao objeto associado a 'this'. Em seguida, criamos uma nova instância de 'Pessoa' usando a palavra-chave 'new' e atribuímos o resultado a 'pessoa1'. Podemos acessar a propriedade 'nome' do objeto usando 'pessoa1.nome'.

#### 22. Explique o conceito de Server Side Rendering

Server-side rendering (SSR) no Angular é o processo de renderizar o conteúdo do aplicativo do lado do servidor antes de enviar para o navegador do usuário. Isso difere do modelo tradicional do Angular, onde todo o aplicativo é renderizado no navegador do usuário. Com o SSR, o servidor envia ao navegador uma versão pré-renderizada da página que pode ser exibida instantaneamente, enquanto o aplicativo carrega em segundo plano.

Existem várias vantagens em usar o SSR no Angular:

- Melhor SEO: O conteúdo pré-renderizado é facilmente acessível para mecanismos de busca, o que pode melhorar a visibilidade do aplicativo nos resultados de pesquisa.
- Melhor desempenho inicial: Como parte do conteúdo já é renderizado no servidor, o navegador do usuário pode exibir a página mais rapidamente, reduzindo a latência percebida pelo usuário.
- Acessibilidade: A versão pré-renderizada da página pode ser exibida para usuários com deficiência visual que utilizam tecnologias assistivas.

Para implementar o SSR no Angular, é necessário criar um servidor Node.js que possa executar o Angular Universal, um módulo que fornece a funcionalidade necessária para pré-renderizar o aplicativo. Isso envolve a criação de componentes e modelos específicos para o servidor, que são usados ​​para renderizar a versão pré-renderizada da página. Além disso, o Angular Universal também fornece suporte para o gerenciamento do estado da aplicação, para garantir que a versão pré-renderizada seja consistente com a versão completa.

#### 23. O que são Estrutura de dados e porque elas são importantes?

Estrutura de dados é uma maneira organizada e estruturada de armazenar e manipular dados em um computador. É uma parte fundamental da ciência da computação e é usada em uma ampla variedade de aplicativos, desde bancos de dados de empresas até videogames e aplicações web. A escolha correta da estrutura de dados pode ter um impacto significativo no desempenho e eficiência de um programa.

As estruturas de dados são importantes porque permitem que os programadores armazenem e acessem dados de forma eficiente e organizada. Eles ajudam a reduzir a complexidade do código e a melhorar a legibilidade e manutenibilidade. Além disso, as estruturas de dados fornecem uma maneira padronizada de representar informações, permitindo que os desenvolvedores trabalhem em equipe e criem aplicativos mais escaláveis e robustos.

#### 24. O que é renderização progressiva?

A renderização progressiva é uma técnica que permite que o conteúdo de uma página da web seja renderizado gradualmente em vez de esperar por todo o conteúdo para ser processado antes de exibir qualquer coisa ao usuário. Em outras palavras, à medida que o servidor processa os dados, ele envia esses dados em pequenos pedaços para o navegador, que por sua vez renderiza o conteúdo imediatamente. Isso significa que o usuário pode começar a interagir com a página mais rapidamente, mesmo que ainda não esteja completamente carregada.

No contexto do Angular, renderização progressiva se refere ao processo de renderizar e exibir partes da interface do usuário de forma gradual e progressiva, à medida que elas são carregadas pelo servidor ou pelo cliente. Isso pode melhorar significativamente a velocidade de carregamento da página e a experiência do usuário, especialmente em conexões de internet lentas ou dispositivos com capacidades limitadas.

O Angular oferece suporte à renderização progressiva por meio do recurso de pré-renderização, que permite gerar uma versão em HTML da página no lado do servidor e enviá-la para o navegador como resposta à solicitação inicial do usuário. Isso permite que o usuário veja imediatamente a página, mesmo que a parte dinâmica dela ainda não tenha sido carregada.

Outra técnica utilizada pelo Angular para renderização progressiva é a lazy loading, que permite carregar módulos ou componentes de forma assíncrona, sob demanda, à medida que o usuário navega pela aplicação. Isso evita o carregamento desnecessário de recursos e melhora a velocidade geral da aplicação.

#### 25. Para que servem os data-attributes?

Os data attributes são atributos HTML personalizados que podem ser adicionados a elementos HTML para armazenar informações adicionais sobre esses elementos. Eles são chamados de "data-" seguidos pelo nome do atributo personalizado. Por exemplo, se você quiser armazenar informações sobre um produto em uma tabela HTML, poderia adicionar um atributo personalizado como "data-product-id" ou "data-product-name" a cada linha da tabela.

Os data attributes são úteis porque permitem que os desenvolvedores adicionem informações personalizadas a elementos HTML sem comprometer a semântica do documento ou interferir com os atributos padrão do HTML. Eles também podem ser usados ​​por scripts e estilos para selecionar e manipular elementos com base em suas informações personalizadas.

No contexto do JavaScript e do CSS, os data attributes podem ser usados para selecionar elementos de maneira mais precisa e específica do que com classes e identificadores, permitindo assim uma maior flexibilidade na manipulação do DOM. Por exemplo, você pode usar um data attribute para selecionar todos os elementos que compartilham uma determinada informação personalizada, independentemente de sua classe ou identificador.

No Angular, geralmente utilizamos as propriedades de componentes para passar dados entre componentes ou para adicionar informações adicionais a elementos HTML. Através das propriedades, podemos passar dados complexos ou tipos primitivos, como strings, números ou booleanos.

No entanto, se for necessário passar um dado específico que não pode ser adicionado como propriedade, pode-se usar o atributo `data` em um elemento HTML para armazenar o dado em questão. Esse atributo pode ser acessado no componente correspondente através do objeto `ElementRef` e do método `getAttribute()`.

Por exemplo, no HTML, pode-se adicionar um atributo data em um elemento `<button>`:

```
<button data-foo="bar">Clique aqui</button>
```

No componente correspondente, pode-se acessar esse atributo através do objeto ElementRef:

```
import { Component, ElementRef } from '@angular/core';

@Component({
  selector: 'app-exemplo',
  template: '<button data-foo="bar" (click)="clique()">Clique aqui</button>'
})
export class ExemploComponent {
  constructor(private elementRef: ElementRef) {}

  clique() {
    const foo = this.elementRef.nativeElement.querySelector('button').getAttribute('data-foo');
    console.log(foo); // Output: "bar"
  }
}
```

#### 26. Explique a diferença entre funções sincronas e assíncronas.

As funções síncronas e assíncronas diferem na forma como elas lidam com a execução de código e o fluxo de controle em um programa.

Uma função síncrona é uma função que executa seu código de forma sequencial, linha por linha, aguardando a conclusão de cada operação antes de passar para a próxima. Ela bloqueia o fluxo de execução do programa até que ela termine sua execução. Ou seja, quando uma função síncrona é chamada, o programa aguarda até que ela termine para continuar sua execução.

Por outro lado, uma função assíncrona é uma função que executa em segundo plano, permitindo que outras operações continuem enquanto ela executa. Essa função não bloqueia o fluxo de execução do programa, permitindo que outras operações sejam executadas enquanto aguarda o resultado de sua operação. Em vez de bloquear o fluxo de execução do programa, a função assíncrona retorna uma promise que pode ser resolvida com o resultado da operação.

#### 27. Qual a diferença entre os métodos setTimeout e setInterval?

Ambos `setTimeout() `e `setInterval()` são métodos de temporização no JavaScript que executam uma função após um determinado intervalo de tempo. No entanto, há uma diferença fundamental entre os dois.

A função `setTimeout()` é usada para atrasar a execução de uma função por um intervalo de tempo específico (em milissegundos). A função é executada uma única vez depois que o tempo especificado expira. É comumente usado para criar atrasos ou para agendar uma única execução de uma tarefa no futuro.

Por outro lado, a função `setInterval()` é usada para executar uma função repetidamente em intervalos regulares. A função é executada várias vezes depois que o intervalo de tempo especificado expira, até que seja explicitamente cancelada. É comumente usado para criar animações ou atualizar dados em tempo real em uma página da web.

#### 28. O que é um construtor?

Em JavaScript, um construtor é uma função especial que é usada para criar e inicializar objetos. Quando uma função é definida como construtora, ela pode ser invocada com a palavra-chave new para criar um novo objeto. Esse objeto é então retornado pela função construtora.

O construtor é usado para definir as propriedades e métodos de um objeto quando ele é criado. As propriedades do objeto são definidas usando a palavra-chave this dentro do corpo da função construtora. O this se refere ao objeto que está sendo criado.

Por exemplo, vamos criar um construtor para um objeto Pessoa que terá as propriedades nome e idade:

```
function Pessoa(nome, idade) {
  this.nome = nome;
  this.idade = idade;
}
```

Em JavaScript, um construtor é uma função especial que é usada para criar e inicializar objetos. Quando uma função é definida como construtora, ela pode ser invocada com a palavra-chave new para criar um novo objeto. Esse objeto é então retornado pela função construtora.

O construtor é usado para definir as propriedades e métodos de um objeto quando ele é criado. As propriedades do objeto são definidas usando a palavra-chave this dentro do corpo da função construtora. O this se refere ao objeto que está sendo criado.

Por exemplo, vamos criar um construtor para um objeto `Pessoa` que terá as propriedades `nome` e `idade`:

javascript
Copy code
function Pessoa(nome, idade) {
this.nome = nome;
this.idade = idade;
}
Em seguida, podemos criar um novo objeto `Pessoa` usando o construtor:

```
let pessoa1 = new Pessoa('João', 30);
console.log(pessoa1.nome); // "João"
console.log(pessoa1.idade); // 30
```

Dessa forma, o construtor é uma forma de criar objetos com as propriedades e métodos necessários, permitindo que sejam criados vários objetos do mesmo tipo de forma fácil e rápida.

#### 29. Qual a função dos prototypes no JavaScript?

Em JavaScript, os prototypes são usados para compartilhar propriedades e métodos entre objetos. Quando um objeto é criado, ele herda as propriedades e métodos do seu protótipo. Isso significa que, em vez de ter cada objeto com suas próprias propriedades e métodos, é possível ter uma "classe" de objetos que compartilham as mesmas propriedades e métodos, tornando o código mais eficiente e fácil de manter.

Para criar um protótipo, é possível usar a função construtora padrão ou definir uma função personalizada. A partir daí, é possível adicionar propriedades e métodos ao objeto protótipo usando a propriedade `prototype`. Por exemplo:

```
function Pessoa(nome, idade) {
  this.nome = nome;
  this.idade = idade;
}

Pessoa.prototype.cumprimentar = function() {
  console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
};

let pessoa1 = new Pessoa("João", 30);
let pessoa2 = new Pessoa("Maria", 25);

pessoa1.cumprimentar(); // Olá, meu nome é João e tenho 30 anos.
pessoa2.cumprimentar(); // Olá, meu nome é Maria e tenho 25 anos.
```

Nesse exemplo, a função `Pessoa` é usada como construtora para criar objetos que possuem as propriedades `nome` e `idade`. Além disso, o método cumprimentar é adicionado ao protótipo da função `Pessoa`. Isso significa que todos os objetos criados a partir da função `Pessoa` herdam esse método e podem usá-lo.

#### 30. O que são High Order Functions

High-order functions são funções que recebem outras funções como argumentos e/ou retornam outras funções como resultado. Em outras palavras, elas tratam funções como valores de primeira classe, permitindo que sejam usadas de forma mais flexível e modular em um programa.

Um exemplo simples de high-order function é a função map(), que é usada em muitas linguagens de programação, incluindo JavaScript. A função map() recebe uma função de transformação como argumento e aplica essa função a cada elemento de um array, retornando um novo array com os valores transformados.

Outro exemplo de high-order function é a função filter(), que recebe uma função de filtro como argumento e retorna um novo array com os elementos que atendem aos critérios definidos pela função de filtro.

High-order functions são úteis porque permitem que o código seja mais genérico e reutilizável, reduzindo a duplicação de código e tornando o programa mais fácil de manter e evoluir. Além disso, elas permitem que as funções sejam compostas e combinadas de forma mais flexível, tornando a programação mais expressiva e poderosa.

## Senior

#### 1. O que é "closure" no javascript? Cite um exemplo?

#### 2. Imperativo vs Funcional vs Programação Reativa.Explique

#### 3. Você pode explicar o que “git reset” faz ?

#### 4. Qual a diferença de Interface e Type no TypeScript?

#### 5. O que é teste de unidade, teste de integração e quais são as diferenças entre eles?

#### 6. O que é uma arvore de busca binária?

#### 7. O que é o Shadow DOM e qual seu uso?

#### 8. Qual a diferença entre os métodos apply.call e bind?

#### 9. O que descreve o algoritmo de Big O Notation?

#### 10. O que é o conceito de Immutabilidade?

#### 11. Quais são boas práticas de Clean Code?

#### 12. O que é o "HEAD" no Git?

#### 13. Quais são as diferenças entre continuous integration, continuous delivery e continuous deployment?

#### 14. Explique um caso de uso do Docker

#### 16. Como você abordaria a correção de problemas de estilo específicos do navegador?

#### 17. Angular: O que são lifecycle hooks para componentes e diretivas?

#### 18. Explique o conceito de Lazy Loading

#### 19. Quando se usar uma classe abstrata?

#### 20. Explique o conceito de encapsulamento de dados

#### 22. Porque você criaria classes estáticas?

#### 23. Explique o CORS e como isso pode afetar um website.

#### 24. Cite algumas vulnerabilidades de REST APIS

#### 25. O que é JWT? Como implementar? Quais são as alternativas?

#### 26. O que é Styled Components? Cite Alternativas

#### 27. Dê exemplos de bibliotecas CSS in JS e suas vantagens e desvantagens

#### 28. Dê exemplos de Convenções de código de JavaScript

#### 29. Quais as vantagens e desvantagens de programação funcional vs orientada a objetos?

#### 30. O que é o two-way data binding e o one-way data flow, e qual sua diferença?

## Expert

#### 1. Cite algumas práticas recomendadas para um melhor design de API RESTful

#### 2. Programação Reativa: Explique Message-Driven vs Event-Driven

#### 3. Qual o modelo mental do redux-saga?

#### 4. Quando se usa "git rebase" ao invés de "git merge"?

#### 5. O que são webcomponents?

#### 6. O que é ARIA?

#### 7. O que é um Hash Table?

#### 8. O que é o WebAssembly?

#### 9. Angular: compliação Just-in-Time (JiT) vs Ahead-of-Time (AoT).Explique a diferença.

#### 10. Qual a vantagem do incremental DOM sobre o virtual DOM?

#### 11. OOP: Qual a diferença entre um mixin e uma herança?

#### 12. Como estilizar um elemento que está após o elemento selecionado?

#### 13. Explique como 'this' funciona no JavaScript

#### 15. Qual dos dois é mais seguro, JWT ou OAuth2?

#### 16. Como o V8 compila o código JavaScript?

#### 17. O que é WCAG? Quais as diferenças de compliance A, AA, and AAA?

#### 18. O que é CSS BEM? Cite outros exemplos de Arquitetura CSS

#### 19. Quais os prós e contras de arquiteturas monolíticas vs microserviços?

#### 20. Qual o problema com o nesting do Sass? De algum exemplo.

#### 21. Fale as principais diferenças entre UX e UI Design

#### 22. O que é caching?

#### 23. Qual é o proposito do metodo OPTIONS em webservices RESTful?

#### 24. Quais ferramentas você usaria para encontrar um bug de performance em seu código?

#### 25. Explique a diferença entre layout, painting and compositing.

#### 26. O que é domain pre-fetching e como ajuda com performance?

#### 27. O que é CDN e quais os benefícios de usar uma?

#### 28. JS: O que é Currying? Dê um exemplo de aplicação

#### 29. ES6: Async-Await x Yield/Next Generator, cite exemplos e diferenças

#### 30. JS: O que é o "use strict";? Quais vantagens e desvantagens?

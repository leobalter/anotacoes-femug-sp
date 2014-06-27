# InterConWP 2014

## FEMUG-SP 

### Anotações (parte 1) - Contribuição open source

* Conhecer dificuldades e frustrações para contribuições open source
* Conhecer o projeto, propor uma novidade e discutir sobre o assunto
* Contribuir para projetos que você utiliza (muitas empresas fazem isso hoje)
* Não ter medo de contribuir
* Não precisa ser código, pode ser documentações, testes entre outros
* Não se desestimular se sua proposta não foi aceita
* É importante seguir as diretrizes do projeto que vai contribuir
* Git e Github foram e são importantes para esta evolução
* Não ficar puto com decisões diferentes da sua num projeto
* Considerar o conhecimento da equipe ao arquitetar um projeto
* Ser adaptável à todos os ambientes é importante
* Assumir o erro e falar que não sabe é sadio para as equipes
* Vaidade em projetos é besteira
* O open source evoluiu
* Alguns exemplos de projetos open source: [esformatter](https://github.com/millermedeiros/esformatter) e [brasil.io](https://github.com/turicas/api.brasil.io)
* Não há problemas em criar diversos projetos diferentes e não unir forças num só projeto
* Naturalmente ocorre auto-regulação e seleção natural para os projetos open source
* Não há problema em criar suas próprias ferramentas

### Anotações (parte 2) - Qualidade de código

* Solucionar problema sem causar mais problema
* Code review atrasa o processo de desenvolvimento mas é importante
* O code review divide a pressão entre quem escreveu e quem revisou o código e deve fazer parte do workflow de trabalho
* O código não pode ter a identidade de um só programador, e sim, da equipe
* É importante manter a sanidade dos branches e seguir guidelines de código
* O código não te define
* Nosso código deve ser apagado frequentemente para não pegarmos amor por ele
* Debugar é a arte de remover o código que você mesmo colocou
* Testar é importante e você deve saber o que e para que testar
* nem sempre erro é certo ou errado

## Palestras sobre front-end

### JS Sustentável por [Leo Balter](https://twitter.com/leobalter)

* Sustentável - Maintainable
* O código em que trabalhamos raramente é novo
* Inconsistência de código, arquitetura fraca, falta de documentação e falta de testes
* Projeto fast-food (pode ter sido feito por outra pessoa)
* Problemas de inconsistência no JS
    * Ou usa ou não usa
    * Não misturar padrões de códigos
    * Existem vários estilos de escrita como jQuery Style Guide, Idiomatic JS entre outros
* Utilizar o Git e o Github como aliado
* Arquitetura do projeto é muito importante
* É importante versionar o código e guardar referências
* Certos projetos funcionam com o seu código ruim (e se consertar, quebra tudo!)
* Sugestões de livros: 
    * JavaScript: The Good Parts
    * Effective JavaScript
    * Maintainable JavaScript
* Documentação é importante e serve para você relembrar seu próprio código
* É importante testar para se certificar de que tudo funciona
* Não existe somente teste unitário
* Pode-se utilizar testes de aceitação, code review entre outros
* Code review é importante
* Problema da tartaruga na árvore: ninguém sabe quem colocou e nem se pode tirá-la de lá
* Não tente otimizar mais o seu código
* Permita que seu código quebre
* Equilíbrio entre o que é **entregável** e **sustentável**
* Envie cédigo para o Github

### Firefox OS + HTML5 + CSS3 + JavaScript por [David Ruiz](https://twitter.com/wupsbr)

* Início da internet (domínio do IE e Netscape comprado pela AOL)
* O seu código foi aberto
* A Microsoft vem adotando padrões ultimamente
* O Google não contribui mais com o WebKit
* O Opera e o Google utilizam o Blink como motor
* A web está migrando para o mobile
* Cada fabricante esta blindando sua plataforma
* Controlam hardware, sistema operacional, navegador, aplicativos e ecossistema de aplicativos
* A web morreu?
* A web móvel é viável se:
    * suportar múltiplas plataformas
    * desempenho nos browsers móveis
    * padrões web móvel
    * mecanismos de monetização para web
    * mecanismos de descobertas de web apps
* A web móvel é viável com HTML5, CSS3, JavaScript
* Quebrar o monopólio com Firefox OS
* Mais de 60% do mercado são feature phones
* Explorar novos recursos 
* Perde-se 50% de desempenho usando setTimeOut
* Para o Firefox OS o site é um aplicativo
* Hosted app - aplicação instalado como favoritos
* App - empacota e faz upload
* É possível implementar push notification no browser
* Aplicativos privilegiado - acesso ao sistema de arquivos, comunicação TCP, contatos entre outros
* Jogos nativos em HTML5, JS e WebGL
* Biblioteca LLVM - código C++ para navegador
* Frameworks
    * Building Blocks - exemplos para interfaces móveis responsivas que funcionam em 
    * buildingfirefoxos.com

### Repensando aplicações WordPress com Backbone por [Jean Carlo Emer](https://twitter.com/jcemer)

* Utilizamos JavaScript para melhorar a interatividade
* A organização é precária
* O jQuery facilita requisições assíncronas e manipulação do DOM
* Mas também o jQuery deixa amarrado com o elemento da página e isso causa problemas
* Problemas que podem ser solucionados com desgin patterns
* São soluções conhecidas e documentadas
* Facilita a manutenção, reúso e abstrações além de promover a leitura
* É necessário conhecer diferentes soluções para atender os problemas da melhor maneira possível
* O [Addy Osmani](addyosmani.com) aborda bastante conteúdo sobre design patterns
* O WordPress adicionou o Backbone ao seu núcleo
* O Backbone utiliza MVC e é utilizado organizar melhor o código e promover a separação de interesses
* Estrutura básica do Backbone
* Propõe models, views, collections
* Models
    * armazena os dados da sua aplicação (todos os dados do front-end no model)
    * utiliza eventos (observer pattern)
    * observer pattern: o sujeito notifica mudanças no seu estado para sua lista de ouvintes
    * fazer o uso de eventos é uma das principais características do Backbone
    * pode-se atrelar APIs REST aos eventos
    * resumo: armazenar dados, notificar ouvintes e facilmente sincronizáveis com o servidor)
* Collections
    * é uma coleção de models
    * permite carregar várias models numa requisição somente
    * UnderscoreJS
        * projeto irmão do Backbone
        * possui funções para operar sobre coleções
        * permite utilizar o JavaScript de uma maneira mais funcional
        * permite filtrar os atributos
    * resumo: armzenar coleção de models, notifica mudanças nos modelos e não salva no servidor
* Views
    * gerenciam a relação entre elementos da página e sua abstração
    * o código da view não deve conter HTML
    * para este fim deve-se utilizar templates    
    * existe um motor de template no UnderscoreJS
    * existe também outros sabores de templates
    * numa breve alusão ao desenvolvimento back-end: as views se comportam como controllers e os templates funcionam como views geralmente
    * a view escuta o model
    * usar o listenTo para o modelo escutar a operação
    * as views são a interface com o usuário
    * as views cuidam dos eventos gerados pelo usuário
    * resumo: abstração que possui elemento HTML, são semelhantes a controllers e  monitora os dados e interações do usuário
* Rotas
    * conecta URLs a estados de sua aplicação
    * as views vão identificar as rotas 
    * as URLs mantem o histórico de navegação do usuário
    * toda URL definida pelo router deve também ser servida pelo servidor
    * gerenciam as rotas de sua aplicação
* WordPress possui uma API REST para acessar seu blog
    

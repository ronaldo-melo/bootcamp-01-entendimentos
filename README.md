# Por favor, escreva seus entendimentos sobre os tópicos abaixo:

- Sobre ser melhor estudante
- Sobre cdd
- Sobre o conjunto de técnicas de código
- Sobre cada funcionalidade implementada

# Por favor faça um Fork desse projeto!

## Está em dúvida de como fazer um Fork? Não tem problema! [Aqui tem uma explicação do que entendemos que você deve considerar!](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo)

1} Atualização - 08/10/2020

Sobre ser melhor estudante: nesse ponto meu contato com o material escrito me apresentou formas diferentes de como algo que antes eu fazia apenas de uma forma. Um exemplo: antes eu sempre usava JPA Repository para consultas e vendo exemplos de outras formas de realizar persistência no banco de dados conclui que para o 3 desafio do processo (prover uma api simulando o comportamento de uma rede social) usar a interface CrudRepository era o suficiente para implementar as funcionalidades desejadas. E continuando no assunto de persistência fui olhar em mais detalhes toda a hierarquia do JPA Repo e nesse ponto vi como o spring faz uso do "mandamento" de programar voltado a interface e não a implementação (este conceito eu já ouvi/vi ser mencionado em diversos textos e podcasts(hipsters.tech e nos capitulos iniciaos do Design Patterns do GoF e eu não me refiro a interface como a palacra reservada do java mas a um ponto central de acesso que esconde uma complexidade de implementação do usuário que fará uso da interface). Mesmo ouvindo esse conceito muitas VEZES achava que era algo bem "utopico" de entendê-lo mas depois de buscar saber como funciona o EntityManager e sua relação com toda a hierarquia do JPA Repo eu pode ter uma luz sobre o que seria "programar voltado para interface e não implementação" porque toda a hierarquia de interfaces de JPA Repo é uma abstração sobre o Entity Manager (que também é uma interface que tem uma classe que a implementa e que por sua vez é uma abstração do modelo OO sobre relacional para o desenvolvedor JAVA). Olhando com mais atenção na documentação pode ver o quanto cada classe que faz a implementação "pesa" ao ser trazida para a aplicação através da injeção de dependência. Por peso eu me refiro aos métodos em cada uma dessas interfaces e os mesmo tempo a quantidade de classes usadas (acoplamentos que as implementações usam para dar corpo aos métodos do contrato da interface), porque a memória é um recurso caro e por isso é preciso ter cuidado com o que cada uma dessas interfaces acaba trazendo para aplicação ao adotá-la no desenvolvimento. Exemplo: para uma aplicação que tem como regra negócio ordenar uma lista de elementos ou fazer a exibição destes em quantias por vez é usada a interface JPA Repository, para situações onde as funções se resumem a criação, pesquisa, atualização e exclusão é a apropriado usar a CRUD Repository. Opcionalmente EntityManager pode ser usada para atender a ambas os cenários descritos antes mas vai exigir do desenvolvedor um conhecimento profundo do seu funcionamento pois o uso dessa interface exige conhecer detalhes de seu funcionamento e isso em termos de tempo pode custar bastante para criar funcionalidades e por isso interfaces como JPA Repository e CRUD Repository são abstrações acima de Entity Manager, ou seja, poupam o desenvolver detalhes dando-lhe mais agilidade na hora de criar soluções para regras de negócio. 

Sobre cdd
Sobre o conjunto de técnicas de código
Sobre cada funcionalidade implementada

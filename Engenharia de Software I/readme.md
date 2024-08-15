# Aula 1

We see three critical differences between programming and software engineering: time, scale, and the trade-offs at play. On a software engineering project, engineers need to be more concerned with the passage of time and the eventual need for change. In a software engineering organization, we need to be more concerned about scale and efficiency, both for the software we produce as well as for the organization that is producing it. Finally, as software engineers, we are asked to make more complex decisions with higher-stakes outcomes, often based on imprecise estimates of time and growth.

## Comentário
O texto aborda as principais diferenças entre programação e engenharia de software, destacando três aspectos críticos:
1. Tempo: Programação foca em tarefas imediatas, enquanto engenharia de software considera manutenção e evolução a longo prazo.
2. Escala: Programação lida com módulos menores; engenharia de software precisa garantir que o sistema seja escalável e eficiente.
3. Trade-offs: Programação envolve decisões locais e rápidas; engenharia de software requer decisões complexas com impacto amplo e baseadas em estimativas imprecisas.
Em resumo, a engenharia de software abrange uma visão mais estratégica e integrada do que a programação.

# Aula 2

Within Google, we sometimes say, “Software engineering is programming integrated over time.” Programming is certainly a significant part of software engineering: after all, programming is how you generate new software in the first place. If you accept this distinction, it also becomes clear that we might need to delineate between programming tasks (development) and software engineering tasks (development, modification, maintenance). The addition of time adds an important new dimension to programming. Cubes aren’t squares, distance isn’t velocity. Software engineering isn’t programming.

## Comentário 

O texto diferencia programação de engenharia de software, explicando que a programação cria software, enquanto a engenharia de software abrange o desenvolvimento, modificação e manutenção ao longo do tempo. Em resumo, engenharia de software integra a programação com uma visão de longo prazo.

# Aula 3: Exemplos de trade-offs com requisitos não funcionais

### 1. Desempenho vs. Segurança:
**Exemplo**: Em C/C++, você pode optar por usar ponteiros e manipulação direta de memória para otimizar o desempenho. No entanto, isso pode tornar o código vulnerável a ataques como buffer overflows ou corrupção de memória.

**Trade-off**: Maximizar o desempenho com manipulação direta de memória pode comprometer a segurança, pois você pode introduzir vulnerabilidades que exigem medidas adicionais para mitigação.

### 2. Manutenibilidade vs. Desempenho:
**Exemplo**: Em Java, você pode usar técnicas avançadas de otimização como o uso de estruturas de dados complexas ou algoritmos altamente eficientes. Embora essas técnicas possam melhorar o desempenho, elas também podem tornar o código mais complexo e difícil de entender e manter.

**Trade-off**: Priorizar o desempenho pode levar a um código menos legível e mais difícil de manter, o que pode aumentar o custo e o esforço para futuras alterações ou correções.

### 3. Portabilidade vs. Funcionalidade Específica:
**Exemplo**: Se você está desenvolvendo um aplicativo em Python e deseja usar bibliotecas específicas para aproveitar características únicas de um sistema operacional (como chamadas de sistema específicas), isso pode tornar seu aplicativo menos portátil.

**Trade-off**: Optar por funcionalidades específicas de um sistema operacional pode limitar a capacidade de seu aplicativo de ser executado em diferentes plataformas ou sistemas, impactando a portabilidade.

### 4. Facilidade de Uso vs. Controle Fino:
**Exemplo**: Em uma linguagem de alto nível como Python, você pode ter abstrações e frameworks que facilitam o desenvolvimento, mas podem abstrair detalhes finos de controle de execução e gerenciamento de recursos. Em contraste, linguagens como C++ oferecem mais controle sobre a memória e o hardware, mas com maior complexidade.

**Trade-off**: Usar abstrações e frameworks para facilitar o desenvolvimento pode limitar o controle fino sobre os recursos do sistema, enquanto o uso de linguagens mais detalhadas pode aumentar a complexidade do desenvolvimento e a curva de aprendizado.

### 5. Velocidade de Desenvolvimento vs. Performance:
**Exemplo**: Em um projeto desenvolvido em Ruby on Rails, o foco pode ser na velocidade de desenvolvimento e prototipagem rápida, usando a convenção sobre configuração e ferramentas integradas. No entanto, isso pode resultar em uma aplicação que não é tão otimizada em termos de desempenho.

**Trade-off**: Priorizar a velocidade de desenvolvimento e a facilidade de uso das ferramentas pode levar a uma aplicação que não é tão eficiente em termos de desempenho, o que pode ser um problema para aplicativos com alta carga ou requisitos de desempenho crítico.

# Análise das trade-offs na arquitetura da Netflix

### 1. Descentralização vs. Consistência
**Descentralização**: A Netflix adota uma arquitetura altamente descentralizada, baseada em microservices. Isso permite que diferentes equipes desenvolvam, implantem e escalem suas próprias partes do sistema de forma independente.

**Consistência**: A descentralização pode levar a desafios com a consistência dos dados. Para mitigar isso, a Netflix usa sistemas de armazenamento e cache que ajudam a garantir que as informações estejam atualizadas e disponíveis, mas não necessariamente em tempo real em todos os pontos.

### 2. Escalabilidade vs. Complexidade
**Escalabilidade**: A arquitetura da Netflix é projetada para escalar horizontalmente. Isso significa que a empresa pode adicionar mais instâncias de serviços para lidar com aumentos na carga, em vez de depender de um único servidor poderoso.

**Complexidade**: A escalabilidade horizontal e a adoção de microservices introduzem uma complexidade significativa na gestão do sistema. Isso inclui desafios com a comunicação entre serviços, a coordenação de implantações e o monitoramento da saúde do sistema.

### 3. Resiliência vs. Custo
**Resiliência**: A Netflix investe fortemente em resiliência e disponibilidade, utilizando técnicas como failover automático e redundância de dados. O Chaos Engineering, por exemplo, é uma prática usada para testar a resiliência do sistema sob condições adversas.

**Custo**: Implementar essas soluções de alta disponibilidade pode ser caro. O custo de infraestrutura, testes e operações aumentam à medida que se adicionam mais recursos para garantir a resiliência.

### 4. Desempenho vs. Flexibilidade
**Desempenho**: Para garantir um desempenho ótimo, a Netflix usa caching agressivo, balanceamento de carga e técnicas de otimização de rede. Isso ajuda a fornecer uma experiência de streaming de alta qualidade para os usuários.

**Flexibilidade**: Implementar essas otimizações pode limitar a flexibilidade em termos de como os serviços são projetados e modificados. A busca por desempenho pode restringir a maneira como os serviços podem evoluir e se adaptar a novas necessidades.

### 5. Automatização vs. Controle Manual
**Automatização**: A Netflix utiliza ferramentas e scripts para automatizar muitas operações, incluindo a implantação de serviços e a gestão de falhas. Isso melhora a eficiência e reduz o risco de erro humano.

**Controle Manual**: Embora a automação traga muitos benefícios, pode haver casos em que o controle manual é necessário para resolver problemas complexos ou implementar mudanças específicas. Encontrar o equilíbrio entre automação e controle manual é um desafio constante.

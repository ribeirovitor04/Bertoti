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

# Exemplos de trade-offs com requisitos não funcionais

### 1. Desempenho vs. Segurança:
Desempenho: Um sistema que prioriza desempenho pode utilizar métodos mais rápidos de processamento e menos verificação, como evitar criptografia complexa para melhorar a velocidade de resposta.
Segurança: Em contraste, um sistema que prioriza segurança pode adicionar camadas de criptografia e autenticação, o que pode impactar a velocidade de processamento e o tempo de resposta do sistema.
Trade-off: Se você optar por um desempenho mais rápido, pode haver um risco maior de vulnerabilidades. Se optar por segurança robusta, o sistema pode ter um desempenho mais lento.

### 2. Escalabilidade vs. Custo:
Escalabilidade: Investir em uma arquitetura escalável pode significar o uso de soluções em nuvem que podem crescer conforme a demanda aumenta, permitindo que o sistema suporte um número crescente de usuários e dados.
Custo: Soluções escaláveis geralmente vêm com custos mais altos devido à infraestrutura e manutenção. Optar por uma solução mais econômica pode significar menos flexibilidade para crescer conforme a demanda.
Trade-off: Se você escolher uma solução mais barata, pode ter limitações na capacidade de escalar rapidamente. Se optar por uma solução escalável, os custos serão mais elevados.

### 3. Manutenibilidade vs. Performance:
Manutenibilidade: Projetar um sistema com foco na manutenibilidade pode envolver a adoção de práticas como o uso de código limpo, modularidade e documentação detalhada, o que pode adicionar alguma sobrecarga ao desempenho.
Performance: Para maximizar a performance, você pode precisar de código otimizado e específico que pode ser mais difícil de manter e entender.
Trade-off: Focar na performance pode levar a um sistema mais difícil de manter e atualizar. Focar na manutenibilidade pode resultar em algum sacrifício de desempenho.

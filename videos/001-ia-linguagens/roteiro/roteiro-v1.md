# A IA pode matar novas linguagens de programação?

**Tese:** a IA não escolhe apenas como o código será escrito; ela começa a mudar quais linguagens são economicamente viáveis para uma empresa.  
**Duração estimada:** 8 a 10 minutos.

Talvez a próxima grande linguagem de programação morra antes mesmo de ficar popular.

Não porque ela é ruim.

Não porque ela é lenta.

E nem porque os programadores não gostaram dela.

Mas porque a IA não sabe programar direito nela.

Pensa comigo. De um lado, você tem uma linguagem moderna, segura, com um sistema de tipos absurdo e criada para evitar uma quantidade enorme de erros. Do outro, você tem Python: uma linguagem que existe em todo lugar, tem biblioteca para absolutamente tudo e provavelmente já apareceu bilhões de vezes nos dados usados para treinar modelos de IA.

Aí o seu chefe pede uma funcionalidade para amanhã de manhã.

Qual das duas você acha que o agente vai escrever melhor?

Pois é.

E esse é um problema muito maior do que decidir se você deve aprender Python, Java, Rust ou a nova linguagem favorita de três pessoas no Hacker News.

Porque, pela primeira vez, talvez uma linguagem não precise convencer apenas os programadores a usá-la. Ela também precisa ser boa para as máquinas que vão escrever código nela.

E isso muda completamente o jogo.

Até pouco tempo atrás, quando uma linguagem ganhava um recurso novo, o caminho parecia relativamente simples. A documentação era publicada, alguns desenvolvedores começavam a usar, bibliotecas apareciam e, aos poucos, o mercado absorvia aquela novidade.

Agora coloca uma IA no meio desse processo.

Você pede um código em uma versão moderna de Java e ela pode até entregar. Só que existe uma chance enorme de aparecerem padrões antigos, estruturas desnecessárias e aquele cheiro de sistema corporativo que foi criado quando o monitor ainda tinha cinquenta centímetros de profundidade.

Não é porque o modelo odeia Java moderno. É porque ele reconhece padrões a partir do material que recebeu, do contexto que você fornece e das ferramentas que consegue consultar. E linguagens antigas e populares possuem uma vantagem brutal: existe muito código, muita documentação, muita resposta em fórum e muito projeto real disponível.

Uma linguagem nova começa praticamente do zero nessa disputa.

Claro, documentação, busca e contexto podem ajudar bastante. Você pode entregar a especificação inteira para o agente, criar regras no projeto e corrigir a saída. Só que agora você começou a pagar uma taxa.

A taxa de ensinar para a IA aquilo que o ecossistema ainda não conseguiu ensinar sozinho.

E empresa nenhuma escolhe tecnologia olhando apenas para a beleza do código. Ela olha para prazo, contratação, manutenção, risco e, principalmente, para quanto custa colocar alguma coisa funcionando em produção.

É aí que entra a Scarf.

Durante cerca de sete anos, o backend da empresa foi construído principalmente em Haskell. E não era projetinho de final de semana feito só para colocar uma linguagem diferente no currículo.

A API principal usava Haskell. O gateway responsável por uma grande quantidade de downloads de pacotes open source também. Eram sistemas em produção, com disponibilidade real e compromissos contratuais.

E Haskell funcionava.

Esse ponto é importante, porque seria muito fácil contar essa história como se a empresa tivesse escolhido uma linguagem acadêmica, quebrado tudo e finalmente voltado para a realidade.

Só que não foi isso.

O sistema de tipos ajudava a encontrar erros. O código era confiável. A performance atendia. A linguagem obrigava a equipe a modelar o domínio com cuidado.

O problema apareceu ao redor do código.

Compilação, cache, Nix, ambiente de desenvolvimento, integração contínua e toda a estrutura necessária para manter uma base séria em Haskell funcionando.

No melhor cenário, com tudo em cache e uma alteração pequena, a equipe conseguia um ciclo de aproximadamente vinte segundos.

Parece aceitável.

E para um humano, muitas vezes era.

Se você passa uma hora implementando uma funcionalidade e depois espera alguns minutos pela compilação, isso é irritante, mas ainda representa uma parte pequena do trabalho. Você levanta, pega um café, questiona todas as decisões que tomou na carreira e volta para o computador.

Só que um agente não leva uma hora para produzir a primeira tentativa.

Ele pode alterar o código em minutos. E, se depois disso, precisa esperar quinze minutos para criar o ambiente, compilar o projeto e descobrir que inventou um método que não existe, a compilação deixou de ser uma pequena irritação.

Ela virou o gargalo.

Agora multiplica isso por vários agentes trabalhando em paralelo, cada um criando um ambiente descartável, testando uma hipótese e esperando o mesmo projeto ficar pronto.

A economia mudou.

Foi por isso que a Scarf começou a escrever suas novas APIs em Python.

Eles não desligaram o backend em Haskell numa sexta-feira às cinco da tarde e começaram a rezar. Um servidor Python passou a funcionar ao lado do sistema existente. Rotas novas foram para Python e o código antigo continuou rodando enquanto partes do sistema eram migradas aos poucos.

Mesmo assim, foi necessário recriar autenticação, acesso ao banco, modelos compartilhados, imagens de implantação, testes e várias outras coisas que ninguém coloca no post bonito anunciando uma migração.

Historicamente, esse trabalho seria caro demais.

Com os modelos atuais, portar código existente para outra linguagem ficou muito mais barato. Não ficou automático, não ficou livre de erro e definitivamente não virou trabalho para fazer sem revisão. Mas ficou barato o bastante para mudar a decisão.

E percebe a ironia?

Haskell entregava mais garantias antes de o programa rodar. Python entregava um ciclo de alteração e teste muito mais rápido. Com a IA produzindo código e testes em grande volume, a Scarf decidiu que conseguia recuperar parte da segurança com mais validação e, ao mesmo tempo, gastar menos energia brigando com a ferramenta.

Isso significa que Haskell morreu e todo mundo deveria escrever Python?

Não.

Essa seria justamente a conclusão preguiçosa que um vídeo sobre inteligência artificial não deveria produzir.

Tipos continuam importantes. Compiladores continuam encontrando erros que uma IA pode ignorar com a confiança de quem nunca vai receber uma ligação de produção às três da manhã. E quanto mais código os agentes geram, mais valiosas podem se tornar as ferramentas que impedem esse código de fazer besteira.

O ponto é outro.

Uma garantia só ajuda depois que você consegue executar o ciclo completo: alterar, compilar, testar, entender o erro e tentar novamente. Se esse ciclo for caro demais, a segurança técnica começa a perder para a velocidade econômica.

Então a disputa entre linguagens começa a incluir uma nova pergunta.

Quão bem esse ecossistema atende um programador que não é humano?

Ele tem documentação clara? Exemplos suficientes? Dependências previsíveis? Ambiente simples de reproduzir? Compilação rápida? Testes que rodam isoladamente? Erros que uma máquina consegue interpretar?

Porque o agente não sente prazer com uma abstração elegante. Ele não participa da comunidade. Ele não tem carinho pela filosofia da linguagem.

Ele altera o arquivo, executa uma ferramenta e precisa receber uma resposta útil.

Isso pode concentrar ainda mais o mercado nas linguagens que já são grandes. Python, JavaScript, Java, C# e outras opções populares carregam décadas de exemplos e ferramentas prontas.

Mas também existe uma oportunidade para linguagens novas.

Se elas nascerem com documentação pensada para consumo automático, ambientes reproduzíveis, compilação rápida, mensagens de erro boas e ferramentas fáceis de integrar, talvez consigam crescer muito mais rápido do que conseguiriam apenas convencendo desenvolvedores um por um.

No final, a IA não torna a escolha da linguagem irrelevante.

Ela torna essa escolha ainda mais importante.

Só que agora não basta perguntar qual linguagem tem a sintaxe mais bonita, o sistema de tipos mais poderoso ou a comunidade mais apaixonada.

Você também precisa perguntar quanto tempo existe entre uma mudança no código e uma evidência confiável de que aquilo funciona.

Porque a linguagem que vai sobreviver à era dos agentes talvez não seja a mais elegante.

Talvez seja a que consegue dizer “isso está errado” antes que a IA tenha tempo de produzir outras dez mil linhas.

E, sinceramente, olhando para a velocidade com que esse código está sendo gerado, espero que ela responda rápido.

---

## Notas de produção e verificação

- O texto original termina incompleto aos 06:20; a segunda metade deste roteiro foi reconstruída a partir da fonte primária da Scarf.
- O bloco comercial do CodeRabbit foi removido. Recolocar somente se houver patrocínio real e briefing aprovado para o canal.
- A Scarf manteve Haskell em produção e passou a fazer novos trabalhos de API em Python de forma gradual; o sistema anterior continua sendo reduzido à medida que as partes são tocadas.
- O relato da Scarf cita ciclos de aproximadamente 20 segundos no melhor caso e esperas muito maiores em compilações frias ou alterações profundas.
- O suporte a Rust no kernel Linux existe, mas ainda possui restrições por arquitetura e configuração; a referência foi retirada da narração porque não é necessária para sustentar a tese.

### Fontes primárias

- [Avi Press — After 7 years in production, Scarf has reluctantly moved away from Haskell](https://avi.press/posts/2026-07-10-after-7-years-in-production-scarf-has-reluctantly-moved-away-from-haskell.html)
- [Haskell Foundation — Who We Are](https://haskell.foundation/who-we-are/)
- [Linux Kernel Documentation — Rust](https://www.kernel.org/doc/html/latest/rust/general-information.html)

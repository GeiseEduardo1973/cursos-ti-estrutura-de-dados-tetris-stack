💡 Sobre a Autora: 
// Criado por Geise Severo Eduardo
// Trabalho de: Estrutura de dados em C++
// Aluna fazendo dupla graduação em
// CIências da Computação, 3º Sememstre - Matrícula 202501462731
// Engenharia de Software, 3º Semestre - Matrícula 202501534724
// Jogo Tetris Stack  
// Instituição: Estácio

📄 README - Tetris Stack: Nível Novato
🕹️ Tetris Stack - Simulação de Fila de Peças
📝 Descrição:
Desenvolvido para a ByteBros, este sistema gere a "fila de peças futuras" de um jogo de Tetris, garantindo que a ordem de aparecimento das peças respeite a lógica de entrada e saída.
🚀 FuncionalidadesFila Circular: Implementação de uma fila de tamanho fixo (MAX 5) com reaproveitamento de espaço
Operações de Fila:Enqueue: Inserção automática de novas peças ao final da fila.
Dequeue: Remoção da peça da frente para ser "jogada".Peças Dinâmicas: Sistema que gera peças dos tipos 'I', 'O', 'T' e 'L', cada uma com um ID único de criação.Interface Personalizada: Menu interativo com temática visual em tons de rosa (PINK).
🛠️ Tecnologias e ConceitosLinguagem:
 C++Estrutura de Dados: Fila Circular (Circular Queue).
 Modularização: Divisão lógica em funções para inserção, remoção e visualização.
 
 📄 README - Tetris Stack - Nível Aventureiro 
 🕹️Este projeto simula o gerenciamento de peças do jogo Tetris Stack, focado na manipulação de estruturas de dados lineares e circulares. 
 O objetivo é gerenciar peças futuras e uma reserva técnica para o jogador.
 🚀 Funcionalidades:O programa permite realizar as seguintes operações através de um menu interativo:Jogar Peça: Remove a peça que está na frente da fila de espera.Reservar Peça: Move a peça da frente da fila diretamente para o topo da pilha de reserva, desde que haja espaço.Usar Peça Reservada: Remove e utiliza a peça que está no topo da pilha.Geração Automática: Sempre que uma peça sai da fila, uma nova peça é gerada com um ID único para manter a fila sempre cheia.
 🏗️ Estruturas de Dados UtilizadasPara cumprir os requisitos de eficiência e lógica de jogo, foram implementadas:Fila Circular (Peças Futuras):Capacidade: 5 elementos.Lógica: Utilizada para exibir as próximas peças do jogo. A implementação circular permite o reaproveitamento eficiente do espaço no array.
 Pilha Linear (Reserva):Capacidade: 3 elementos.Lógica: Segue o princípio LIFO (Last In, First Out), onde a última peça reservada é obrigatoriamente a primeira a ser usada.
 📋 Atributos das PeçasCada peça dentro do sistema possui as seguintes propriedades:Nome: Um caractere representando o formato ('I', 'O', 'T', 'L').ID: Um identificador numérico único baseado na ordem de criação.
 🛠️ Regras de NegócioPeças removidas (jogadas ou usadas da reserva) saem definitivamente do jogo.A reserva é limitada; se estiver cheia, o jogador não pode enviar novas peças da fila para lá até liberar espaço.O tipo da peça é gerado aleatoriamente pelo sistema

 🕹️ Tetris Stack - Nível Mestre
Este módulo do projeto foca na manipulação avançada de estruturas de dados lineares (Pilha e Fila) para criar mecânicas de inversão de peças.

📋 O que este código faz?
O objetivo principal é demonstrar como inverter a ordem de uma Fila utilizando uma Pilha como intermediária. No contexto do jogo, isso simula um "Bônus de Inversão", onde as peças que estavam para cair têm sua ordem de prioridade espelhada.

🛠️ Estruturas Utilizadas
Struct Peca: A unidade básica do jogo (ID e Nome/Tipo).

Fila (FIFO - First In, First Out):

filaOriginal: Armazena as peças na ordem em que foram geradas.

filaInvertida: Armazena as peças após o processo de inversão.

Pilha (LIFO - Last In, First Out):

auxiliar: Funciona como um "balde" onde as peças são empilhadas para que a última a entrar seja a primeira a sair, causando a inversão natural.

🔄 Passo a Passo da Lógica Mestre
O processo de inversão ocorre em dois momentos principais:

1. Desenfileirar para Empilhar
Retiramos as peças da filaOriginal (quem chegou primeiro sai primeiro) e as colocamos na Pilha auxiliar.

Resultado: A primeira peça da fila agora está no fundo da pilha. A última peça da fila está no topo.

2. Desempilhar para Reenfileirar
Retiramos as peças do topo da Pilha auxiliar e as inserimos na filaInvertida.

Resultado: Como o topo da pilha era a última peça da fila antiga, ela se torna a primeira da fila nova. A ordem foi invertida com sucesso.

⚠️ Garantias de Estabilidade (Safety)
Para evitar que o jogo trave ou feche sozinho, o código inclui:

pilhaCheia / filaCheia: Verificam o limite de memória antes de inserir novos dados.

pilhaVazia / filaVazia: Impedem que o programa tente ler dados que não existem.

🚀 Como Executar
O programa gera automaticamente 5 peças aleatórias.

Exibe a fila na ordem de criação.

Processa a inversão.

Exibe a nova fila com a ordem espelhada.
💡 Sobre a Autora: 
// Criado por Geise Severo Eduardo
// Trabalho de: Estrutura de dados em C++
// Aluna fazendo dupla graduação em
// CIências da Computação, 3º Sememstre - Matrícula 202501462731
// Engenharia de Software, 3º Semestre - Matrícula 202501534724
// Jogo Tetris Stack  - Nivel: Novato
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
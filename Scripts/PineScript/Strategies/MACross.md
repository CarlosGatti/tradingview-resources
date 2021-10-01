Moving Average Studies With MA Crossover Expert Advisor
Este é o código para um Expert Advisor (bot) para a plataforma de negociação algorítmica MetaTrader 5.

Este bot funciona usando a estratégia de cruzamento de média móvel. Quando a média móvel de curto prazo ultrapassa a média de longo prazo, o bot fecha sua posição atual e emite uma ordem de compra. Da mesma forma, quando a média móvel de curto prazo cruza com a média de longo prazo, o bot fecha sua posição atual e emite uma ordem de venda.

O usuário tem permissão para alterar parâmetros de entrada permitindo testar diversas estratégias e acompanhar o movimento do mercado. Também é possivel realizar intervenção manual durante reversões inesperadas do mercado ou até mesmo ajustar a exposição da carteira. Embora este EA tenha sido escrito para explorar rapidamente as opções de gerenciamento de negociação e otimização por meio de backtesting, é muito útil usá-lo com suas configurações preferidas durante a negociação.

Como sempre, não há promessas de lucros ao usar este programa e é trivial configurá-lo para proteger seu dinheiro, acompanhando as perdas e ganhos registrados. A escolha de executar isso em uma conta real é sua, e eu sinceramente espero que você teste suas suposições e condições de negociação primeiro por meio de uma conta demo. Avise-me se encontrar bugs ou possibilidade de melhorias.

Check the code

Close Position
take profit: Quando o preço atinge o objetivo de ganho ganho na operação a ordem deve ser encerrada. O take profit deve ser preenchido conforme a unidade PIP de preenchimento correspondente de cada moeda (0,01) ou (0,0001).

stop loss: Quando o preço atinge o objetivo de perda na operação a ordem deve ser encerrada. O stop loss deve ser preenchido conforme a unidade PIP de preenchimento correspondente de cada moeda (0,01) ou (0,0001).

crossover reverso: Quando a media curta cruzar a media longa no sentido contrário ao sentido inicial da operação a ordem deve encerrada, considerando como uma reversão de tendência.

Open Position :: Settings
MAPeriodShort: Representa a média móvel mais rápida, ou seja, cujo período de avaliação é mais curto. default (9 dias)
MAPeriodLong: Representa a média móvel mais lenta, ou seja, cujo período de avaliação é maior. default (21 dias)
MAShift: Desloca o preço da média para uma melhor visualização do tempo de reação.
MAMethodS: Método Média Móvel Short SMA
MAMethodL: Método Média Móvel Long SMA
MAPrice: Esse parâmetro define o preço que será calculado para efeito da média. O valor padrão está o preço do fechamento.
magicNum: O magic number é utilizado para identificação do bot, e não interferir em operações de outros.
desvPts: Desvio em pontos.
preenchimento: Preenchimento da ordem.
stopLoss: Define o risco de perda em PIPs.
takeProfit: Define o objetivo de ganho em PIPs para a operação.
lote: Define a alavancagem que será utilizada.
gatilhoBE: O gatilho para o BreakEven é o ponto que acionará o recurso.
stepTS: Representa o step para o Trailing Stop.
horaInicioAbertura: Este parâmetro é responsável por habilitar o início das execução de ordens automáticas. Representa a hora início da abertura das negociações.
minutoInicioAbertura: Este parâmetro é responsável por habilitar o início das execução de ordens automáticas. Representa o minuto início da abertura das negociações.
horaFimAbertura: Este parâmetro é responsável por habilitar o fim das execução de ordens automáticas. Representa a hora fim das negociações.
minutoFimAbertura: Este parâmetro é responsável por habilitar o fim das execução de ordens automáticas. Representa o minuto fim das negociações.
horaInicioFechamento: Este parâmetro é responsável por determinar o fim das ordens pendentes. Representa a hora que as negociações abertas serão encerradas.
minutoInicioFechamento: Este parâmetro é responsável por determinar o fim das ordens pendentes. Representa o minuto que as negociações abertas serão encerradas.
Testing and Optimization
Este programa avaliará apenas se deve abrir uma nova negociação no início de uma nova barra. Se você quiser verificar a cada minuto, coloque-o em um gráfico definido para o período de 1 minuto. Se você quiser verificar uma vez por semana, defina o cronograma do gráfico para 1 semana. Isso também significa que o backtesting em "cada tick" é praticamente inútil durante o teste exploratório. A avaliação de fechar ou não negociações ocorre a cada tick. Você deve usar a opção de usar "apenas barras abertas" para fazer testes exploratórios pesados e, em seguida, restringir para "pontos de controle" ou "cada tick" para obter os preços de saída mais próximos da realidade histórica. Honestamente, usar o modo visual do testador enquanto "pontos de controle" é selecionado ajudará você a definir quais configurações você deseja muito mais rápido do que a força bruta percorrer todas as permutações de configurações possíveis aqui.
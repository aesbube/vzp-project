# Проект по Визуелно програмирање 
# TicTacToe (Икс-Нула)

### Проблем
TicTacToe, односно Икс-Нула е веќе добро позната игра која е наменета за двајца играчи. Во оваа игра главниот проблем се состои од утврдување на победник од еден од играчите или прогласување на нерешено, така што се следат потезите на играчите и се ажурира состојбата на играта. Исходот се наоѓа со проверка дали успешно еден од играчите ги усогласил своите 3 знаци - „Х“ или „О“ хоризонтално, вертикално или дијагонално во 3х3 матрица. Доколку матрицата е пополнета, а не се усогласени знаците, тогаш играта завршува како нерешена. 

### Имплементација
При започнување на играта се отвора прозорче каде што е потребно да се внесат имињата на играчите (Player 1 и Player 2) и бројот на рунди кои што ќе се одиграат помеѓу тие двајца играчи. Дадени се и две копчиња "Cancel Game" - кое што ја гаси играта и "Start Game" за почеток на игра, но за ова копче воопшто да може да се кликне мора да се внесат имињата на двајцата играчи. Откако ќе ја започнеме играта се отвора нов прозорец на кој се наоѓа матрицата со девет полиња кои може да се кликнат со цел да се постави одреден знак. На десната страна од прозорецот е Player Turn - кој играч е на ред да постави знак, моменталната рунда која што се игра и бројот на победени рунди по играч. На овој прозорец се наоѓаат и две копчиња, од кои едното е за прекин на играта при што клик отвора уште едно прозорче кое прашува дали сме сигурни, а другото е за почеток на нова игра со нови играчи и се гаси моменталната игра. За секоја победена рунда играч добива плус 1 поен, а за нерешена рунда никој не добива поени.  Победник на играта е тој кој што има повеќе рунди победено и истиот се прикажува на крајот во Message Box. 

### Oпис на класа
Класата TicTacToe  се грижи за иницијализацијата на играта, управувањето со играчите, управувањето со рундите и корисничките интеракции преку графичкиот кориснички интерфејс. Класата има својства како што се Player1, Player2, Winner, currentRound, matrix, buttons, game, Sign, SignChar, Turn, TilesLeft како и bool својства за управување со состојбата на играта и апликацијата. Конструкторот ја иницијализира формата и играта, додека InitializeGame() поставува нова игра. Event Handler-от TicTacToe_Load() започнува нова рунда и ги ажурира лабелите, а updateLabels() го ажурира корисничкиот интерфејс со моменталната состојба на играта. Методот TicTacToe_FormClosing() бара потврда од корисникот пред да ја затвори играта, а NewGame() започнува нова игра по потврда од страна на корисникот. Методот StartRound() ја ресетира таблата за игра и ажурира кој играч е следен. Методот AddButtons() додава копчиња на таблата за игра и поставува хендлери при кликнување. Методот isWonGame() проверува за победнички услов, а SetWinner() го поставува победникот на рундата и го ажурира бројот на неговите победи. Методот isGameOver() проверува дали играта ги достигнала максималните рунди и го одредува крајниот победник, додека isTieGame() проверува за нерешен резултат. Еvent handler-от Tile_Click() ја ажурира таблата за игра, проверува за услови на победа или нерешен резултат и го управува текот на играта. Методот QuitGame_Click() се грижи за барањето на корисникот да ја напушти играта, а NewGameButton_Click() се грижи за барањето на корисникот за започнување на нова игра. 

### Слики
![](https://github.com/5ar100/TicTacToe/assets/116762358/3ac2b5f6-da83-427d-880b-70008b3a2129)

![](https://github.com/5ar100/TicTacToe/assets/116762358/94990c4f-0b1c-4c00-b3ab-a2efbbec0862)

![](https://github.com/5ar100/TicTacToe/assets/116762358/79345033-fd1c-4700-b54e-5c51af78519f)

![](https://github.com/5ar100/TicTacToe/assets/116762358/e188e03e-ab96-4b84-b1c0-8776c2f71a9f)

![](https://github.com/5ar100/TicTacToe/assets/116762358/cab4bbae-f9de-4d84-ac70-afe415de1ea3)

![](https://github.com/5ar100/TicTacToe/assets/116762358/c3f8d057-33cd-44e4-80c0-d8ade3fb44bb)

![](https://github.com/5ar100/TicTacToe/assets/116762358/64a41d8c-75d2-4715-9ddc-31265a300836)

![](https://github.com/5ar100/TicTacToe/assets/116762358/ad74e9d8-9df9-4736-b6f1-5212a1206628)

![](https://github.com/5ar100/TicTacToe/assets/116762358/90bdad9a-137a-4a47-9799-276be43848c2)

![](https://github.com/5ar100/TicTacToe/assets/116762358/66f25a9c-7a27-47c4-b457-a03169b42b05)


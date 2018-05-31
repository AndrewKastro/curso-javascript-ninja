# Desafio da semana #3

```js
// Declarar uma variável qualquer, que receba um objeto vazio.
?

var object = {};

/*
Declarar uma variável `pessoa`, que receba suas informações pessoais.
As propriedades e tipos de valores para cada propriedade desse objeto devem ser:
- `nome` - String
- `sobrenome` - String
- `sexo` - String
- `idade` - Number
- `altura` - Number
- `peso` - Number
- `andando` - Boolean - recebe "falso" por padrão
- `caminhouQuantosMetros` - Number - recebe "zero" por padrão
*/
?

var people = {
	nome: 'Andrew',
	sobrenome: 'Castro',
	sexo: 'Masculino',
	idade: 22,
	altura: 1.75,
	peso: 83.5,
	andando: false,
	caminhouQuantosMetros: 0 
};

/*
Adicione um método ao objeto `pessoa` chamado `fazerAniversario`. O método deve
alterar o valor da propriedade `idade` dessa pessoa, somando `1` a cada vez que
for chamado.
*/
?

people.fazerAniversario = function(){
	people.idade++;
};

/*
Adicione um método ao objeto `pessoa` chamado `andar`, que terá as seguintes
características:
- Esse método deve receber por parâmetro um valor que representará a quantidade
de metros caminhados;
- Ele deve alterar o valor da propriedade `caminhouQuantosMetros`, somando ao
valor dessa propriedade a quantidade passada por parâmetro;
- Ele deverá modificar o valor da propriedade `andando` para o valor
booleano que representa "verdadeiro";
*/
?

people.andar = function(metrosCaminhados){
		people.caminhouQuantosMetros += metrosCaminhados;
		people.andando = true;
};

/*
Adicione um método ao objeto `pessoa` chamado `parar`, que irá modificar o valor
da propriedade `andando` para o valor booleano que representa "falso".
*/
?

people.parar = function(){
	people.andando = false;
};

/*
Crie um método chamado `nomeCompleto`, que retorne a frase:
- "Olá! Meu nome é [NOME] [SOBRENOME]!"
*/
?

function nomeCompleto(){
	return 'Olá! Meu nome é ' + people.nome + ' ' + people.sobrenome + '!';
};

/*
Crie um método chamado `mostrarIdade`, que retorne a frase:
- "Olá, eu tenho [IDADE] anos!"
*/
?

people.mostrarIdade = function(){
	return 'Ola, eu tenho ' + people.idade + 'anos!';
};

/*
Crie um método chamado `mostrarPeso`, que retorne a frase:
- "Eu peso [PESO]Kg."
*/
?

people.mostrarPeso = function(){
	return 'Eu peso ' + people.peso + 'Kg.';
};

/*
Crie um método chamado `mostrarAltura` que retorne a frase:
- "Minha altura é [ALTURA]m."
*/
?

people.mostrarAltura = function(){
	return 'Minha altura é ' + people.altura + 'm.';
};

/*
Agora vamos brincar um pouco com o objeto criado:
Qual o nome completo da pessoa? (Use a instrução para responder e comentários
inline ao lado da instrução para mostrar qual foi a resposta retornada)
*/
?

nomeCompleto(); //"Olá! Meu nome é AndrewCastro!"

/*
Qual a idade da pessoa? (Use a instrução para responder e comentários
inline ao lado da instrução para mostrar qual foi a resposta retornada)
*/
?

people.mostrarIdade(); //"Ola, eu tenho 22anos!"

/*
Qual o peso da pessoa? (Use a instrução para responder e comentários
inline ao lado da instrução para mostrar qual foi a resposta retornada)
*/
?

people.mostrarPeso(); //"Eu peso 83.5Kg."

/*
Qual a altura da pessoa? (Use a instrução para responder e comentários
inline ao lado da instrução para mostrar qual foi a resposta retornada)
*/
?

people.mostrarAltura(); //"Minha altura é 1.75m."

/*
Faça a `pessoa` fazer 3 aniversários.
*/
?

people.fazerAniversario();
people.fazerAniversario();
people.fazerAniversario();

/*
Quantos anos a `pessoa` tem agora? (Use a instrução para responder e
comentários inline ao lado da instrução para mostrar qual foi a resposta
retornada)
*/
?

people.mostrarIdade(); //"Ola, eu tenho 25anos!"

/*
Agora, faça a `pessoa` caminhar alguns metros, invocando o método `andar` 3x,
com metragens diferentes passadas por parâmetro.
*/
?

people.andar(25);
people.andar(20);
people.andar(15);

/*
A pessoa ainda está andando? (Use a instrução para responder e comentários
inline ao lado da instrução para mostrar qual foi a resposta retornada)
*/
?

people.andando; //true

/*
Se a pessoa ainda está andando, faça-a parar.
*/
?

people.parar();

/*
E agora: a pessoa ainda está andando? (Use uma instrução para responder e
comentários inline ao lado da instrução para mostrar a resposta retornada)
*/
?

people.andando; //false

/*
Quantos metros a pessoa andou? (Use uma instrução para responder e comentários
inline ao lado da instrução para mostrar a resposta retornada)
*/
?

people.caminhouQuantosMetros //60

/*
Agora vamos deixar a brincadeira um pouco mais divertida! :D
Crie um método para o objeto `pessoa` chamado `apresentacao`. Esse método deve
retornar a string:
- "Olá, eu sou o [NOME COMPLETO], tenho [IDADE] anos, [ALTURA], meu peso é [PESO] e, só hoje, eu já caminhei [CAMINHOU QUANTOS METROS] metros!"

Só que, antes de retornar a string, você vai fazer algumas validações:
- Se o `sexo` de `pessoa` for "Feminino", a frase acima, no início da
apresentação, onde diz "eu sou o", deve mostrar "a" no lugar do "o";
- Se a idade for `1`, a frase acima, na parte que fala da idade, vai mostrar a
palavra "ano" ao invés de "anos", pois é singular;
- Se a quantidade de metros caminhados for igual a `1`, então a palavra que
deve conter no retorno da frase acima é "metro" no lugar de "metros".
- Para cada validação, você irá declarar uma variável localmente (dentro do
método), que será concatenada com a frase de retorno, mostrando a resposta
correta, de acordo com os dados inseridos no objeto.
*/
?

// Agora, apresente-se ;)
?
```
people.apresentacao = function() {
		
		var sexoX = 'eu sou o';
		var idadeX = 'anos';
		var metroX = 'metros';

		if(people.sexo == 'Feminino'){
			sexoX = 'eu sou a';
		}
		if(people.idade == 1){
			idadeX = 'ano';
		}
		if(people.caminhouQuantosMetros == 1){
			metroX = 'metro';
		}
		return  'Olá, eu sou o ' + people.nome+ ' ' + people.sobrenome + ', tenho ' + people.idade+ ' ' + idadeX +', ' +  people.altura + ', meu peso é ' + people.altura + ' e, só hoje, eu já caminhei ' + people.caminhouQuantosMetros + ' ' + metroX + '!';
	};
  
  /*
people.sexo = 'Feminino';
"Feminino"
people.idade = 1;
1
people.caminhouQuantosMetros = 1;
1
people.apresentacao();

"Olá, eu sou o Andrew Castro, tenho 1 ano, 1.75, meu peso é 1.75e, só hoje, eu já caminhei 1 metro.!"
*/

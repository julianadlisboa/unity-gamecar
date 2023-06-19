# unity-gamecar
Projeto da cena em 3d de um jogo.

criando movimentação do carro

Utilizei um carro 3d dos assets da loja, faremos com que ele se movimente na cena.

CRIAÇÃO DA CENA
1. adiciona um quad para fazer o solo
2. para montar a pista, foi usado assests prontos, encaixei as pistas formando um circuito.
3. montei uma bandeira usando um cubo e um quad, coloquei textura de cor e do desenho da bandeira.
4. coloquei alguns itens para personalizar a pista, como power ups e barreiras.
5. criei obstaculos com cilindros

//script do carro
1. após importar o carro no unity, arraste o carro na cena
2. coloque rigid body no carro e colisores na roda 
3. altere a massa, suspensão e radius do carro 
4. Script->
    4.1. declare as variáveis. Motorforce, Steerforce, Brakeforce( força do motor,  força do volante e força do freio). Coloque as variáveis designando as rodas.
   
 //pegando os gatilhos do teclado    
    4.2. Para o carro andar, na vertical, o carro irá para frente multiplica pela força do motor. Faça a mesma coisa para a horizontal e multiplique pela força do volante. 
(para cima e para baixo)(esquerda e direita)

//rodas
     4.3. as rodas traseiras iram acelerar o carro e as da frente vão virar. Então para as traseiras  colocamos motortorque para dar força ao objeto, recebem v porque ou acelera ou freia. Agora para as da frente giram para um lado ou para o outro por isso usamos o SteerAngle(gira no eixo y) e recebem o h.
     
//colocando o freio

//zera a força do freio após soltar a te la espaço 

     4.4. Se eu pressionar o espaço vai freiar.
( if(input.getkey(keycode.space))). 
Nas ridas traseiras trocamos por braketorque e vai receber o brakeforce.
Tudo isso quando pressiona,logo, quando eu soltar o carro deve parar. 
Para isso msntem o mesmo código de cima, mude o GetKey para GetKeyDown e coloque invés de v, zero.

//freia o carro se não tiver nenhuma tecla pressionada
        4.5. Quando eu soltar o dedo da seta de acelerar também deve parar se não vai acelerar pra sempre. Para isso, ( if(input.getaxis(vertical)==0), então se não tiver pressionado nenhuma tecla deve parar.
   

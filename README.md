# Projeto de Troca Automática de Câmeras (Apenas para Aprendizado)

Este projeto tem como objetivo automatizar a troca de câmeras em um estúdio(ObsStudio) de streaming. A ideia é que, ao exibir uma imagem com um QR Code em um dos cantos da tela, a pessoa que estiver assistindo possa escanear o código e fazer um pagamento para selecionar qual câmera será exibida em seguida.

O funcionamento é simples: ao fazer um pagamento de determinado valor, ex: R$ 1,09 um contador de tempo é iniciado por 1 minuto e o qrcode desativado para permitir que a pessoa possa trocar de câmera novamente somente após o fim do contador. Além disso, o valor do centavos determina qual câmera será exibida, nesse caso, será exibido a câmera 9.

Para automatizar a troca de câmeras, o projeto utiliza as teclas do computador para enviar comandos ao software de streaming. Dessa forma, quando uma pessoa faz um pagamento e escolhe uma nova câmera, o software recebe o comando e faz a troca automaticamente.

Esperamos que este projeto possa ser útil para quem busca uma forma de monetizar transmissões ao vivo e também para quem deseja criar experiências interativas para seus espectadores. Fique à vontade para utilizar e adaptar este projeto de acordo com suas necessidades.

## Como usar

Para utilizar este projeto, é necessário ter um software de streaming configurado em um computador com acesso à internet. Além disso, é preciso ter uma conta em um serviço de pagamento online para receber os pagamentos realizados pelos espectadores.

Para configurar o projeto, siga os seguintes passos:

1. Faça o download dos arquivos deste repositório e extraia-os para uma pasta em seu computador.
2. Abra o arquivo `config.json` e edite as seguintes informações:
   - `payment_service`: o nome do serviço de pagamento que você está utilizando (ex: PayPal, PagSeguro, etc).
   - `payment_value_table`: uma tabela com os valores dos pagamentos e as câmeras correspondentes. Exemplo: `{ "1.09": 9, "2.50": 2, "5.00": 5 }`.
   - `keyboard_shortcuts`: as teclas do teclado que devem ser utilizadas para trocar as câmeras. Exemplo: `{ "1": "ctrl+1", "2": "ctrl+2", "3": "ctrl+3", "4": "ctrl+4", "5": "ctrl+5", "6": "ctrl+6", "7": "ctrl+7", "8": "ctrl+8", "9": "ctrl+9" }`.
3. Salve o arquivo `config.json` e execute o arquivo `main.py`.
4. Exiba uma imagem com o QR Code em um dos cantos da tela e aguarde que os espectadores façam os pagamentos e escolham as câmeras.
5. Ao receber um pagamento, o software irá trocar automaticamente para a câmera correspondente e iniciar um contador de tempo para permitir que o espectador faça uma nova troca.
6. Quando o tempo acabar, o espectador poderá fazer uma nova escolha e o processo se repete.

Caso você encontre algum problema ou tenha sugestões de melhorias para o projeto, fique à vontade para abrir uma nova issue ou submeter um pull request

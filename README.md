#Passos para construção do container.

1- Baixar o código (git clone)

2- Entrar localmente na pasta conversao-temperatura\src

3- Criar a imagem > Executar o comando "docker image build -t jpzanini/conversao-temperatura:tag"

4- Subir o container > Executar o comando "docker run -p 8080:8080 jpzanini/conversao-temperatura:tag"

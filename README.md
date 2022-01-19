#Passos para construção do container.

1- Baixar o código (git clone)

2- Entrar localmente na pasta conversao-temperatura\src

3- Criar a imagem > Executar o comando "docker image build -t jpzanini/conversao-temperatura:tag"

4- Subir o container > Executar o comando "docker run -p 8080:8080 jpzanini/conversao-temperatura:tag"

#Passos para subir o container no Kubernetes

1- clonar o repositorio para a sua maquina local (git clone)

2- entrar localmente na pasta conversao-temperatura\src

3- Criar a imagem > Executar o comando "docker image build -t jpzanini/conversao-temperatura:tag"

4- Subir o container para o seu repositorio > Executar o comando "docker push jpzanini/conversao-temperatura:tag"

5- Criar o seu cluster > Executar o comando "k3d cluster create mycluster --agents 3 --servers 3 -p "8080:30000@loadbalancer" "

6- Subir para a pasta conversao-temperatura e aplicar o arquivo de deployment > Executar o comando "kubectl apply -f deployment.yaml"

# Como transferir uma instância Amazon EC2 para outra conta

Não é possível transferir instâncias existentes entre contas da AWS, mas é possível compartilhar imagens EC2 entre contas e então criar instâncias a partir dessas imagens.

# Passo a passo
1. Criar uma AMI personalizada: 
> - Acesse a listagem de instâncias EC2
> - Clique com o botão direito do mouse sobre a instância > Image > ```Create Image```.

2. Compartilhe a AMI com a conta de destino.
> - Acesse a listagem de AMIs
> - Clique com o botão direito do mouse sobre a AMI criada > ```Modify Image Permissions```.
> - No campo ```AWS Account Number```, adicione o número da conta alvo e clique em ```Save```.

* Obs: o número de conta (AWS Account Number) pode ser encontrado no menu ```My account```.

3. Na conta de destino, encontre a AMI.
> - Clique no meu IMAGES > AMIs
> - Altere o primeiro filtro de ```Owned by``` me para ```Private images```.

4. Inicie uma nova instância a partir da AMI compartilhada com a conta destino.

# Caso a AMI não tenha aparecido.
Provavelmente a causa desse problema é por conta da região em que a AMI foi criada e a região da conta destino em que se deseja subir uma instãncia a partir da AMI. Para resolvar isso é necessário copiar a AMI para outra região.
1. Clique com o botão direito sobre a AMI > ```Copy AMI```.
2. Selecione a nova região.
3. Clique no botão ```Copy AMI```.

[< Voltar](../README.md)


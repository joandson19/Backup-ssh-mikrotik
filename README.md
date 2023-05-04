*Requisitos para o mkbkp.sh funcionar*

# Instale o sshpass e unzip
apt install sshpass -y
apt install unzip -y

Entre no arquivo mkbkp.sh e altere as variaveis de TOKEN e CHAT_ID do telegram, após é só rodar o comando como no exemplo abaixo
# ./mkbkp "IP" "USER" "SENHA"

O script irá acessar seu mikrotik e irá primeiramente coletar o nome do seu equipamento usado o comando "/system identity print", com isso ele irá acessar pela segunda vez gerando o arquivo de backup, e na terceira vez ele irá acessar novamente de scp para baixar o arquivo para uma pasta temporaria para daí compactar e após enviar via para o telegram. Por fim ele irá remover o arvivo que agora já não é mais necessário. 

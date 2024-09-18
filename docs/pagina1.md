# Passo 1: Instalar o VirtualBox e Criar uma VM Linux

## Baixe e instale o VirtualBox:
1. Acesse o [site oficial do VirtualBox](https://www.virtualbox.org/) e baixe o instalador para Windows.
2. Siga as instruções de instalação.

## Baixe uma ISO de uma distribuição Linux:
1. Por exemplo, Ubuntu Server pode ser baixado do [site oficial do Ubuntu](https://ubuntu.com/download/server).

## Crie uma nova VM no VirtualBox:
1. Abra o VirtualBox e clique em "Novo".
2. Dê um nome à VM (por exemplo, "ServidorWeb") e escolha "Linux" como o tipo e "Ubuntu (64-bit)" como a versão.
3. Alocação de memória: 2 GB (2048 MB) é suficiente para um servidor básico.
4. Crie um disco rígido virtual: 20 GB é suficiente para começar.
   - Selecione a opção para usar um arquivo de disco virtual (VDI) e opte por alocação dinâmica.

## Instale o Linux na VM:
1. Selecione a VM criada e clique em "Iniciar".
2. Quando solicitado, selecione a ISO do Ubuntu Server que você baixou.
3. Siga as instruções na tela para instalar o Ubuntu Server na VM.

# Passo 2: Configurar a VM com Apache, MkDocs e WordPress

## Acesse a VM via SSH ou diretamente pelo console do VirtualBox:
- Se estiver usando o console, basta iniciar a VM.
- Para acessar via SSH, você pode configurar a rede da VM para usar um adaptador de rede em modo bridge ou NAT com portas encaminhadas.

## Atualize o sistema:
```sh
sudo apt update
sudo apt upgrade

## Instale o Apache

```sh
sudo apt install apache2
sudo systemctl start apache2
sudo systemctl enable apache2

# Instale o Mkdocs

```sh 
sudo apt install python3-pip
pip3 install mkdocs


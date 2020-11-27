<h1 align="center">
<br>
  <img src="https://github.com/OtavioAL/LTSP/blob/main/logo.jpg" alt="" width="500">
<br>
<br>
Terminais leves com LTSP
</h1>

<p align="center">O LTSP é um conjunto de serviços que proporcionam um ambiente de terminais leves e de baixo custo, conectado a um servidor que se encarrega de processar todas as aplicações e exibi-las no monitor do cliente.
Vagrant é um software de código aberto para criar e manter ambientes de desenvolvimento virtuais portáteis, utilizando VirtualBox.
O vagrant foi utilizado para simplificar a instalação e configuração do ambiente.</p>

## Getting started

<h3>Instalação</h3>

- Clonar o repositorio;

- Configurar o arquivo settings.sh;

- Definir seu ip no LAN_IP;

- Definir sua interface de rede no LAN_IF;

- Em STANDALONE="no" o servidor não oferece serviço DHCP aos clientes e presupoem que exista um servidor DHCP na rede;

- Em STANDALONE="yes" o proprio servidor fornece o serviço DHCP aos clientes;

- Executar o comando vagrant up no terminal.

## License

This project is licensed under the MIT License - see the [LICENSE](https://opensource.org/licenses/MIT) page for details

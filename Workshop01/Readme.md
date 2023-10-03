# Workshop 01 - Bookworm con Vagrant 

## Instalacion de Virtual Box 

Para instalar Virtual Box.
- [Descargar Virtual Box](https://www.virtualbox.org/wiki/Downloads)

## Instalacion De Vagrant 
- [Descargar Vagrant](https://developer.hashicorp.com/vagrant/downloads?product_intent=vagrant)

## Aprovicionar Maquina Vagrant

Una vez descargado e instalado vangrant se deberá de aprovisionar  una instancia de la maquina que se dese en este caso será Debian Bookworm 64 Bits  
```bash
vagrant  init debian/bookworm64

```
**Pero:** 
 > Recordemos que los sistemas operativos  Debian se encuentran por versiones y en el siguiente enlace los podrán encontrar todas las versiones , además muchas **Boxes **que proporciona vagrant.
- [Descargar Boxes de Vagagrant](https://app.vagrantup.com/boxes/search)


### Edicion del Vagrantfile
Primero se debe abrir el archivo desde la consola que estes utilizando
>Esta opción la puedes realizar con tu editor y consola de preferencia, para este ejemplo se usará visual estudio y desde **Bash** se abre el archivo con el siguiente comando 

```bash 
code vagrantfile
```

Luego editamos el vagrant file, hablitando la red privada con la ip 192.168.56.10 vamos a editar 
y descomentar la linea para que de esta manera la red sea funcional para la maquina
```bash
config.vm.network "private_network", ip: "192.168.56.10"

```
Antes de lanzar el vagrant file se debe de habilitar la ip asignada en el virtualizador 

 ![Configuracion de VBoxNet](./Images/Capture.PNG "Box red")
### Iniciamos la maquina
Comando respectivo
```bash 
vagrant up
```

De esta manera tendremos una maquina virtual debian funcional con unos simples pasos

 ![Configuracion de VBoxNet](./Images/Capture2.PNG "Box red")

Para apagar la maquina
 ```bash 
vagrant halt
```


Con esto estaria terminado el aprovisionamiento del equipo de desarrollo 
 ## Algunos comandos útiles 

| Comandos      | 
| ------------- |
| cd            |
|ls             |
|mkdir          |
|pwd            |
|mv             |
|tree or tree.com|
|ls -la         |
|code           |
|pin            |
|ssh            |
|exit           |
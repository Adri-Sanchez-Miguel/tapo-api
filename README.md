# tapo-api
Código en Rust para extraer información de los enchufes inteligentes TAPO P110. 

## Instalación

Si se instala en una Raspberry Pi limpia, tras actualizar e instalar todas las librerías, hará falta tener instalado "Rust", "open-ssl" y "arp-scan" en el dispositivo. 

```bash
sudo apt update
sudo apt upgrade

curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
sudo apt install libssl-dev
sudo apt install arp-scan
```

## Ejecución

Para su ejecución, habrá que establecer las variables de entorno "TAPO_USERNAME", "TAPO_PASSWORD" y "MONGODB_URI" (consultar con el autor, para añadir también la IP del dispositivo a las permitidas). 

```bash
export TAPO_USERNAME=
export TAPO_PASSWORD=
export MONGODB_URI=

cargo build
cargo run --example tapo_p110_multiple
```

Creada por Adrián Sánchez-Miguel para el grupo de investigación MAmI.

# Blockchain-Smart-Contracts

Repositorio correspondiente al Trabajo Práctico de la materia Tecnologías Emergentes

## Requerimientos:

Se deberá instalar truffle y ganache (globalmente o en el directorio del proyecto):

```

$ npm install -g truffle ganache

```

## Pasos:

Para ejecutar el programa, se deberán seguir los siguientes pasos:

- Ejecutar el Front-End realizado en React:

```

$ npm run start

```

- Abrir una terminal y ejecutar ganache:

```

$ ganache

```

- 10 Addresses con sus respectivas private keys van a ser generadas. Copiamos la primera private key, y la importamos a la extensión Metamask en la opción de "Importar cuenta".
- Consecuentemente, conectamos Metamask a la red que estamos usando en Ganache. Donde nos figura la red principal de Ethereum, elegimos la opción agregar red y luego agregar red manualmente. En nombre de Red insertamos "GanacheConsole" por ejemplo. En "Nueva dirección URL de RPC" ingresamos la información respectiva que se encuentre en el archivo truffle-config.js. En identificador de cadena insertamos el Chain ID que nos entrega Ganache. Por último, en Símbolo Moneda, simplemente ingresamos ETH. Guardamos esta configuración.
- Luego, descomentamos la información necesaria del archivo de truffle-config.js:

```

development: {

host:  "127.0.0.1", // Localhost (default: none)

port:  8545, // Standard Ethereum port (default: none)

network_id:  "*", // Any network (default: none)

},

```

- A posteriori, en una nueva terminal, nos localizamos en el directorio de truffle y ejecutamos:

```

$ truffle migrate --network development

```

- Finalmente, tiramos abajo el Front-End y lo volvemos a correr con el mismo comando descrito anteriormente.

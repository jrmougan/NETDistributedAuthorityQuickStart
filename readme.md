# Explica aquí os métodos e variables dos seguintes scripts:

## ConnectionManager.cs
### Variables
- _profileName: nome do xogador
- _sessionName: nome da sesión
- _maxPlayers: número máximo de xogadores por sesión
- _state: estado da conexión
- _session: sesión actual
- m_NetworkManager: Referencia ao compoñente NetworkManager asociado ao obxecto ao que está asociado este script

### Métodos
- Awake: método asíncrono que inicializa os servizos de Unity e obtén o compoñente NetworkManager
- OnSessiónOwnerPromoted: callback que se invoca cando un cliente é promovido a propietario (owner)

- OnClientConnectedCallback: callback que se invoca cando un cliente se conecta

- OnGUI: Método para xerar interfaz cos inputs para introducir nome de xogador e de sesión

- OnDestroy: método que se invoca ao destruir o obxecto, co obxetivo de que o xogador abandone a sesión.

- CreateOrJoinSessionAync: método asíncrono que xestiona a autenticación e creación de sesións


## PlayerCubeController.cs

### Variables

- Speed: velocicade

- ApplyVerticalInputToZAxius: booleano para configurar a entrada vertical, si se debe aplicar no eixe z en lugar de no y.

- m_motion: Vecto3 que almacena os vectores de movemento introducidos polo usuario

### Métodos

- Update: método que se executa en cada fotograma, onde se comproba a autoridade antes de mover o obxeto de xogador correspondente.

# Explica os compoñentes seguintes do GameObject `NetworkManager`:

## Network Manager
Compoñente que xestiona a configuración de rede no xogo.

## Unity Transport
Protocolo de comunicación empregado no compoñente NetworkManager, netes caso é un protocolo propio de Unity

## Connection Manager
Compoñente personalizado que xestiona as conexións dos clientes e servidores, manexando eventos de conexión, desconexión e aprobación de conexións

# Explica os compoñentes seguintes do Prefab `PlayerCube`:

## Network Object
Compoñente que permite utilizar un GameObject como un obxecto en rede.

## Player Cube Controller
Script que controla o comportamento do cubo do xogador, xestionando o movemento e outras interaccións segundo as entradas do usuario e a lóxica do xogo.
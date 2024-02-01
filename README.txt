Este es el port de  MiST a POSEIDON de una reconstrucción de un Apple ][e de la década de 1980 (mejorado) implementado en VHDL para FPGA.
El proyecto se basa en una implementación Apple ][+ FPGA.
Original for the DE2: http://www1.cs.columbia.edu/~sedwards/apple2fpga/
Port for the MiST: http://ws0.org/tag/apple2/

Características:
- Selección de archivos de disco .NIB mediante OSD (lectura/escritura)
- Carga de cinta a través del pin UART RX
- CPU 6502 o 65C02 seleccionable
- Soporte para joystick
- Salida RGB (opcionalmente escaneada para VGA) o YPbPr
- Monitor color, ámbar, verde y blanco y negro
- Base de 64K + RAM auxiliar de 64K con 80 columnas y soporte doble de alta resolución
- Mockingboard modelo A (dos chips AY-3-8913 para seis canales de audio) en la ranura 4

En la pantalla de inicio "Apple //e", abra el OSD con F12 y elija un disco NIB. arrancará
el disco automáticamente. Utilice dsk2nib para convertir imágenes de disco AppleII en imágenes .nib.
La implementacion de disco es lectura. y escritura.

Si pulsas restetr (el botón derecho en MiST), entrará en Applesoft con el mensaje ].
Desde aquí tienes el Applesoft BASIC. Ver: http://www.landsnail.com/a2ref.htm
Si deseas iniciar otro disco, elige una imagen .nib a través del osd y escribe lo siguiente:

]PR#6

or

]CALL -151
*C600G

El comando CALL entrará al Monitor. Escribe la llamada por segunda vez si el mensaje * no aparece
mostrar la primera vez.
En el Monitor también puedes escribir 6 y luego Ctrl-P seguido de retorno.
Ver http://vectronicsappleworld.com/appleii/dos.html#bootdos

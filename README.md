# SISTEMAS-OPERATIVOS-_COMANDOS

printf "%s %s %s\n" "$(date '+%d-%m-%Y %H:%M')" "$(whoami)" "$(hostname)"
Salida Esperada:    11-11-2026 21:49 epbrow serveresbrow
echo $(date '+%d-%m-%Y %H:%M') $(whoami) $(hostname)
Salida Esperada:    11-11-2026 21:49 epbrow serveresbrow



mkdir -p PrimerCiclo/{"Sistemas Operativos","Redes de Datos","Lenguaje y Comunicacion"}
mkdir PrimerCiclo/Sistemas\ Operativos/{"U1","U2"} && mkdir PrimerCiclo/Redes\ de\ Datos/{"U1","U2"} && mkdir PrimerCiclo/Lenguaje\ y\ Comunicacion/{"U1","U2"}

Salida esperada
PrimerCiclo
├── Lenguaje y Comunicacion
│   ├── U1
│   └── U2
├── Redes de Datos
│   ├── U1
│   └── U2
└── Sistemas Operativos
    ├── U1
    └── U2

    
mkdir PrimerCiclo/Redes\ de\ Datos/U1/{"Actividades","Practicas","Evaluaciones"} && mkdir PrimerCiclo/Redes\ de\ Datos/U2/{"Actividades","Practicas","Evaluaciones"}
tree PrimerCiclo

Salida esperada 

PrimerCiclo
├── Lenguaje y Comunicacion
│   ├── U1
│   └── U2
├── Redes de Datos
│   ├── U1
│   │   ├── Actividades
│   │   ├── Evaluaciones
│   │   └── Practicas
│   └── U2
│       ├── Actividades
│       ├── Evaluaciones
│       └── Practicas
└── Sistemas Operativos
    ├── U1
    └── U2


touch PrimerCiclo/Redes\ de\ Datos/U1/Actividades/{"AltaA1","MediaA1","BajaA1"} && touch PrimerCiclo/Redes\ de\ Datos/U2/Evaluaciones/{"AltaA1","MediaA1","BajaA1"} && touch PrimerCiclo/Redes\ de\ Datos/U2/Practicas/{"AltaA1","MediaA1","BajaA1"}
tree PrimerCiclo
Salida Esperada 
PrimerCiclo
├── Lenguaje y Comunicacion
│   ├── U1
│   └── U2
├── Redes de Datos
│   ├── U1
│   │   ├── Actividades
│   │   │   ├── AltaA1
│   │   │   ├── BajaA1
│   │   │   └── MediaA1
│   │   ├── Evaluaciones
│   │   └── Practicas
│   └── U2
│       ├── Actividades
│       ├── Evaluaciones
│       │   ├── AltaA1
│       │   ├── BajaA1
│       │   └── MediaA1
│       └── Practicas
│           ├── AltaA1
│           ├── BajaA1
│           └── MediaA1
└── Sistemas Operativos
    ├── U1
    └── U2

16 directories, 9 files


tar -cvf Copia.PrimerCiclo_$(date '+%d%m%Y_%H%M%S').tar.gz PrimerCiclo

tar -cvf Parcial01_$(date '+%d%m%Y_%H%M%S').tar.gz "PrimerCiclo/Redes de Datos" "PrimerCiclo/Sistemas Operativos"
Salida esperada
PrimerCiclo/Redes de Datos/
PrimerCiclo/Redes de Datos/U1/
PrimerCiclo/Redes de Datos/U1/Actividades/
PrimerCiclo/Redes de Datos/U1/Actividades/AltaA1
PrimerCiclo/Redes de Datos/U1/Actividades/MediaA1
PrimerCiclo/Redes de Datos/U1/Actividades/BajaA1
PrimerCiclo/Redes de Datos/U1/Practicas/
PrimerCiclo/Redes de Datos/U1/Evaluaciones/
PrimerCiclo/Redes de Datos/U2/
PrimerCiclo/Redes de Datos/U2/Actividades/
PrimerCiclo/Redes de Datos/U2/Practicas/
PrimerCiclo/Redes de Datos/U2/Practicas/AltaA1
PrimerCiclo/Redes de Datos/U2/Practicas/MediaA1
PrimerCiclo/Redes de Datos/U2/Practicas/BajaA1
PrimerCiclo/Redes de Datos/U2/Evaluaciones/
PrimerCiclo/Redes de Datos/U2/Evaluaciones/AltaA1
PrimerCiclo/Redes de Datos/U2/Evaluaciones/MediaA1
PrimerCiclo/Redes de Datos/U2/Evaluaciones/BajaA1
PrimerCiclo/Sistemas Operativos/
PrimerCiclo/Sistemas Operativos/U1/
PrimerCiclo/Sistemas Operativos/U2/


ls
Copia.PrimerCiclo_11112026_214510.tar.gz  Parcial01_11112026_214700.tar.gz  PrimerCiclo


Se requiere listar todas las carpetas que contengan prácticas, por ejemplo, deberían aparecer, todas las carpetas que contengan el texto “práctica”

Comando Utilizado:   find PrimerCiclo -type d -name "Pra*"

Salida Esperada
PrimerCiclo/Redes de Datos/U1/Practicas
PrimerCiclo/Redes de Datos/U2/Practicas



Comando Utilizado:    find PrimerCiclo -type d -name "Pra*"

Salida Esperada
PrimerCiclo/Redes de Datos/U1/Practicas
PrimerCiclo/Redes de Datos/U2/Practicas


Comando Utilizado:     find PrimerCiclo -type f -name "Me*"
Salida Esperada

PrimerCiclo/Redes de Datos/U1/Actividades/MediaA1
PrimerCiclo/Redes de Datos/U2/Practicas/MediaA1
PrimerCiclo/Redes de Datos/U2/Evaluaciones/MediaA1


Comando Utilizado:     find . -type d -name "*[1-2]"
Salida Esperada

./PrimerCiclo/Sistemas Operativos/U1
./PrimerCiclo/Sistemas Operativos/U2
./PrimerCiclo/Redes de Datos/U1
./PrimerCiclo/Redes de Datos/U2
./PrimerCiclo/Lenguaje y Comunicacion/U1
./PrimerCiclo/Lenguaje y Comunicacion/U2


Comando Utilizado:     find . -type d -name "*[U][2]"
Salida Esperada

./PrimerCiclo/Sistemas Operativos/U2
./PrimerCiclo/Redes de Datos/U2
./PrimerCiclo/Lenguaje y Comunicacion/U2


Comando Utilizado:    find PrimerCiclo -type f -name "B*"
Salida Esperada

PrimerCiclo/Redes de Datos/U1/Actividades/BajaA1
PrimerCiclo/Redes de Datos/U2/Practicas/BajaA1
PrimerCiclo/Redes de Datos/U2/Evaluaciones/BajaA1


Para agregar nombres de los compañeros:

nano PrimerCiclo/Sistemas\ Operativos/U1/estudiantes.txt
tree PrimerCiclo
PrimerCiclo
├── Lenguaje y Comunicacion
│   ├── U1
│   └── U2
├── Redes de Datos
│   ├── U1
│   │   ├── Actividades
│   │   │   ├── AltaA1
│   │   │   ├── BajaA1
│   │   │   └── MediaA1
│   │   ├── Evaluaciones
│   │   └── Practicas
│   └── U2
│       ├── Actividades
│       ├── Evaluaciones
│       │   ├── AltaA1
│       │   ├── BajaA1
│       │   └── MediaA1
│       └── Practicas
│           ├── AltaA1
│           ├── BajaA1
│           └── MediaA1
└── Sistemas Operativos
    ├── U1
    │   └── estudiantes.txt
    └── U2


cat PrimerCiclo/Sistemas\ Operativos/U1/estudiantes.txt
Karen Peñafiel
Justin Neira
Carlos Jerves
Jose Ochoa
Jorge Orellana

tail -n 3 PrimerCiclo/Sistemas\ Operativos/U1/estudiantes.txt
Carlos Jerves
Jose Ochoa
Jorge Orellana

head -n 4 PrimerCiclo/Sistemas\ Operativos/U1/estudiantes.txt
Karen Peñafiel
Justin Neira
Carlos Jerves
Jose Ochoa


Para buscar los apellidos: 
cut -f 2 -d " " PrimerCiclo/Sistemas\ Operativos/U1/estudiantes.txt
Peñafiel
Neira
Jerves
Ochoa
Orellana


Guarde los apellidos de los compañeros un archivo llamado apellidos.txt en la carpeta
Comandos Utilizados
cut -f 2 -d " " PrimerCiclo/Sistemas\ Operativos/U1/estudiantes.txt > PrimerCiclo/Lenguaje\ y\ Comunicacion/U1/ape
tree PrimerCiclo

Resultado a Obtener: 
PrimerCiclo
├── Lenguaje y Comunicacion
│   ├── U1
│   │   └── apellidos.txt
│   └── U2
├── Redes de Datos
│   ├── U1
│   │   ├── Actividades
│   │   │   ├── AltaA1
│   │   │   ├── BajaA1
│   │   │   └── MediaA1
│   │   ├── Evaluaciones
│   │   └── Practicas
│   └── U2
│       ├── Actividades
│       ├── Evaluaciones
│       │   ├── AltaA1
│       │   ├── BajaA1
│       │   └── MediaA1
│       └── Practicas
│           ├── AltaA1
│           ├── BajaA1
│           └── MediaA1
└── Sistemas Operativos
    ├── U1
    │   └── estudiantes.txt
    └── U2

16 directories, 11 files

cat PrimerCiclo/Lenguaje\ y\ Comunicacion/U1/apellidos.txt
Peñafiel
Neira
Jerves
Ochoa
Orellana




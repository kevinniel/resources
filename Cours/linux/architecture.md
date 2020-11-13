# Architecture des fichiers

```bash
\
├── bin
|   ├── cd
|   ├── nano
|   ├── mv
|   └── ...      //contient les commandes de LINUX
|
├── boot   // système pour le lancement
|   ├── grub
|   └── ... -amd64
|
├── dev      //périphériques
|   ├── stdin
|   ├── stdout
|   ├── cdrom
|   └── ...
|
├── etc   //configuration système
|   ├── sudoers
|   ├── sudoers.d
|   └── ...
|
├── home
|   ├── lost+found     // ne peut pas être ouvert
|   └── osboxes        // nom de l'utilisateur
|       ├── Desktop
|       ├── Documents
|       └── ...        // contient fichiers perso du user
|
├── mnt
|
├── opt
|
├── proc
|   └── ... // tous les fichiers temp de processus
|
├── root  // répertoire admin système
|
├── run    // fichiers pour l'execution
|   ├── alsa
|   ├── cup
|   └── ...
|
├── srv
|
├── sys   // fonctionnalité système
|   ├── block
|   ├── bus
|   ├── class
|   ├── dev
|   ├── device
|   ├── firmware
|   ├── fs
|   ├── hypervisor
|   ├── kernel
|   ├── module
|   └── power
|
├── tmp
|   └── ...  // Fichiers temporaires
|
├── usr
|   ├── bin
|   ├── games
|   ├── include
|   ├── lib
|   ├── lib32
|   ├── lib64
|   ├── libexec
|   ├── libx32
|   ├── local
|   ├── sbin
|   ├── share
|   └── src
|
└── var // données variables
```
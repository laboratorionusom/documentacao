---
description: Neste tutorial iremos compilar o pure-data versão vanilla no Raspberry Pi.
---

# Compilando Pure Data vanilla no RPi



**Válido para o** [**Raspbian Buster with Desktop**](https://www.raspberrypi.org/downloads/raspbian/)**.**

No momento em que este tutorial foi escrito, a versão mais recente do Pure data é a 0.51-4, é a versão que instalaremos com este tutorial.

  


**PASSO 2** - Crie um diretório com código fonte e entre nele \(opcional\):

```bash
mkdir src && cd src
```

**PASSO 3** - Instale as dependências para compilação e baixe o pure data 0.50-2:

```bash
sudo apt install build-essential autoconf automake libtool gettext git libasound2-dev libjack-jackd2-dev libfftw3-3 libfftw3-dev tcl tk
```

```text
wget http://msp.ucsd.edu/Software/pd-0.51-4.src.tar.gz
```

**PASSO 4** - Descompacte o código fonte baixado e entre no diretório com o código fonte:

```bash
tar -xzf pd-0.51-4.src.tar.gz
```

```text
cd pd-0.51-4
```

**PASSO 5** - Configure e compile:

```text
./autogen.sh
```

```text
./configure --enable-jack --enable-fftw
```

```text
make
```

**PASSO 6** - Após terminar a compilação, vamos abrir o pd compilado pra conferir se está funcionando:

```text
cd bin
```

```text
./pd
```

**PASSO 7** - Se o Pure-data funcionou direitinho, é hora de instalá-lo no sistema:

```text
cd ..
```

```text
sudo make install
```

Toda vez que quiser abrir o pure-data  que você compilou, basta abrir o terminal \(Passo 1\) e digitar: 

```text
pd
```


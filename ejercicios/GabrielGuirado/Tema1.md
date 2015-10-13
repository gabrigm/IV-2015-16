## __Ejercicio 1.__ 

__Consultar en el catálogo de alguna tienda de informática el precio de un ordenador tipo servidor y calcular su coste de amortización a cuatro y siete años. Consultar este artículo en Infoautónomos sobre el tema.__

Para este ejercicio tomaré como ejemplo el pc HP ENVY PHOENIX 810-304NS de pcgreen cuyo precio es de 1946,38 € y que aparece en el siguiente enlace:

<center> <http://www.pcgreen.com/hp-envy-phoenix-810-304ns-776813-p.htm> </center>

Su precio sin IVA pasa a ser de 1608,58 € y queremos saber su coste amortizándolo en 4 y 7 años. 

Podemos hacer una amortización de muchas formas. En mi caso, en ambos casos amortizaré el pc amortizando el mismo porcentaje cada año; sin embargo, en el de 4 años lo haré suponiendo que la compra la realizo el 1 de enero y en el de 7 años a fecha 1 de octubre.
  
<center> <u>Amortización en 4 años.<u> </center>

Fecha de compra: 1 de enero.

Porcentaje equitativo (100/4=25%).

1608,58 * 0,25 = 402,15 €

*Cada año se amortizan 402,15 €.*

<center> <u>Amortización en 7 años.<u> </center>

Fecha de compra: 1 de octubre.

Porcentaje hasta primer fin de año(2 meses): (100/7/12*2=2,38%).
Porcentaje próximos 6 años: (100/7=14,29%)
Porcentaje último año de sólo los 10 primeros meses:(100/7/12*10=11,9%)

*El primer año(sólo 2 meses) se amortizarían: 1608,58 * 0,238 = 38,27 €*

*Los próximos 6 años se marotizarían: 1608,58 * 0,1429 = 229,78 €*

*El último año (sólo 10 meses) se amortizan: 1608,58 * 0,119 = 191,42 €*

## __Ejercicio 2.__ 

__Usando las tablas de precios de servicios de alojamiento en Internet y de proveedores de servicios en la nube, Comparar el coste durante un año de un ordenador con un procesador estándar (escogerlo de forma que sea el mismo tipo de procesador en los dos vendedores) y con el resto de las características similares (tamaño de disco duro equivalente a transferencia de disco duro) en el caso de que la infraestructura comprada se usa sólo el 1% o el 10% del tiempo.__

Tanto el servidor dedicado como el servicio cloud se contratarán desde la web <https://www.1and1.es>.


<center> <u>Ordenador con procesador estándar.<u> </center>

Tal y como se muestra en el siguiente [aquí][1]:

 [1]: https://www.1and1.es/costs?__lf=Order-Tariff&__sendingdata=1&cart.action=add&cart.ignoreFlow=true&cart.article=tariff-toggle-second&__forcestop=true&__CMD[costs]:SELWRP=cart
 
__Servidor o12A-64 + SSD__

* AMD Opteron™ 6338P

* 12 Cores x 2,3 GHz

* 64 GB de RAM 

* DDR3 ECC

* 4.000 GB 

* (2 x 4.000 GB SATA)

* Ubuntu Server 14.04 LTS básico (64 bit)

* Disco duro SSD 240 GB (2 x 240 GB SSD) Intel S3500

El contrato maximo de permanencia es de 6 meses a 104,99 € cada uno(629,94 €). 

A partir de aquí cada mes tendria un coste 129,99 € y lo queremos otros 6 meses para cumplir el año (779,94€ en total).

Si ademas le añadimos otros 99 € por el alta del servicio, *lo más barato que nos puede salir un año es de 1508,88 €.*


<center> <u>Servicio cloud.<u> </center>

Tal y como se muestra en el siguiente [enlace][2]:

[2]: https://www.1and1.es/costs?__reuse=1444153597167&__lf=Order-Product

* vCores: 12 x 2,0 GHz

* Memoria RAM: 32 GB RAM

* Disco Duro: 360 GB

* Sistema operativo: Linux Ubuntu 14.04 (64 bit) 

Con este servicio nos regalan un mes y el resto nos saldría a 249,99 €(2749,89 € en total).

*Usándolo un 1%, el precio sería de 27,50 € al año.*

*Usándolo un 10%, el precio sería de 274,99 € al año.*

Vistos los resultados queda muy claro el gran ahorro que obtenemos contratando un servicio cloud.


## __Ejercicio 3.__

__¿Qué tipo de virtualización usarías en cada caso? Comentar en el foro__

Para trabajar durante poco tiempo con SO's o probarlos para comprobar su funcionamiento yo siempre he preferido la virtualización plena. Así no necesito tener instalado un SO concreto y las ocasiones en que lo necesite puedo virtualizarlo rápidamente con todas sus funciones.

Por otro lado, para la programación web y de aplicaciones considero muy recomendable la vitualización de aplicaciones y de escritorio. Así es mucho más cómodo trabajar desde el lado del servidor y del cliente por separado.

## __Ejercicio 4.__ 

__Comprobar si el procesador o procesadores instalados tienen estos flags. ¿Qué modelo de procesador es? ¿Qué aparece como salida de esa orden?__

Al ejecutar la orden <u>egrep '^flags.*(vmx|svm)' /proc/cpuinfo</u> en mi pc no aparece ningún flag puesto que mi ordenador es un procesador celeron con 1 GB de RAM y, por tanto, no posee ninguna de las tecnologías x86: VT-x de Intel ni AMD-V.

Al ejecutar la orden *cat /proc/cpuinfo* se pueden ver las especificaciones de la CPU localizadas(todas) en el archivo cpuinfu:

processor	: 0

vendor_id	: GenuineIntel

cpu family	: 6

model		: 22

model name	: Intel(R) Celeron(R) CPU          540  @ 1.86GHz

stepping	: 1

microcode	: 0x16

cpu MHz		: 1861.988

cache size	: 1024 KB

physical id	: 0

siblings	: 1

core id		: 0

cpu cores	: 1

apicid		: 0

initial apicid	: 0

fdiv_bug	: no

f00f_bug	: no

coma_bug	: no

fpu		: yes

fpu_exception	: yes

cpuid level	: 10

wp		: yes

flags		: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss tm pbe nx lm constant_tsc arch_perfmon pebs bts aperfmperf pni dtes64 monitor ds_cpl tm2 ssse3 cx16 xtpr pdcm lahf_lm dtherm

## __Ejercicio 5.__ 

### __Apartado 1__

__Comprobar si el núcleo instalado en tu ordenador contiene este módulo del kernel usando la orden kvm-ok.__

El núcleo de mi ordenador no tiene isntalado ni puede usar la infraestructura KVM y no puede usar la aceleración por harware.

gabrigm@gabri:~$ kvm-ok

INFO: Your CPU does not support KVM extensions

INFO: For more detailed results, you should run this as root

HINT:   sudo /usr/sbin/kvm-ok

gabrigm@gabri:~$ sudo /usr/sbin/kvm-ok

[sudo] password for gabrigm: 

INFO: Your CPU does not support KVM extensions

KVM acceleration can NOT be used


### __Apartado 2__

__Instalar un hipervisor para gestionar máquinas virtuales, que más adelante se podrá usar en pruebas y ejercicios.__



El hipervisor instalado en mi ordenador ha sido virtualbox desde la web <http://virtualbox.org>.

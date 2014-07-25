---
layout: post
title:  "Performance Digital Ocean"
date:   2013-07-28 07:00:00
---

Suite aux benchmarks réalisés par [petitchevalroux](dev.petitchevalroux.net/hebergement/test-vps-benchmark-serveurs-virtuels.389.html), j'ai décidé d'utiliser la même méthode pour tester mon nouvel hébergement chez Digital Ocean.

Voici les caractéristiques de l'instance :

512MB / 1 CPU
20GB SSD DISK
1TB TRANSFER
Bandwith: 1Gb/sec
Distribution Ubuntu 13.04 x64
Region : Amsterdam 1
Monthly $5.00 Hourly: $0.007

Processeur

{% highlight bash %}
root@bench:~# cat /proc/cpuinfo
processor    : 0
vendor_id    : GenuineIntel
cpu family    : 6
model        : 2
model name    : QEMU Virtual CPU version 1.0
stepping    : 3
microcode    : 0x1
cpu MHz        : 2299.998
cache size    : 4096 KB
fpu        : yes
fpu_exception    : yes
cpuid level    : 4
wp        : yes
flags        : fpu de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pse36 clflush mmx fxsr sse sse2 syscall nx lm rep_good nopl pni vmx cx16 popcnt hypervisor lahf_lm
bogomips    : 4599.99
clflush size    : 64
cache_alignment    : 64
address sizes    : 40 bits physical, 48 bits virtual
power management:
{% endhighlight %}

Score UnixBench : 1466.4

Performances des disques dur : 2373

Performance CPU : 1609

# info parque machine

pour avoir des info cpu

```bash
cat /proc/cpuinfo| grep "model name" | uniq
```

pour avoir des info memoire

```bash
dmidecode --type 17 | grep Type  | grep DDR | sort | uniq
dmidecode --type 17 | grep Speed | sort | uniq
dmidecode --type 17 | grep Size  | sort | uniq
```

## NewTahiti

IP:
CPU: model name	: Pentium(R) Dual-Core  CPU      E5200  @ 2.50GHz
RAM:
* Type: DDR2
* Speed: 800 MT/s
* Size: 1024 MB + 2048 MB

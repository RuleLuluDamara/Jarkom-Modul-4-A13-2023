# Jarkom-Modul-4-A13-2023
## Laporan Resmi Pengerjaan Praktikum Jaringan Komputer

| No. | Anggota               | NRP          |
|-----|----------------------------|--------------|
| 1   | Rule Lulu Damara           | 5025211050   |

## Topologi
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/5aca9611-3dee-4fca-a9e2-f4b9fc73644e)

## Rute 
Berikut merupakan rute subner yang digunakan pada praktikum berikut : 
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/4d3458c0-4c97-4181-ab46-08bd28a6f917)

## Prefix IP
Prefix IP yang digunakan adalah ```bash 192.175.x.x```

## VLSM
## Topologi 
Berikut merupakan topologi yang digunakan dalam metode VLSM dengan GNS3:
![WhatsApp Image 2023-12-05 at 04 17 29_b943d86c](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/f8a60f0d-6e56-4033-91cf-040ca149cbf3)

## Tree VLSM
Berikut merupakan tree yang digunakan dalam metode VLSM:
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/076daf96-ed83-4647-be1e-bab7526acfed)

## Pembagian IP 
Berikut merupakan Ppemabgian IP yang digunakan dalam metode VLSM dengan GNS3:
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/2149f68e-5080-4c92-a1cf-92daf0aad037)

## Konfigurasi Network VLSM
## Subneting

- AURA
```bash
auto eth0
iface eth0 inet dhcp
up iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 192.175.0.0/19

auto eth1
iface eth1 inet static
	address 192.175.24.125
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.175.24.129
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 192.175.24.133
	netmask 255.255.255.252

```
- FREIREN
```bash
auto eth0
iface eth0 inet static
	address 192.175.24.126
	netmask 255.255.255.252
	gateway 192.175.24.125
	up echo nameserver 192.122.168.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.175.24.65
	netmask 255.255.255.224

auto eth2
iface eth2 inet static
	address 192.175.24.121
	netmask 255.255.255.252
```

- FLAMME
```bash
auto eth0
iface eth0 inet static
	address 192.175.24.122
	netmask 255.255.255.252
	gateway 192.175.24.121
	up echo nameserver 192.122.168.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.175.24.113
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.175.8.1
	netmask 255.255.252.0

auto eth3
iface eth3 inet static
	address 192.175.24.117
	netmask 255.255.255.252
```

- FERN
```bash
auto eth0
iface eth0 inet static
	address 192.175.24.114
	netmask 255.255.255.252
	gateway 192.175.24.113
	up echo nameserver 192.122.168.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.175.0.1
	netmask 255.255.248.0
```

- HIMMEL
```bash
auto eth0
iface eth0 inet static
	address 192.175.24.118
	netmask 255.255.255.252
	gateway 192.175.24.117
	up echo nameserver 192.122.168.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.175.24.97
	netmask 255.255.255.248
```

-EISEN
```bash
auto eth0
iface eth0 inet static
	address 192.175.24.134
	netmask 255.255.255.252
	gateway 192.175.24.133
	up echo nameserver 192.122.168.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.175.24.105
	netmask 255.255.255.248

auto eth2
iface eth2 inet static
	address 192.175.24.137
	netmask 255.255.255.252

auto eth3
iface eth3 inet static
	address 192.175.24.141
	netmask 255.255.255.252

auto eth4
iface eth4 inet static
	address 192.175.23.1
	netmask 255.255.255.0
```

- LINIE
```bash
auto eth0
iface eth0 inet static
	address 192.175.24.142
	netmask 255.255.255.252
	gateway 192.175.24.141
	up echo nameserver 192.122.168.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.175.24.145
	netmask 255.255.255.252

auto eth2
iface eth2 inet static
	address 192.175.24.149
	netmask 255.255.255.252
```

- LAWINE
```bash
auto eth0
iface eth0 inet static
	address 192.175.24.146
	netmask 255.255.255.252
	gateway 192.175.24.145
	up echo nameserver 192.122.168.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.175.24.1
	netmask 255.255.255.192
```

- HEITER
```bash
auto eth0
iface eth0 inet static
	address 192.175.24.147
	netmask 255.255.255.192
	gateway 192.175.24.145
	up echo nameserver 192.122.168.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.175.12.1
	netmask 255.255.252.0
```

- LUGNER
```bash
auto eth0
iface eth0 inet static
	address 192.175.24.150
	netmask 255.255.255.252
	gateway 192.175.24.149
	up echo nameserver 192.122.168.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.175.16.1
	netmask 255.255.252.0

auto eth2
iface eth2 inet static
	address 192.175.23.1
	netmask 255.255.255.0

```

- DANKEN
```bash
auto eth0
iface eth0 inet static
	address 192.175.24.130
	netmask 255.255.255.252
	gateway 192.175.24.129
	up echo nameserver 192.122.168.1 > /etc/resolv.conf

auto eth1
iface eth1 inet static
	address 192.175.22.1
	netmask 255.255.255.0

```

## Routing
- AURA
```bash
#Kanan
route add -net 192.175.24.64 netmask 255.255.255.224 gw 192.175.24.126
route add -net 192.175.24.116 netmask 255.255.255.252 gw 192.175.24.126
route add -net 192.175.24.112 netmask 255.255.255.252 gw 192.175.24.126
route add -net 192.175.24.120 netmask 255.255.255.252 gw 192.175.24.126
route add -net 192.175.0.0 netmask 255.255.248.0 gw 192.175.24.126
route add -net 192.175.8.0 netmask 255.255.252.0 gw 192.175.24.126
route add -net 192.175.24.96 netmask 255.255.255.248 gw 192.175.24.126

#Kiri
route add -net 192.175.22.0 netmask 255.255.255.0 gw 192.175.24.130

#Bawah
route add -net 192.175.24.104 netmask 255.255.255.248 gw 192.175.24.134
route add -net 192.175.24.136 netmask 255.255.255.252 gw 192.175.24.134
route add -net 192.175.24.140 netmask 255.255.255.252 gw 192.175.24.134
route add -net 192.175.24.0 netmask 255.255.255.192 gw 192.175.24.134
route add -net 192.175.12.0 netmask 255.255.252.0 gw 192.175.24.134
route add -net 192.175.20.0 netmask 255.255.254.0 gw 192.175.24.134
route add -net 192.175.24.144 netmask 255.255.255.252 gw 192.175.24.134
route add -net 192.175.23.0 netmask 255.255.255.0 gw 192.175.24.134
route add -net 192.175.16.0 netmask 255.255.252.0 gw 192.175.24.134
route add -net 192.175.24.148 netmask 255.255.255.252 gw 192.175.24.134
```

- FIREREN
```bash
route add -net 192.175.24.120 netmask 255.255.255.252 gw 192.175.24.122
route add -net 192.175.0.0 netmask 255.255.248.0 gw 192.175.24.122
route add -net 192.175.8.0 netmask 255.255.252.0 gw 192.175.24.122
route add -net 192.175.24.116 netmask 255.255.255.252 gw 192.175.24.122
route add -net 192.175.24.96 netmask 255.255.255.248 gw 192.175.24.122
```

- FLAMME
```bash
route add -net 192.175.0.0 netmask 255.255.255.252 gw 192.175.24.114
route add -net 192.175.24.96 netmask 255.255.255.252 gw 192.175.24.118
```

- EISEN
```bash
route add -net 192.175.24.144 netmask 255.255.255.252 gw 192.175.24.142
route add -net 192.175.24.0 netmask 255.255.255.192 gw 192.175.24.142
route add -net 192.175.12.0 netmask 255.255.252.0 gw 192.175.24.142
route add -net 192.175.20.0 netmask 255.255.254.0 gw 192.175.24.142

route add -net 192.175.23.0 netmask 255.255.255.0 gw 192.175.24.150
route add -net 192.175.16.0 netmask 255.255.252.0 gw 192.175.24.150
```

- LINIE
```bash
route add -net 192.175.24.0 netmask 255.255.255.192 gw 192.175.24.146
route add -net 192.175.12.0 netmask 255.255.252.0 gw 192.175.24.146
```

- LAWINE
```bash
route add -net 10.2.12.0 netmask 255.255.252.0 gw 10.2.24.2
```

## CIFUGURASI CLIENT 
- LAKEKORIDOR
```bash
auto eth0
iface eth0 inet static
	address 192.175.24.66
	netmask 255.255.255.224
	gateway 192.175.24.65
	up echo nameserver 192.122.168.1 > /etc/resolv.conf
```

- LAUBHILLS
```bash
auto eth0
iface eth0 inet static
	address 192.175.0.2
	netmask 255.255.248.0
	gateway 192.175.0.1
	up echo nameserver 192.122.168.1 > /etc/resolv.conf
```

- APETITEREGION
```bash
auto eth0
iface eth0 inet static
	address 192.175.0.3
	netmask 255.255.248.0
	gateway 192.175.0.1
	up echo nameserver 192.122.168.1 > /etc/resolv.conf
```

- ROHRROAD
```bash
auto eth0
iface eth0 inet static
	address 192.175.8.2
	netmask 255.255.252.0
	gateway 192.175.8.1
	up echo nameserver 192.122.168.1 > /etc/resolv.conf
```

- ROHRROAD
```bash
auto eth0
iface eth0 inet static
	address 192.175.24.98
	netmask 255.255.255.248
	gateway 192.175.24.97
	up echo nameserver 192.122.168.1 > /etc/resolv.conf
```

- RICHTER
```bash
auto eth0
iface eth0 inet static
	address 192.175.24.106
	netmask 255.255.255.248
	gateway 192.175.24.105
	up echo nameserver 192.122.168.1 > /etc/resolv.conf
```

- REVOLTE
```bash
auto eth0
iface eth0 inet static
	address 192.175.24.107
	netmask 255.255.255.248
	gateway 192.175.24.105
	up echo nameserver 192.122.168.1 > /etc/resolv.conf
```

- BREDREGION
```bash
auto eth0
iface eth0 inet static
	address 192.175.24.2
	netmask 255.255.255.192
	gateway 192.175.24.1
	up echo nameserver 192.122.168.1 > /etc/resolv.conf
```

- SEIN
```bash
auto eth0
iface eth0 inet static
	address 192.175.12.2
	netmask 255.255.252.0
	gateway 192.175.12.1
	up echo nameserver 192.122.168.1 > /etc/resolv.conf
```

- REIGELCANYON
```bash
auto eth0
iface eth0 inet static
	address 192.175.12.3
	netmask 255.255.252.0
	gateway 192.175.12.1
	up echo nameserver 192.122.168.1 > /etc/resolv.conf
```

- GRANZCHANNEL
```bash
auto eth0
iface eth0 inet static
	address 192.175.20.2
	netmask 255.255.254.0
	gateway 192.175.20.1
	up echo nameserver 192.122.168.1 > /etc/resolv.conf
```

- GRABFOREST
```bash
auto eth0
iface eth0 inet static
	address 192.175.23.2
	netmask 255.255.255.0
	gateway 192.175.23.1
	up echo nameserver 192.122.168.1 > /etc/resolv.conf
```

- TURKREGION
```bash
auto eth0
iface eth0 inet static
	address 192.175.16.2
	netmask 255.255.252.0
	gateway 192.175.16.1
	up echo nameserver 192.122.168.1 > /etc/resolv.conf
```

- STARK
```bash
auto eth0
iface eth0 inet static
	address 192.175.24.138
	netmask 255.255.255.252
	gateway 192.175.24.137
	up echo nameserver 192.122.168.1 > /etc/resolv.conf
```

- WILEREGION
```bash
auto eth0
iface eth0 inet static
	address 192.175.22.3
	netmask 255.255.255.252
	gateway 192.175.22.1
	up echo nameserver 192.122.168.1 > /etc/resolv.conf
```

- ROYALCAPITAL
```bash
auto eth0
iface eth0 inet static
	address 192.175.22.2
	netmask 255.255.255.252
	gateway 192.175.22.1
	up echo nameserver 192.122.168.1 > /etc/resolv.conf
```

## Testing
Berikut testing dengan melakukan ping:
![WhatsApp Image 2023-12-05 at 04 20 58_739b4c32](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/31c6a30e-7d31-411f-9ee9-3baa6432ef00)


## CIDR
## Topologi 
Berikut merupakan topologi yang digunakan dalam metode CIDR dengan CPT
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/df220014-cfe3-4142-8c02-6c6fbf0d9710)

## Tree CIDR
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/d76319c4-a721-4db1-a731-6d67cbacb2eb)

## Penggabungan IP
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/db644d2c-3ca3-4cbd-a697-f796ec4fd46a)

![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/b7f020d6-a855-42cc-8f2c-f89f7d0aa15b)

## pembagian IP
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/22b78ba4-f68c-4ef9-a172-e61ed09d9b16)

## SUBNETING
- LAUBHILLS
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/f38f5ddf-7a61-43fe-ba3e-d4b56f348142)

- APPETITREGION
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/33724dbf-8e2c-42e1-bc79-df2abde9c118)

- ROHRROAD
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/3c10ccc1-8812-41b0-9574-8decf3119ec1)

- SCHWERMOUNTAINS
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/5562009e-a3b6-42ac-8d63-4fbfa94e5159)

- LAKEKORIDOR
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/355235d9-e63d-4e11-a78e-5002050e5a1c)

- ROYALCAPITAL
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/0c52dfa5-27e1-4f34-b7db-7d25f8ba9972)

- WILLEREGION
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/27daff35-0e20-4405-a761-d80d652377af)

- RITCHER
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/7dd3f479-e3b3-466d-ad22-fb05741d4283)

- REVOLTE
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/2b08a481-a9b1-4731-b592-d0648d160b93)

- STARK
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/1f961146-003b-4912-9eec-370f005e07ef)

- TURKREGION
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/83492976-f492-4d7f-9a6b-04cbbb21e40c)

- GROBEFOREST
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/c9b5a412-89c8-4fb6-aa1b-390a9bb0536c)

- GRANZCHANNEL
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/828f25e2-f068-4ac3-9ebe-155b76b5a773)

- BREDTREGION
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/1256587a-326b-462c-b3ad-d40e88473cdb)

- SEIN
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/5b2b0d05-af35-4b50-a405-98b31086b966)

- REIGEL CANYON
  
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/31ab7dc4-4105-4577-b594-348dbbc5892a)


## Routing
- AURA
```bash
192.178.0.0/24 via 192.178.1.2
192.177.64.0/27 via 192.177.128.2
192.177.32.0/30 via 192.177.128.2
192.175.144.0/30 via 192.176.0.2
192.175.136.0/30 via 192.176.0.2
192.175.64.0/29 via 192.176.0.2
192.175.32.0/30 via 192.176.0.2
192.177.8.0/30 via 192.177.128.2
192.177.0.0/21 via 192.177.128.2
192.177.16.0/22 via 192.177.128.2
192.177.20.8/30 via 192.177.128.2
192.177.20.0/29 via 192.177.128.2
192.175.128.0/26 via 192.176.0.2
192.175.123.0/24 via 192.176.0.2
192.177.16.0/23 via 192.176.0.2
192.175.8.0/30 via 192.176.0.2
192.175.4.0/26 via 192.176.0.2
192.175.0.0/22 via 192.176.0.2
```

- FREIREN
```bash
0.0.0.0/0 via 192.177.128.1
192.177.16.0/22 via 192.177.32.2
192.177.8.0/30 via 192.177.32.2
192.177.0.0/21 via 192.177.32.2
192.177.20.8/30 via 192.177.32.2
192.177.20.0/29 via 192.177.32.2
```

- FLAMME
```bash
0.0.0.0/0 via 192.177.32.1
192.177.0.0/21 via 192.177.8.2
192.177.20.0/29 via 192.177.20.10
```

- FERN
```bash
0.0.0.0/0 via 192.177.8.1
```

- HIMMEL
```bash
0.0.0.0/0 via 192.177.20.9
```

- DENKEN
```bash
0.0.0.0/0 via 192.178.1.1
```

- EISEN
```bash
0.0.0.0/0 via 192.176.0.1
192.175.128.0/26 via 192.175.136.2
192.175.123.0/24 via 192.175.136.2
192.177.16.0/23 via 192.175.32.2
192.175.8.0/23 via 192.175.32.2
192.175.4.0/26 via 192.175.32.2
192.175.0.0/22 via 192.175.32.2
```

- LUGNER
```bash
0.0.0.0/0 via 192.175.136.1
```

- LINIE
```bash
0.0.0.0/0 via 192.175.32.1
192.175.4.0/26 via 192.175.8.2
192.175.0.0/22 via 192.175.8.2
```

- LAWINE
```bash
0.0.0.0/0 via 192.175.8.1
192.175.0.0/22 via 192.175.4.3
```

- HEITER
```bash
0.0.0.0/0 via 192.175.4.1
```

## TESTING
Berikut testing dengan melakukan ping 
![image](https://github.com/RuleLuluDamara/Jarkom-Modul-4-A13-2023/assets/105763198/8aea3a9a-d022-4487-af3c-161e9689f798)

## KENDALA
- Nguli

<h1 align="center">Laporan Praktikum 4 Kelompok C09 Jarkom C</h1>

---

Anggota Kelompok:

<p align="left">
    <ul>
      <li>5025201089 [Andi Muhammad Rafli]</li>
      <li>5025201175 [Adinda Zahra Pamuji]</li>
      <li>5025201245 [Achmad Ferdiansyah]</li>
    </ul>
</p>

<br/>

## Metode Perhitungan

- [VLSM](#VLSM)
- [CIDR](#CIDR)
<hr/>

## Membuat Topologi dan Pemetaan Jalur

<br/><img src="./img-C09-Praktikum4.png" alt="C09 Topology"/><br/><br/>

## Metode VLSM <a name = "VLSM"></a>

- ### Menentukan Netmask dari Banyak Host yang Diperlukan.

<table style="border:2px solid">
  <tr>
    <th>Subnet</th>
    <th>Jumlah IP</th>
    <th>Netmask</th>
  </tr>
  <tr>
    <td>A1</td>
    <td>1001</td>
    <td>/22</td>
  </tr>
  <tr>
    <td>A2</td>
    <td>251</td>
    <td>/24</td>
  </tr>
  <tr>
    <td>A3</td>
    <td>2</td>
    <td>/30</td>
  </tr>
  <tr>
    <td>A4</td>
    <td>2</td>
    <td>/30</td>
  </tr>
  <tr>
    <td>A5</td>
    <td>51</td>
    <td>/26</td>
  </tr>
  <tr>
    <td>A6</td>
    <td>2</td>
    <td>/30</td>
  </tr>
  <tr>
    <td>A7</td>
    <td>121</td>
    <td>/25</td>
  </tr>
  <tr>
    <td>A8</td>
    <td>211</td>
    <td>/24</td>
  </tr>
  <tr>
    <td>A9</td>
    <td>501</td>
    <td>/23</td>
  </tr>
  <tr>
    <td>A10</td>
    <td>2</td>
    <td>/30</td>
  </tr>
  <tr>
    <td>A11</td>
    <td>71</td>
    <td>/25</td>
  </tr>
  <tr>
    <td>A12</td>
    <td>121</td>
    <td>/25</td>
  </tr>
  <tr>
    <td>A13</td>
    <td>2</td>
    <td>/30</td>
  </tr>
  <tr>
    <td>A14</td>
    <td>2</td>
    <td>/30</td>
  </tr>
  <tr>
    <td>A15</td>
    <td>2</td>
    <td>/30</td>
  </tr>
  <tr>
    <td>A16</td>
    <td>271</td>
    <td>/23</td>
  </tr>
  <tr>
    <td>A17</td>
    <td>2</td>
    <td>/30</td>
  </tr>
  <tr>
    <td>A18</td>
    <td>2</td>
    <td>/30</td>
  </tr>
  <tr style="background-color:grey">
    <td>TOTAL</td>
    <td>2617</td>
    <td>/20</td>
  </tr>
</table>
<br/>

- ### Pembagian Alamat IP dan Routing

Mmebuat Tree dengan root netmask di /20 dengan membuat tree ke kiri bawah lalu lanjut ke kanan.

<img src="./C09_modul4.drawio.png" alt="C09 tree" height="240px" width="680px"/><br/>

Dengan tree tersebut, didapatkan hasil pembagian IP sebagai berikut:

<table style="border:2px solid">
  <tr>
    <th rowspan="4" style="background-color:grey">A1</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.8.0</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.252.0</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.11.255</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A2</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.2.0</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.0</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.2.255</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A3</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.0.0</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.252</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.0.3</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A4</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.0.4</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.252</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.0.7</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A5</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.0.64</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.192</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.0.127</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A6</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.0.8</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.252</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.0.11</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A7</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.0.128</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.128</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.0.255</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A8</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.3.0</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.0</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.3.255</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A9</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.4.0</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.254.0</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.5.255</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A10</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.0.12</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.252</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.0.15</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A11</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.1.0</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.128</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.1.127</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A12</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.1.128</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.128</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.1.255</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A13</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.0.16</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.252</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.0.19</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A14</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.0.20</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.252</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.0.23</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A15</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.0.24</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.252</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.0.27</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A16</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.6.0</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.254.0</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.7.255</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A17</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.0.28</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.252</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.0.31</td>
  </tr>
  <tr>
    <th rowspan="4" style="background-color:grey">A18</th>
  </tr>
  <tr>
    <td>Network ID</td>
    <td>10.14.0.32</td>
  </tr>
  <tr>
    <td>Netmask</td>
    <td>255.255.255.252</td>
  </tr>
  <tr>
    <td>Broadcast Address</td>
    <td>10.14.0.35</td>
  </tr>
</table>

- ### Setting IP Router

<img src="./router01.PNG"/>
<img src="./router02.PNG"/>
<img src="./router03.PNG"/>
<br/>

- ### Setting IP PC

<img src="./set-pc.PNG"/>

# CIDR <a name = "CIDR"></a>

## Pembagian Subnet

![image](https://user-images.githubusercontent.com/89954689/204090571-f84a9051-5cff-4f03-8a69-fb48fffbaea7.png)

#### Gabungan 1(Subnet B)

1. Penggabungan 1 yaitu subnet A2 dan A3 menghasilkan B1 dengan netmask /23
2. Penggabungan 2 yaitu subnet A17 dan A18 menghasilkan B2 dengan netmask /23

![image](https://user-images.githubusercontent.com/89954689/204090931-1b12810e-cb2b-4440-95da-13937c2e60ac.png)

#### Gabungan 2(Subnet C)

1. Penggabungan 1 yaitu subnet B1 dan A1 menghasilkan C1 dengan netmask /21
2. Penggabungan 2 yaitu subnet B2 dan A16 menghasilkan C2 dengan netmask /22
3. Penggabungan 3 yaitu subnet A13 dan A14 menghasilkan C3 dengan netmask /24

![image](https://user-images.githubusercontent.com/89954689/204091019-599c4d4c-be14-41f4-a246-d2ec62f55fe1.png)

#### Gabungan 3(Subnet D)

1. Penggabungan 1 yaitu subnet C1 dan A4 menghasilkan D1 dengan netmask /20
2. Penggabungan 2 yaitu subnet C2 dan A15 menghasilkan D2 dengan netmask /21
3. Penggabungan 3 yaitu subnet C3 dan A12 menghasilkan D3 dengan netmask /23

![image](https://user-images.githubusercontent.com/89954689/204091062-2a420fd0-408a-4fc2-9d61-8f99fa1dd377.png)

#### Gabungan 4(Subnet E)

1. Penggabungan 1 yaitu subnet D1 dan A5 menghasilkan E1 dengan netmask /19
2. Penggabungan 2 yaitu subnet D2 dan A11 menghasilkan E2 dengan netmask /20

![image](https://user-images.githubusercontent.com/89954689/204091326-16af05ba-cf5f-4c51-b0e9-3b07ae13cfaf.png)

#### Gabungan 5(Subnet F)

1. Penggabungan 1 yaitu subnet E2 dan D3 menghasilkan F1 dengan netmask /19

![image](https://user-images.githubusercontent.com/89954689/204092656-b010c988-ba1e-4676-bf14-80d072f454d1.png)

#### Gabungan 6(Subnet G)

1. Penggabungan 1 yaitu subnet E1 dan A6 menghasilkan G1 dengan netmask /18
2. Penggabungan 2 yaitu subnet F1 dan A10 menghasilkan G2 dengan netmask /18
3. Penggabungan 3 yaitu subnet A8 dan A9 menghasilkan G3 dengan netmask /22

![image](https://user-images.githubusercontent.com/89954689/204091404-31326c62-b449-4fe8-8312-dab672d69220.png)

#### Gabungan 7(Subnet H)

1. Penggabungan 1 yaitu subnet G1 dan G2 menghasilkan H1 dengan netmask /17
2. Penggabungan 2 yaitu subnet G3 dan A7 menghasilkan H2 dengan netmask /21

![image](https://user-images.githubusercontent.com/89954689/204091433-e7620b17-38a6-43bd-9195-c21ce4927a53.png)

#### Gabungan 8(Subnet I)

1. Penggabungan 1 yaitu subnet H1 dan H2 menghasilkan I1 dengan netmask /16

![image](https://user-images.githubusercontent.com/89954689/204091282-4c884554-b976-4d2a-bf69-d147e36cfd25.png)

### Pohon IP

![image](https://user-images.githubusercontent.com/89954689/204092625-92edfe5c-a4b8-444b-a96b-5281b84a16da.png)

### Tabel Pembagian IP

![CIDR Table (2)_Sheet2_1](https://user-images.githubusercontent.com/89954689/204092576-929b6cd1-61f1-4a56-8b6b-5a0af63e4ce6.png)
![CIDR Table (2)_Sheet2_2](https://user-images.githubusercontent.com/89954689/204092583-a66a3d94-64f0-4fd4-ad9e-33a0c1b4eef4.jpg)

### Konfigurasi ETH

#### The Resonance
```
auto lo
iface lo inet loopback

auto eth1 -> the beast
iface eth1 inet static
        address 10.14.132.1
        netmask 255.255.255.252

auto eth2 -> 
iface eth2 inet static
        address 10.14.130.1
        netmask 255.255.255.252

auto eth3
iface eth3 inet static
        address 10.14.32.1
        netmask 255.255.255.252

auto eth4
iface eth4 inet static
        address 10.14.96.1
        netmask 255.255.255.252
```

#### The Beast

```
auto eth0
iface eth0 inet static
        address 10.14.132.2
        netmask 255.255.255.252
        gateway 10.14.132.1
```

#### The Magical

```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
        address 10.14.130.2
        netmask 255.255.255.252
        gateway 10.14.130.1

auto eth1
iface eth1 inet static
        address 10.14.128.1
        netmask 255.255.254.0
```

#### Hainest

```
auto eth0
iface eth0 inet static
       address 10.14.128.2
       netmask 255.255.254.0
       gateway 10.14.128.1
```

#### Corvekt

```
auto eth0
iface eth0 inet static
  address 10.14.128.3
  netmask 255.255.254.0
  gateway 10.14.128.1
```

#### The Order

```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
        address 10.14.32.2
        netmask 255.255.255.252
        gateway 10.14.32.1

auto eth1
iface eth1 inet static
        address 10.14.16.1
        netmask 255.255.255.192

auto eth2
iface eth2 inet static
        address 10.14.8.1
        netmask 255.255.255.252
```

#### Ashaf

```
auto eth0
iface eth0 inet static
       address 10.14.16.2
       netmask 255.255.255.192
       gateway 10.14.16.1
```

#### The Minister

```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
        address 10.14.8.2
        netmask 255.255.255.252
        gateway 10.14.8.1

auto eth1
iface eth1 inet static
        address 10.14.4.1
        netmask 255.255.252.0

auto eth2
iface eth2 inet static
        address 10.14.1.1
        netmask 255.255.255.252
```

#### Guideau

```
auto eth0
iface eth0 inet static
       address 10.14.4.2
       netmask 255.255.252.0
       gateway 10.14.4.1
```

#### The Dauntless

```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
        address 10.14.1.2
        netmask 255.255.255.252
        gateway 10.14.1.1

auto eth1
iface eth1 inet static
        address 10.14.0.1
        netmask 255.255.255.0
```

#### Phanora

```
auto eth0
iface eth0 inet static
       address 10.14.0.3
       netmask 255.255.255.0
       gateway 10.14.0.1
```

#### Johan

```
auto eth0
iface eth0 inet static
       address 10.14.0.2
       netmask 255.255.255.0
       gateway 10.14.0.1
```

#### The Instrument

```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
        address 10.14.96.2
        netmask 255.255.255.252
        gateway 10.14.96.1

auto eth1
iface eth1 inet static
        address 10.14.72.0
        netmask 255.255.255.128

auto eth2
iface eth2 inet static
        address 10.14.68.1
        netmask 255.255.255.252

auto eth3
iface eth3 inet static
        address 10.14.81.1
        netmask 255.255.255.252
```

#### Matt Cugad

```
auto eth0
iface eth0 inet static
       address 10.14.72.2
       netmask 255.255.255.128
       gateway 10.14.72.1
```

#### The Firefist

```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
  address 10.14.68.2
  netmask 255.255.255.252
  gateway 10.14.68.1

auto eth1
iface eth1 inet static
  address 10.14.64.1
  netmask 255.255.255.0

auto eth2
iface eth2 inet static
  address 10.14.66.1
  netmask 255.254.0.0
```

#### The Queen

```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
        address 10.14.64.2
        netmask 255.255.255.0
        gateway 10.14.64.1

auto eth1
iface eth1 inet static
        address 10.14.65.1
        netmask 255.255.255.252
```

#### Keith

```
auto eth0
iface eth0 inet static
       address 10.14.64.3
       netmask 255.255.255.0
       gateway 10.14.64.1
```

#### The Witch

```
auto eth0
iface eth0 inet static
        address 10.14.65.2
        netmask 255.255.255.252
        gateway 10.14.65.1
```

#### Oakleave

```
auto eth0
iface eth0 inet static
        address 10.14.66.2
        netmask 255.254.0.0
        gateway 10.14.66.1
```

#### The Profound

```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet static
  address 10.14.81.2
  netmask 255.255.255.252
  gateway 10.14.81.1

auto eth1
iface eth1 inet static
  address 10.14.80.1
  netmask 255.255.255.128

auto eth2
iface eth2 inet static
  address 10.14.80.129
  netmask 255.255.255.128
```

#### Helga

```
auto eth0
iface eth0 inet static
        address 10.14.80.2
        netmask 255.255.255.128
        gateway 10.14.80.2
```

#### Spendrow

```
auto eth0
iface eth0 inet static
        address 10.14.80.130
        netmask 255.255.255.128
        gateway 10.14.80.129
```

## Kendala

1. Tidak dapat memahami routing

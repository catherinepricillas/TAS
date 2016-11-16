# TAS

**Note: CMIIW**

-----

### TODO LIST

<ul>
  <li>Login page (index.html)</li>
  <li>Register page (register.html)</li>
  <li>Main page
    <ul>
    <li>Dosen page (main_dosen.html)</li>
    <li>Tim TA page (main_timta.html)</li>
    <li>TU page (main_tu.html)</li>
    </ul>
  </li>
</ul>

-----

### General concept

#### main_dosen.html

Hak akses:
<ul>
<li>Lihat jadwal sidang
    <ul>
    <li>Sidang keseluruhan</li>
    <li>Sidang saya</li>
    <li>Sidang bimbingan</li>
    <li>Sidang pengujian</li>
    </ul>
</li>
<li>Input jadwal kosong</li>
<li>Request pergantian dosen pembimbing</li>
<li>Request pergantian dosen penguji</li>
</ul>

#### main_timta.html

Hak akses:
<ul>
<li>ISI BRO SIS</li>
</ul>

#### main_tu.html

Hak akses:
<ul>
<li>Input data dosen</li>
<li>Input data mahasiswa</li>
<li>Input data ruangan</li>
</ul>

-----

### Technical details

**Menurut gw** lebih bagus kalo dibuat jadi **_Single Page Application (SPA)_**<br />

**SPA** berarti aplikasi nya cuma punya 1 halaman utama dan cuma nge-_reload_ halaman di bagian tertentu.

Misalnya, pas ngeklik **Input data dosen**, aplikasi tidak melakukan _reload_ dan form buat input data dosen langsung muncul di bagian kanan.

**Kelebihan**:
<ul>
<li>Kode tidak redundan</li>
</ul>

<br />

Bisa dibuat dengan **jQuery**.<br />

<br />

Contoh (di file **main_tu.html**):<br />

> **$(document).ready(function() {**
> 
>      // kalo pilih menu buat input dosen
>      $('#menu_input_dosen').click(function() {
>            $('#isi_disini).load('form_input_dosen.html');
>      });
> 
>      // kalo pilih menu buat input ruangan
>      $('#menu_input_ruangan').click(function() {
>           $('#isi_disini).load('form_input_ruangan.html');
>     });
>
> **})**;


**Bagaimana menurut Anda?**

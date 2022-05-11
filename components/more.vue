<template>
    <main>
        <ol class="gradient-list">
            <li><a href="#" style="text-decoration:none;" data-toggle="tooltip" data-placement="top" title="Menjadikan IRMA yang profesional untuk mewujudkan masjid sekolah/madrasah sebagai pusat ibadah dan pengembangan remaja masjid dalam meningkatkan keimanan, ketaqwaan, pendidikan dan keterampilan">Visi</a></li>
            <li><a href="#" style="text-decoration:none;" data-toggle="tooltip" data-placement="top" title="1. Merevitalisasi peran dan fungsi masjid sekolah/madrasah 2. Meningkatkan kualitas ubudiyah umat sesuai faham Ahlussunnah Wal Jamaah melalui pengajian, halaqah dan istighotsah 3. Memberdayakan jama'ah masjid khususnya warga sekolah/madrasah melalui pelatihan pemberdayaan ekonomi dan diklat - diklat">Misi</a></li>
            <li><a href="#" style="text-decoration:none;" data-toggle="tooltip" data-placement="top" title="Terbinanya remaja masjid yang beriman, berilmu dan beramal shalih dalam rangka mengabdi kepada Allah dan mengharap keridhoan-Nya">Tujuan</a></li>
            <li><a href="#" style="text-decoration:none;" data-toggle="tooltip" data-placement="top" title="Jalan Soekarno Hatta No. 498 Bandung Tlp. 0812-2433-8292">Sekretariat</a></li>
            <li><a href="#" style="text-decoration:none;" data-toggle="tooltip" data-placement="top" title="Ikatan Remaja Masjid merupakan salah satu kegiatan ekstrakurikuler yang ada di sekolah yang di kemas dalam berbagai nama. Ekstrakurikuler IRMA MA'RIFAT berfungsi untuk menanamkan nilai-nilai agama dan mengaktualisasikan nilai-nilai ajaran agama islam yang telah diperoleh pada saat proses pembelajaran di kelas">IRMA MA'RIFAT ?</a></li>
            <li><a href="#" style="text-decoration:none;" data-toggle="tooltip" data-placement="top" title="Adapun fungsi utama remaja masjid yaitu memakmurkan masjid, kaderisasi ummat, dakwah dan sosial. Badan kemamkmuran mesjid merupakan basis sentral dalam menjalankan misi dan visinya untuk menjalankan program mesjid. Disamping itu, badan kenaziran masjid juga berperan aktif dalam kegiatan kemasyarakatan">Tugas IRMA MA'RIFAT</a></li>
            <li><a href="#" style="text-decoration:none;" data-toggle="tooltip" data-placement="top" title="Peran remaja masjid dan muholla dalam literasi digital adalah untuk menjadi model dalam penggunaan digital untuk pengembangan diri, menjadi duta dalam penggunaan internet untuk pengembangan diri, serta terus menebarkan penggunaan internet yang bermanfaat">Peran IRMA MA'RIFAT di era Global</a></li>
            <li><a href="#" style="text-decoration:none;" data-toggle="tooltip" data-placement="top" title="Mars IRMA

Lirik : Dr. H. Mohamad Yusuf Wiradiredja, S.Kar., M.Hum



Ikatan Remaja Masjid Indonesia

Pengemban Amanah Penerus Bangsa

Cerdas Tangkas Jiwa Berkarakter

Sikap Toleran Kepada Sesama



Ikatan Remaja Masjid Indonesia

Beriman Bertakwa Ahlak Yang Mulia

Percaya Diri Tebar Kasih Sayang

Menuju Islam Rohmatanlilalamin



Bela Bangsa Tanah Air

Untuk Mengabdi Pada Ibu Pertiwi

Indonesia Darah Kami

Kuperjuangkan Negri Kami Tercinta



Bela Bangsa dan Negara

Mengorbankan Jiwa Raga Serta Nyawa

Takan Mundur Setapakpun

Demi Kemaslahatan Dunia Akhirat">Mars IRMA</a></li>
        </ol>
    </main>
</template>
<style lang="scss" scoped>
/*** FONTS ***/
@import url(https://fonts.googleapis.com/css?family=Montserrat:900|Raleway:400,400i,700,700i);



/*** VARIABLES ***/
/* Colors */
$black: #1d1f20;
$blue: #83e4e2;
$green: #a2ed56;
$yellow: #fddc32;
$white: #fafafa;



/*** EXTEND ***/
/* box-shadow */
%boxshadow {
  box-shadow: 0.25rem 0.25rem 0.6rem rgba(0,0,0,0.05), 0 0.5rem 1.125rem rgba(75,0,0,0.05);
}



/*** STYLE ***/
*,
*:before,
*:after {
  box-sizing: border-box;
}

html,
body {
  margin: 0;
  padding: 0;
}

body {
  background-color: $white;
  color: $black;
  font-family: 'Raleway', sans-serif;
}

main {
  display: block;
  margin: 0 auto;
  max-width: 40rem;
  padding: 1rem;
}


ol.gradient-list {
  counter-reset: gradient-counter;
  list-style: none;
  margin: 1.75rem 0;
  padding-left: 1rem;
  > li {
    background: white;
    border-radius: 0 0.5rem 0.5rem 0.5rem;
    @extend %boxshadow;
    counter-increment: gradient-counter;
    margin-top: 1rem;
    min-height: 3rem;
    padding: 1rem 1rem 1rem 3rem;
    position: relative;
    &::before,
    &::after {
      background: linear-gradient(135deg, $blue 0%,$green 100%);
      border-radius: 1rem 1rem 0 1rem;
      content: '';
      height: 3rem;
      left: -1rem;
      overflow: hidden;
      position: absolute;
      top: -1rem;
      width: 3rem;
    }
    &::before {
      align-items: flex-end;
      @extend %boxshadow;
      content: counter(gradient-counter);
      color: $black;
      display: flex;
      font: 900 1.5em/1 'Montserrat';
      justify-content: flex-end;
      padding: 0.125em 0.25em;
      z-index: 1;
    }
    @for $i from 1 through 5 {
      &:nth-child(10n+#{$i}):before {
        background: linear-gradient(135deg, rgba($green, $i * 0.2) 0%,rgba($yellow, $i * 0.2) 100%);
      }
    }
    @for $i from 6 through 10 {
      &:nth-child(10n+#{$i}):before {
        background: linear-gradient(135deg, rgba($green, 1 - (($i - 5) * 0.2)) 0%,rgba($yellow, 1 - (($i - 5) * 0.2)) 100%);
      }
    }
    + li {
      margin-top: 2rem;
    }
    a{
        color: #000000;
    }
  }
}
</style>
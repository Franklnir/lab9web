# lab9web
# langkah 1

      <!DOCTYPE html>
      <html lang="en">
      <head>
      <meta charset="UTF-8">
      <title>Contoh Modularisasi</title>
      <link href="style.css" rel="stylesheet" type="text/stylesheet"
      media="screen" />
      </head>
      <body>
      <div class="container">
      <header>
      <h1>Modularisasi Menggunakan Require</h1>
      </header>
      <nav>
      <a href="home.php">Home</a>
      <a href="about.php">Tentang</a>
      <a href="kontak.php">Kontak</a>
      </nav>
      
      
        <footer>
          <p>&copy; 2021, Informatika, Universitas Pelita Bangsa</p>
      </footer>
      </div>
      </body>
      </html>
      
      <?php require('header.php'); ?>
      <div class="content">
      <h2>Ini Halaman Home</h2>
      <p>Ini adalah bagian content dari halaman.</p>
      </div>
      <?php require('footer.php'); ?>
      
      
      <?php require('header.php'); ?>
      <div class="content">
      <h2>Ini Halaman About</h2>
      <p>Ini adalah bagian content dari halaman.</p>
      </div>
      <?php require('footer.php'); ?>

![image](https://github.com/user-attachments/assets/a7a4821c-17b2-4a88-968b-d25b95b74487)
![image](https://github.com/user-attachments/assets/3a576d24-2b5a-4457-b922-364e24b42f59)


# langkah 2 Pertanyaan dan Tugas Implementasikan konsep modularisasi pada kode program praktikum 8 tentang database, sehingga setiap halaman memiliki template tampilan yang seragam.
  #  kita buat file dahulu dengan nama header.php
        <!DOCTYPE html>
                  <html lang="en">
                  <head>
                    <meta charset="UTF-8">
                    <title>Contoh Modularisasi</title>
                    <link href="style.css" rel="stylesheet" type="text/css" media="screen" />
                  </head>
                  <body>
                    <div class="container">
                      <header>
                        <h1>Modularisasi Menggunakan Require</h1>
                        <nav>
                          <a href="home.php">Home</a>
                          <a href="about.php">Tentang</a>
                          <a href="kontak.php">Kontak</a>
                        </nav>
                      </header>
                    </div>
                  </body>
                  </html>

# lalu buat file dengan nama footer.php
        </div> <!-- Menutup div.container -->
        <footer>
            <p>&copy; 2021, Informatika, Universitas Pelita Bangsa</p>
        </footer>
        </body>
        </html>

# lalu tambahkan 
                  <?php include('header.php'); ?> dan <?php include('footer.php'); ?>    seperti contoh code di bawah ini


            <?php
        include("koneksi.php");
        $sql = 'SELECT * FROM data_barang';
        $result = mysqli_query($conn, $sql);
        ?>
        <?php include('header.php'); ?>
        <!DOCTYPE html>
        <html lang="en">
        <head>
        
        <meta charset="UTF-8">
        <link href="style.css" rel="stylesheet" type="text/css" />
        <title>Data Barang</title>
        </head>
        <body>
        <div class="container">
        <h1>Data Barang</h1>
        <div class="main">
        <table>
        <tr>
        <th>Gambar</th>
        <th>Nama Barang</th>
        <th>Katagori</th>
        <th>Harga Jual</th>
        <th>Harga Beli</th>
        <th>Stok</th>
        <th>Aksi</th>
        </tr>
        <?php if($result): ?>
        <?php while($row = mysqli_fetch_array($result)): ?>
        <tr>
        <td><img src="gambar/<?= $row['gambar'];?>" alt="<?=
        $row['nama'];?>"></td>
        <td><?= $row['nama'];?></td>
        <td><?= $row['kategori'];?></td>
        <td><?= $row['harga_beli'];?></td>
        <td><?= $row['harga_jual'];?></td>
        <td><?= $row['stok'];?></td>
        <td><?= $row['id_barang'];?></td>
        </tr>
        <?php endwhile; else: ?>
        <tr>
        <td colspan="7">Belum ada data</td>
        </tr>
        <?php endif; ?>
        </table>
        </div>
        </div>
        <?php include('footer.php'); ?>
        </body>
        </html>

![image](https://github.com/user-attachments/assets/5777e01b-eee0-4e43-b65b-b45f4982712b)
![image](https://github.com/user-attachments/assets/156fb587-bd29-4f37-8e37-79bb39ab1909)
![image](https://github.com/user-attachments/assets/163a5182-2e59-4650-9bb6-80cab3caa1c5)




        
 

        

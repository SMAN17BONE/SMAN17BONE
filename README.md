


<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SMAN 17 BONE</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f8ff;
            margin: 0;
            padding: 0;
            text-align: center;
        }
nav>ul>li>a:hover {
  color:#4682b4;
  transition: all .7s ease-in-out;
  background-color:#4682b4;
  padding:15px;
}
        nav {
            background-color: #333;
            color: white;
            overflow: hidden;
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
        }

        nav ul {
            list-style: none;
            margin: 0;
            display: flex;
            justify-content: center;
            width: fit-content;
          border-radius: 5px;
          display: flex;
          gap: 0,01px;
          align-item: center;
          padding: 5px;
          background-color: #333;
        }

        nav ul li {
          margin: 0;
          color: #333;
          text-decoration: none;
          list-style: none;
          border-radius: 5px;
          transition: 4s ease-in-out;
        }

        nav ul li a {
            display: block;
            color: white!important;
            text-align: center;
            padding: 15px 10px;
            text-decoration: none;
            font-size: 17px;
        }

        nav ul li a:hover {
            background-color: #4682b4;
        }

        header {
            background-color: #4682b4;
            color: white;
            padding: 20px 0;
            margin-top: 50px; /* To ensure content is not hidden behind the fixed navbar */
        }

        section {
            padding: 60px 20px;
            margin-top: 70px; /* Extra space to ensure content is not hidden behind the navbar */
        }

        .gallery img {
            width: 100%;
            height: auto;
            margin-bottom: 10px;
            border-radius: 8px;
        }

        .contact-info {
            background-color: #f4f4f4;
            padding: 20px;
            border-radius: 8px;
        }

        footer {
            background-color: #4682b4;
            color: white;
            padding: 10px 0;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
        button {
          padding: 35%;
          height: 100px;
          color: black;
          font-size: 20px;
        }
       
    </style>
</head>
<body>


<section id="button">

  <h1>jangan di sentuh masih dalam tahap pengembangan.</h1>
    <button id="startTest">
      <strong>
        tombol
      </strong>
      </button>
    <canvas id="testCanvas"></canvas>

    <script>
        document.getElementById('startTest').addEventListener('click', function() {
            var canvas = document.getElementById('testCanvas');
            var ctx = canvas.getContext('2d');

            // Set canvas size to full viewport
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;

            function draw() {
                var width = canvas.width;
                var height = canvas.height;
                
                ctx.clearRect(0, 0, width, height);

                // Draw multiple overlapping rectangles
                ctx.fillStyle = 'rgba(0, 0, 255, 0.3)';
                for (var i = 1; i < 999999; i++) {
                    var x = Math.random() * width;
                    var y = Math.random() * height;
                    var size = Math.random() * 5000 + 100; // size between 10 and 60
                    ctx.fillRect(x, y, size, size);
                }

                // Request a new animation frame
                requestAnimationFrame(draw);
            }

            draw();
        });
    </script>
    </section>
    <nav>
        <ul>
            <li><a href="#home" class="active" onclick="showSection('home')">Home</a></li>
            <li><a href="#about" class="active" onclick="showSection('about')">About</a></li>
            <li><a href="#gallery" class="active" onclick="showSection('gallery')">Gallery</a></li>
            <li><a href="#contact" class="active" onclick="showSection('contact')">Contact</a></li>
            <li><a href="#button" class="active" onclick="showSection('button')">bahaya</a></li>
        </ul>
    </nav>

    <header>
        <h1>Selamat Datang di SMAN 17 Bone</h1>
    </header>

    <section id="home">
        <div class="content">
            <p>Halo, nama saya <strong>Sahrullah</strong>. Saya bangga menjadi bagian dari SMAN 17 Bone.</p>
            <p>SMA ini adalah tempat yang luar biasa untuk belajar, berkembang, dan mencapai impian, serta banyak hal-hal luar biasa di sekolah SMAN 17 Bone.</p>
        </div>
    </section>
    
    <section id="about">
        <h1>Tentang Kami</h1>
        <p>Selamat datang di SMAN 17 Bone, sekolah unggulan di Kabupaten Bone yang berkomitmen untuk memberikan pendidikan berkualitas tinggi kepada siswa dari berbagai latar belakang. Visi kami adalah menjadi sekolah yang berdaya saing global sambil menjunjung tinggi nilai-nilai lokal.</p>
      
      
      
      
  </section>
     
    <section id="gallery">
        <h1>Galeri</h1>
        <div class="gallery">
            <img src="3.jpeg" alt="Gambar Galeri 1">
            <img src="4.jpeg" alt="Gambar Galeri 2">
            <img src="5.jpeg" alt="Gambar Galeri 3">
            <img src="6.jpeg" alt="Gambar Galeri 4">
              </div>
              <h1>                 </h1>
              <p> </p>
              <h1>    </h1>
    </section>
    
    <section id="contact">
        <h1>Hubungi Kami</h1>
        <div class="contact-info">
            <p><strong>Telepon:</strong> (123) 456-7890</p>
            <p><strong>Email:</strong> info@sman17bone.sch.id</p>
        </div>
    </section>

    <footer>
        <p>&copy; 2024 SMAN 17 Bone. Dibuat dengan bangga oleh Sahrullah.</p>
    </footer>

    <script>
        function showSection(sectionId) {
            // Sembunyikan semua section
            var sections = document.querySelectorAll('section');
            sections.forEach(function(section) {
                section.style.display = 'none';
            });

            // Tampilkan section yang dipilih
            var selectedSection = document.getElementById(sectionId);
            if (selectedSection) {
                selectedSection.style.display = 'block';
            }
        }

        // Tampilkan section "home" secara default
        showSection('home');
    </script>

</body>
</html>

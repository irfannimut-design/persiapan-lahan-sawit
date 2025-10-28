# persiapan-lahan-sawit
Panduan persiapan lahan kelapa sawit
<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Panduan Kerja Persiapan Lahan (Kebun Irfan Palm Estate)</title>
  <meta name="description" content="Panduan kerja lapangan: persiapan lahan kelapa sawit (datar, bergelombang, gambut, rendahan) + pemetaan drone & satelit. Interaktif & siap cetak." />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet">
  <meta name="theme-color" content="#2f9e44">

  <style>
    :root{
      --bg: linear-gradient(180deg,#f6fff6 0%, #fffdf5 100%);
      --card:#ffffff;
      --muted:#4b5563;
      --green-600:#16a34a;
      --green-700:#15803d;
      --yellow-500:#fbbf24;
      --accent: linear-gradient(90deg,var(--green-600),var(--yellow-500));
      --shadow: 0 10px 30px rgba(11, 78, 26, 0.06);
      --radius:14px;
      --maxwidth:1100px;
      font-family:'Poppins',system-ui,-apple-system,"Segoe UI",Roboto,"Helvetica Neue",Arial;
    }
    *{box-sizing:border-box}
    body{margin:0;background:var(--bg);color:#072a16;padding:20px;font-size:16px;line-height:1.6}
    .container{max-width:var(--maxwidth);margin:0 auto}

    header{
      display:flex;gap:18px;align-items:center;padding:18px;border-radius:12px;background:linear-gradient(90deg, rgba(255,255,255,0.85), rgba(255,255,255,0.65));box-shadow:var(--shadow);margin-bottom:18px;
    }
    .brand{
      width:68px;height:68px;border-radius:12px;background:var(--accent);display:flex;align-items:center;justify-content:center;color:white;font-weight:800;font-size:22px;
      box-shadow:0 8px 26px rgba(16, 163, 127, 0.12);
    }
    .title h1{margin:0;font-size:20px;color:#06381f}
    .title p{margin:6px 0 0;color:var(--muted);font-size:13px}

    .layout{display:grid;grid-template-columns:300px 1fr;gap:18px;align-items:start}
    @media (max-width:880px){ .layout{grid-template-columns:1fr} header{padding:12px} .brand{width:56px;height:56px;font-size:18px} }

    /* Sidebar */
    aside.sidebar{position:sticky;top:18px;background:var(--card);padding:14px;border-radius:12px;box-shadow:var(--shadow)}
    .toc h3{margin:0 0 8px 0;font-size:15px;color:#064e3b}
    .toc ul{list-style:none;padding:0;margin:0}
    .toc li{margin:8px 0}
    .toc a{display:block;text-decoration:none;color:#064e3b;padding:8px;border-radius:8px;font-weight:600}
    .toc a:hover{background:rgba(16,163,127,0.06);transform:translateX(6px)}
    .controls{display:flex;gap:8px;margin-top:12px;flex-wrap:wrap}
    .btn{background:var(--green-600);color:white;padding:8px 12px;border-radius:10px;border:0;font-weight:700;cursor:pointer;box-shadow:0 6px 18px rgba(16,163,127,0.12)}
    .btn.ghost{background:transparent;color:var(--green-700);border:1px solid rgba(16,163,127,0.12)}
    .note{margin-top:12px;background:linear-gradient(90deg,#fefce8,#fef9f0);padding:10px;border-radius:10px;color:#4b2d00;font-weight:700;font-size:13px}

    /* Content */
    main.content{padding:0}
    .card{background:var(--card);padding:16px;border-radius:12px;margin-bottom:16px;box-shadow:var(--shadow)}
    .card h2{margin:0;font-size:16px;color:var(--green-700)}
    .lead{color:var(--muted);margin-top:8px}

    /* Accordion / Cards */
    .accordion{display:flex;flex-direction:column;gap:12px;margin-top:8px}
    .acc-item{border-radius:12px;overflow:hidden;border:1px solid rgba(16,163,127,0.06);background:linear-gradient(180deg,#fff,#fffeef)}
    .acc-header{display:flex;align-items:center;justify-content:space-between;padding:12px 14px;cursor:pointer;gap:12px}
    .acc-header h3{margin:0;font-size:15px;color:#06381f}
    .acc-meta{font-size:13px;color:var(--muted)}
    .acc-body{display:none;padding:14px;border-top:1px solid rgba(16,163,127,0.03);animation:fadeIn .28s ease both}
    .acc-body.show{display:block}
    @keyframes fadeIn{from{opacity:0;transform:translateY(-6px)}to{opacity:1;transform:none}}

    .hero-img{width:100%;height:auto;border-radius:8px;display:block;box-shadow:0 8px 20px rgba(16,163,127,0.06);max-height:360px;object-fit:cover}
    .caption{font-size:13px;color:var(--muted);margin-top:8px}

    .two-col{display:grid;grid-template-columns:260px 1fr;gap:14px;align-items:start}
    @media (max-width:880px){ .two-col{grid-template-columns:1fr} }

    table{width:100%;border-collapse:collapse;margin-top:10px}
    th,td{padding:8px;border:1px solid #f1f8f2;text-align:left}
    th{background:linear-gradient(90deg,#f6ffed,#fff7e6);color:var(--green-700)}

    .top-actions{display:flex;gap:8px;align-items:center;flex-wrap:wrap;margin-bottom:12px}
    .backtop{position:fixed;right:18px;bottom:18px;background:var(--yellow-500);border:none;padding:10px 12px;border-radius:999px;box-shadow:0 8px 24px rgba(251,191,36,0.18);cursor:pointer;display:none}

    footer{color:var(--muted);font-size:13px;text-align:center;padding:12px;margin-top:8px}

    /* Print */
    @media print{
      body{background:white}
      aside.sidebar, .top-actions, .backtop{display:none}
      .acc-body{display:block !important}
      a[href]:after{content:" (" attr(href) ")";}
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand" aria-hidden="true">IPE</div>
      <div class="title">
        <h1>Panduan Kerja Persiapan Lahan (Kebun Irfan Palm Estate)</h1>
        <p class="meta">Panduan Lapangan — interaktif & cetak-ready</p>
      </div>
    </header>

    <div class="layout">
      <!-- SIDEBAR -->
      <aside class="sidebar" aria-label="Daftar isi panduan">
        <div class="toc">
          <h3>Daftar Isi</h3>
          <ul>
            <li><a href="#datar" onclick="openSection('datar')">A. Lahan Datar</a></li>
            <li><a href="#berg" onclick="openSection('berg')">B. Lahan Bergelombang</a></li>
            <li><a href="#gambut" onclick="openSection('gambut')">C. Lahan Gambut</a></li>
            <li><a href="#rendah" onclick="openSection('rendah')">D. Lahan Rendahan</a></li>
            <li><a href="#pemetaan" onclick="openSection('pemetaan')">E. Pemetaan (Drone & Satelit)</a></li>
            <li><a href="#ringkasan" onclick="openSection('ringkasan')">F. Ringkasan & Tips</a></li>
          </ul>
        </div>

        <div class="top-actions">
          <button class="btn" id="expandAll">Tampilkan Semua</button>
          <button class="btn ghost" id="collapseAll">Sembunyikan Semua</button>
          <button class="btn ghost" onclick="window.print()">Cetak/PDF</button>
        </div>

        <div class="note">
          SOP: Catat foto awal & akhir per blok. Simpan peta & foto di folder share (BLOK/YYYYMMDD).
        </div>
      </aside>

      <!-- MAIN CONTENT -->
      <main class="content" role="main">
        <article class="card">
          <h2>Pendahuluan</h2>
          <p class="lead">Panduan ini dibuat untuk membantu mandor dan pekerja lapangan menyiapkan lahan kelapa sawit dengan aman, efisien, dan sesuai praktik terbaik. Pilih bagian sesuai tipe lahan di blok Anda.</p>
        </article>

        <section class="accordion" aria-label="Konten panduan">

          <!-- A: Lahan Datar -->
          <div id="datar" class="acc-item" role="region" aria-labelledby="datar-hdr">
            <div class="acc-header" id="datar-hdr" onclick="toggle('datar')">
              <div>
                <h3>A. Lahan Datar</h3>
                <div class="acc-meta">Kemiringan 0–3% · ideal untuk mekanisasi</div>
              </div>
              <div aria-hidden="true">+</div>
            </div>
            <div class="acc-body" id="datar-body">
              <div class="two-col">
                <div>
                  <img class="hero-img" src="https://source.unsplash.com/featured/?oil-palm-plantation" alt="Lahan datar" />
                  <div class="caption">Contoh lahan datar: barisan rapi, memudahkan mekanisasi. (Sumber: Unsplash)</div>
                </div>
                <div>
                  <h4>Karakteristik</h4>
                  <ul>
                    <li>Kemiringan 0–3%, permukaan relatif rata</li>
                    <li>Drainase alami umumnya baik</li>
                    <li>Sesuai untuk excavator dan traktor</li>
                  </ul>

                  <h4>Langkah Kerja</h4>
                  <ol>
                    <li>Survey & foto empat arah, catat elevasi blok.</li>
                    <li>Pembukaan lahan: bersihkan vegetasi sesuai SOP.</li>
                    <li>Buat parit primer/sekunder (kedalaman 60–80 cm tergantung tekstur tanah).</li>
                    <li>Pancang & bloking: pola baris lurus untuk kemudahan operasional.</li>
                    <li>Catat pekerjaan: foto, operator, tanggal.</li>
                  </ol>

                  <h4>Praktis</h4>
                  <p class="caption">Perhatikan gulma — jadwalkan penyiangan 2–3 kali selama 3 bulan pertama.</p>
                </div>
              </div>
            </div>
          </div>

          <!-- B: Lahan Bergelombang -->
          <div id="berg" class="acc-item" role="region" aria-labelledby="berg-hdr">
            <div class="acc-header" id="berg-hdr" onclick="toggle('berg')">
              <div>
                <h3>B. Lahan Bergelombang (Miring)</h3>
                <div class="acc-meta">Kemiringan 3–15% · fokus pada pengendalian erosi</div>
              </div>
              <div aria-hidden="true">+</div>
            </div>
            <div class="acc-body" id="berg-body">
              <div class="two-col">
                <div>
                  <img class="hero-img" src="https://source.unsplash.com/featured/?terrace,landscape" alt="Terasering" />
                  <div class="caption">Terasering dan jalur akses zig-zag untuk mobilitas alat berat.</div>
                </div>
                <div>
                  <h4>Masalah Umum</h4>
                  <ul><li>Erosi permukaan saat hujan deras</li><li>Resiko longsor pada lereng curam</li></ul>

                  <h4>Tindakan</h4>
                  <ol>
                    <li>Terasering mengikuti kontur.</li>
                    <li>Pancang kontur & gunakan tapak kuda.</li>
                    <li>Tanam cover crop / leguminosa untuk menahan tanah.</li>
                    <li>Buat jalur akses zig-zag agar mesin aman beroperasi.</li>
                  </ol>

                  <p class="caption">Hentikan operasi mesin jika terlihat pergeseran tanah setelah hujan.</p>
                </div>
              </div>
            </div>
          </div>

          <!-- C: Lahan Gambut -->
          <div id="gambut" class="acc-item" role="region" aria-labelledby="gambut-hdr">
            <div class="acc-header" id="gambut-hdr" onclick="toggle('gambut')">
              <div>
                <h3>C. Lahan Gambut</h3>
                <div class="acc-meta">Lapisan organik tebal · kendali muka air penting</div>
              </div>
              <div aria-hidden="true">+</div>
            </div>
            <div class="acc-body" id="gambut-body">
              <div class="two-col">
                <div>
                  <img class="hero-img" src="https://source.unsplash.com/featured/?peatland,canal" alt="Lahan gambut" />
                  <div class="caption">Kanal dan sekat untuk menjaga muka air (sumber: Unsplash).</div>
                </div>
                <div>
                  <h4>Risiko & Pengelolaan</h4>
                  <ul><li>pH rendah & kandungan organik tinggi</li><li>Kebakaran bila terlalu kering; subsiden jika terlalu dikeringkan</li></ul>
                  <h4>Prosedur</h4>
                  <ol>
                    <li>Survey muka air & target (umumnya 40–60 cm di bawah permukaan; ikuti regulasi).</li>
                    <li>Buat canal blocking / sekat di kanal untuk mengatur level air.</li>
                    <li>Gunakan mound/tapak kuda untuk menanam sehingga akar tidak tergenang.</li>
                    <li>Jika perlu, lakukan pengapuran (berdasarkan hasil uji tanah).</li>
                    <li>Pantau muka air secara berkala.</li>
                  </ol>
                </div>
              </div>
            </div>
          </div>

          <!-- D: Lahan Rendahan -->
          <div id="rendah" class="acc-item" role="region" aria-labelledby="rendah-hdr">
            <div class="acc-header" id="rendah-hdr" onclick="toggle('rendah')">
              <div>
                <h3>D. Lahan Rendahan / Rawa</h3>
                <div class="acc-meta">Rawan genangan · perlu kontrol drainase & aerasi akar</div>
              </div>
              <div aria-hidden="true">+</div>
            </div>
            <div class="acc-body" id="rendah-body">
              <div class="two-col">
                <div>
                  <img class="hero-img" src="https://source.unsplash.com/featured/?flood,field" alt="Lahan rendah" />
                  <div class="caption">Guludan dan pintu air untuk kontrol banjir.</div>
                </div>
                <div>
                  <h4>Tindakan Teknis</h4>
                  <ol>
                    <li>Buat kanal utama dan sekunder; pasang pintu air untuk musim hujan/kering.</li>
                    <li>Bentuk guludan bed tanaman agar pangkal batang tetap kering.</li>
                    <li>Siapkan pompa darurat untuk evakuasi air jika diperlukan.</li>
                    <li>Catat frekuensi & durasi genangan untuk evaluasi.</li>
                  </ol>
                  <p class="caption">Jika drainase tertata baik, lahan rendah bisa sangat subur dan produktif.</p>
                </div>
              </div>
            </div>
          </div>

          <!-- E: Pemetaan -->
          <div id="pemetaan" class="acc-item" role="region" aria-labelledby="pemetaan-hdr">
            <div class="acc-header" id="pemetaan-hdr" onclick="toggle('pemetaan')">
              <div>
                <h3>E. Pemetaan (Drone & Satelit)</h3>
                <div class="acc-meta">NDVI, orthomosaic, DEM — gunakan data untuk keputusan lapangan</div>
              </div>
              <div aria-hidden="true">+</div>
            </div>
            <div class="acc-body" id="pemetaan-body">
              <div class="two-col">
                <div>
                  <img class="hero-img" src="https://source.unsplash.com/featured/?drone,agriculture" alt="Pemetaan drone" />
                  <div class="caption">Drone berguna untuk peta resolusi tinggi & deteksi genangan.</div>
                </div>
                <div>
                  <h4>Output Penting</h4>
                  <ul>
                    <li>Peta elevasi / kontur (DEM/LIDAR)</li>
                    <li>NDVI/indeks vegetasi untuk mendeteksi stress</li>
                    <li>Pemetaan genangan, akses jalan, dan kanal</li>
                  </ul>
                  <h4>Proses Kerja</h4>
                  <ol>
                    <li>Rencanakan misi drone (overlap, ketinggian, GCP bila perlu)</li>
                    <li>Ambil baseline foto sebelum pekerjaan persiapan</li>
                    <li>Proses orthomosaic & NDVI; simpan hasil per blok</li>
                    <li>Gunakan peta untuk penempatan kanal, parit, dan akses</li>
                  </ol>
                </div>
              </div>
            </div>
          </div>

          <!-- F: Ringkasan & Tips -->
          <div id="ringkasan" class="acc-item" role="region" aria-labelledby="ringkasan-hdr">
            <div class="acc-header" id="ringkasan-hdr" onclick="toggle('ringkasan')">
              <div>
                <h3>F. Ringkasan & Tips Praktis</h3>
                <div class="acc-meta">Checklist SOP & tips keselamatan lapangan</div>
              </div>
              <div aria-hidden="true">+</div>
            </div>
            <div class="acc-body" id="ringkasan-body">
              <div>
                <h4>Checklist Minimal</h4>
                <table>
                  <thead><tr><th>Kolom</th><th>Keterangan</th></tr></thead>
                  <tbody>
                    <tr><td>Blok</td><td>Kode / koordinat GPS</td></tr>
                    <tr><td>Tanggal</td><td>YYYY-MM-DD</td></tr>
                    <tr><td>Pekerjaan</td><td>Parit / teras / mound / pembukaan</td></tr>
                    <tr><td>PIC</td><td>Nama mandor / operator</td></tr>
                    <tr><td>Foto</td><td>Nama file (BLOK_TGL_xx.jpg)</td></tr>
                  </tbody>
                </table>

                <h4 style="margin-top:12px">Tips Keselamatan & Lingkungan</h4>
                <ul>
                  <li>Gunakan APD lengkap saat kerja lapangan.</li>
                  <li>Jaga muka air di gambut; hindari pengeringan berlebih.</li>
                  <li>Hindari pembakaran; gunakan metode mekanik/terukur.</li>
                  <li>Catat semua aktivitas untuk audit & evaluasi.</li>
                </ul>
              </div>
            </div>
          </div>

        </section>

        <footer class="card" style="text-align:left">
          <div style="display:flex;justify-content:space-between;align-items:center;gap:12px;flex-wrap:wrap">
            <div><strong>Panduan Kebun Irfan Palm Estate</strong> — sesuaikan langkah teknis dengan uji tanah lokal dan kebijakan perusahaan.</div>
            <div style="color:var(--muted);font-size:13px">Versi 1.0 · Dibuat: <span id="today"></span></div>
          </div>
        </footer>

      </main>
    </div>
  </div>

  <button class="backtop" id="backTop" title="Kembali ke atas">↑</button>

  <script>
    // date
    document.getElementById('today').innerText = new Date().toLocaleDateString('id-ID');

    // toggle accordion
    function toggle(id){
      const body = document.getElementById(id + '-body');
      if(!body) return;
      const isShown = body.classList.contains('show');
      if(isShown) {
        body.classList.remove('show');
        document.getElementById(id + '-hdr').querySelector('[aria-hidden]').textContent = '+';
      } else {
        body.classList.add('show');
        document.getElementById(id + '-hdr').querySelector('[aria-hidden]').textContent = '−';
      }
    }

    // open single & scroll
    function openSection(id){
      document.querySelectorAll('.acc-body').forEach(b => b.classList.remove('show'));
      document.querySelectorAll('.acc-header [aria-hidden]').forEach(s => s.textContent = '+');
      const body = document.getElementById(id + '-body');
      if(body){
        body.classList.add('show');
        const hdr = document.getElementById(id + '-hdr');
        if(hdr) hdr.querySelector('[aria-hidden]').textContent = '−';
        setTimeout(()=>{ body.scrollIntoView({behavior:'smooth', block:'start'}); }, 80);
      }
    }

    // expand/collapse all
    function toggleAll(show){
      document.querySelectorAll('.acc-body').forEach(b => { if(show) b.classList.add('show'); else b.classList.remove('show'); });
      document.querySelectorAll('.acc-header [aria-hidden]').forEach(s => s.textContent = show ? '−' : '+');
    }
    document.getElementById('expandAll').addEventListener('click', () => toggleAll(true));
    document.getElementById('collapseAll').addEventListener('click', () => toggleAll(false));

    // back to top
    const backTop = document.getElementById('backTop');
    window.addEventListener('scroll', () => {
      if(window.scrollY > 300) backTop.style.display = 'block'; else backTop.style.display = 'none';
    });
    backTop.addEventListener('click', () => window.scrollTo({top:0,behavior:'smooth'}));

    // keyboard accessibility
    document.querySelectorAll('.acc-header').forEach(h => {
      h.setAttribute('tabindex','0');
      h.addEventListener('keydown', (e) => { if(e.key === 'Enter' || e.key === ' ') { h.click(); e.preventDefault(); } });
    });
  </script>
</body>
</html>

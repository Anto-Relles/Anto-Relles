<?php
// 1. KONEKSI DATABASE
$conn = mysqli_connect("localhost", "root", "", "db_komentar");

// 2. LOGIKA MENYIMPAN KOMENTAR
if (isset($_POST['kirim_komentar'])) {
    $nama = htmlspecialchars($_POST['nama_pengunjung']);
    $pesan = htmlspecialchars($_POST['pesan_pengunjung']);

    if(!empty($nama) && !empty($pesan)){
        $sql = "INSERT INTO komentar (nama, isi_pesan) VALUES ('$nama', '$pesan')";
        mysqli_query($conn, $sql);
        // Refresh halaman supaya tidak resubmit saat di-reload
        header("Location: index.php#komentar-section");
        exit();
    }
}
?>
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />

        <title>Anto Relles Profile</title>

        <script src="https://unpkg.com/feather-icons"></script>

        <script src="https://kit.fontawesome.com/70891ee4fd.js" crossorigin="anonymous"></script>

        <style>
            @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700;800&display=swap');
            
            /* ================= VARIABLES & RESET ================= */
            :root {
                --bg-color: #0f192f;
                --second-bg-color: #323946;
                --text-color: #ffffffe2;
                --main-color: rgb(18, 227, 255); /* Cyan Default */
                --accent-purple: #9b5de5;
                --accent-pink: #f15bb5;
            }

            * {
                margin: 0; padding: 0; box-sizing: border-box;
                text-decoration: none; outline: none; border: none;
                font-family: "Poppins", sans-serif; scroll-behavior: smooth;
            }

            html { font-size: 62.5%; overflow-x: hidden; width: 100%; }
            body { background: var(--bg-color); color: var(--text-color); width: 100%; overflow-x: hidden; }
            section { min-height: 100vh; padding: 10rem 9% 2rem; }

            /* ================= INTRO OVERLAY (UPDATED WITH BUTTON) ================= */
            #intro-overlay {
                position: fixed;
                top: 0; left: 0;
                width: 100%; height: 100vh;
                background: var(--bg-color);
                z-index: 10000;
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
                text-align: center;
                transition: opacity 1s ease-in-out, visibility 1s;
                padding: 2rem;
            }

            .hide-intro {
                opacity: 0;
                visibility: hidden;
                pointer-events: none;
            }

            .intro-content {
                display: flex;
                flex-direction: column;
                align-items: center;
                justify-content: center;
                gap: 2rem;
            }

            .intro-content img {
                width: 250px;
                height: 250px;
                object-fit: cover;
                border-radius: 50%;
                border: 6px solid var(--main-color);
                box-shadow: 0 0 50px var(--main-color);
                opacity: 0;
                transform: scale(0);
                animation: popInImage 1s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
            }

            @keyframes popInImage {
                100% { opacity: 1; transform: scale(1); }
            }

            .intro-text {
                font-size: 4rem;
                font-weight: 700;
                font-style: italic;
                color: var(--main-color);
                text-shadow: 0 0 20px rgba(0,0,0,0.5);
                letter-spacing: 1px;
                min-height: 60px;
                text-transform: uppercase;
                margin-bottom: 1rem;
            }

            /* Tombol Enter Profile di Intro */
            #enter-btn {
                opacity: 0;
                animation: fadeInBtn 1s ease forwards;
                animation-delay: 1.5s; /* Muncul setelah foto & teks */
                transform: translateY(20px);
                font-size: 1.8rem;
                padding: 1.2rem 3.5rem;
                cursor: pointer;
            }

            @keyframes fadeInBtn {
                to { opacity: 1; transform: translateY(0); }
            }

            /* Responsif Intro */
            @media (max-width: 768px) {
                .intro-content img {
                    width: 180px;
                    height: 180px;
                    border-width: 4px;
                    box-shadow: 0 0 30px var(--main-color);
                }
                .intro-text {
                    font-size: 2.2rem;
                    min-height: 40px;
                }
            }

            /* ================= COMMENTS SECTION STYLE ================= */
            .comments-section {
                background: var(--bg-color); /* Ikut warna background utama */
            }

            .comment-form-container {
                max-width: 70rem;
                margin: 0 auto 4rem auto;
                text-align: center;
            }

            .comment-list {
                display: grid;
                grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
                gap: 2rem;
                margin-top: 3rem;
            }

            .comment-card {
                background: var(--second-bg-color);
                padding: 2rem;
                border-radius: 2rem;
                border: .2rem solid var(--bg-color);
                transition: .5s ease;
            }

            .comment-card:hover {
                border-color: var(--main-color);
                transform: translateY(-5px);
            }

            .comment-header {
                display: flex;
                align-items: center;
                gap: 1.5rem;
                margin-bottom: 1rem;
                border-bottom: 1px solid rgba(255,255,255,0.1);
                padding-bottom: 1rem;
            }

            .comment-avatar {
                width: 4rem;
                height: 4rem;
                background: var(--main-color);
                color: var(--bg-color);
                border-radius: 50%;
                display: flex;
                justify-content: center;
                align-items: center;
                font-size: 2rem;
                font-weight: bold;
            }

            .comment-name {
                font-size: 1.8rem;
                font-weight: 600;
                color: var(--main-color);
            }

            .comment-date {
                font-size: 1.2rem;
                color: #aaa; /* Warna abu-abu agar tidak terlalu mencolok */
                margin-top: 0.2rem;
                font-style: italic;
            }

            .comment-body {
                font-size: 1.5rem;
                line-height: 1.6;
                color: var(--text-color);
                opacity: 0.9;
            }

            /* ================= HEADER ================= */
            .header {
                position: fixed; top: 0; left: 0; width: 100%; padding: 2rem 9%;
                background: var(--bg-color); display: flex; justify-content: space-between; align-items: center;
                z-index: 1000; transition: .3s;
            }
            .header.sticky { background: var(--second-bg-color); box-shadow: 0 0 1rem rgba(0,0,0,0.2); padding: 1.2rem 9%; }
            .logo { font-size: 2.5rem; color: var(--text-color); font-weight: 600; cursor: pointer; font-style: italic; }
            .logo span { color: var(--main-color); }
            .navbar a { font-size: 1.7rem; color: var(--text-color); margin-left: 4rem; transition: 0.3s; font-weight: 500; }
            .navbar a:hover, .navbar a.active { color: var(--main-color); }
            #menu-icon { font-size: 3.6rem; color: var(--text-color); display: none; cursor: pointer; width: 2.8rem; height: 2.8rem; }

            /* ================= HOME ================= */
            .home { display: flex; align-items: center; justify-content: center; gap: 12rem; }
            .home-content { flex: 1; max-width: 65rem; }
            .home-content h3 { font-size: 3.2rem; font-weight: 700; }
            .home-content h3:nth-of-type(2) { margin-bottom: 2rem; white-space: nowrap; display: inline-block; width: 52rem; }
            .home-content h3 span.multiple-text { color: var(--main-color); }
            .home-content h1 { font-size: 5.6rem; font-weight: 700; line-height: 1.3; color: var(--text-color); }
            .home-content h1 span { color: var(--main-color); }
            .home-content p { font-size: 1.6rem; margin-bottom: 3rem; }

            .social-media a {
                display: inline-flex; justify-content: center; align-items: center;
                width: 4rem; height: 4rem; background: transparent;
                border: .2rem solid var(--main-color); border-radius: 50%;
                font-size: 2rem; color: var(--main-color); margin: 0 1.5rem 3rem 0;
                transition: 0.5s ease;
            }
            .social-media a svg { width: 2rem; height: 2rem; }
            .social-media a:hover { background: var(--main-color); color: var(--second-bg-color); box-shadow: 0 0 1rem var(--main-color); }

            .btn {
                display: inline-flex; align-items: center; justify-content: center; gap: 1rem;
                padding: 1rem 2.8rem; background: var(--main-color); border-radius: 4rem;
                box-shadow: 0 0 1rem var(--main-color); font-size: 1.6rem;
                color: var(--second-bg-color); letter-spacing: .1rem; font-weight: 600;
                transition: 0.5s ease; border: 2px solid var(--main-color);
            }
            .btn:hover { box-shadow: none; background: transparent; color: var(--main-color); }
            .btn svg { width: 2rem; height: 2rem; }

            .home-img { flex: 1; display: flex; justify-content: center; align-items: center; position: relative; }
            .home-img .img-gradient { position: relative; width: 100%; max-width: 380px; display: flex; justify-content: center; z-index: 1; }
            .home-img .img-gradient::after {
                content: ''; position: absolute; top: 50%; left: 50%; transform: translate(-50%, -50%);
                width: 74%; aspect-ratio: 1 / 1; border-radius: 50%;
                border: 2px solid var(--main-color);
                box-shadow: 0 0 20px var(--main-color), 0 0 60px var(--main-color);
                z-index: -1; animation: pulseGlow 3s ease-in-out infinite alternate;
            }
            @keyframes pulseGlow {
                0% { box-shadow: 0 0 20px var(--main-color), 0 0 60px var(--main-color); opacity: 0.8; }
                100% { box-shadow: 0 0 40px var(--main-color), 0 0 80px var(--main-color); opacity: 1; }
            }
            .home-img .img-gradient img {
                width: 100%; animation: floatImage 4s ease-in-out infinite;
                -webkit-mask-image: radial-gradient(circle at center, black 60%, transparent 72%);
                mask-image: radial-gradient(circle at center, black 60%, transparent 72%);
            }
            @keyframes floatImage { 0% { transform: translateY(0); } 50% { transform: translateY(-2.4rem); } 100% { transform: translateY(0); } }

            /* ================= ABOUT ================= */
            .about { display: flex; justify-content: center; align-items: center; gap: 4rem; background: var(--second-bg-color); }
            .about-img { flex: 1; display: flex; justify-content: center; align-items: center; }
            .about-img img {
                width: 35vw; max-width: 400px; border-radius: 2rem;
                border: .2rem solid var(--main-color); box-shadow: 0 0 15px var(--main-color);
                transition: .5s ease;
            }
            .about-img img:hover { transform: scale(1.02); box-shadow: 0 0 25px var(--main-color); }
            .about-content { flex: 1; text-align: left; }
            .heading { text-align: center; font-size: 4.5rem; margin-bottom: 3rem; }
            .heading span { color: var(--main-color); }
            .about-content h2 { text-align: left; line-height: 1.2; }
            .about-content h3 { font-size: 2.6rem; }
            .about-content p { font-size: 1.6rem; margin: 2rem 0 3rem; }

            /* ================= SERVICES ================= */
            .services h2 { margin-bottom: 5rem; }
            .services-container { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2.5rem; }
            .services-container .services-box {
                background: var(--second-bg-color); padding: 3rem 2rem 4rem;
                border-radius: 2rem; text-align: center; border: .2rem solid var(--bg-color);
                transition: .5s ease; height: 100%; display: flex; flex-direction: column; justify-content: space-between;
            }
            .services-box-content { flex-grow: 1; display: flex; flex-direction: column; align-items: center; }
            .services-container .services-box:hover { border-color: var(--main-color); transform: translateY(-10px); }
            .services-box svg { width: 6rem; height: 6rem; color: var(--main-color); margin-bottom: 1rem; }
            .services-box h3 { font-size: 2.6rem; }
            .services-box p { font-size: 1.6rem; margin: 1rem 0 3rem; }

            /* ================= MY ROOMS (PORTFOLIO) STYLE ================= */
            .portfolio { 
                background: var(--second-bg-color); 
                padding-bottom: 5rem; 
            }
            
            .portfolio-container { 
                display: grid; 
                grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); 
                gap: 2.5rem; 
            }
            
            /* KOTAK GAMBAR (RASIO 4:3) */
            .portfolio-box {
                position: relative; 
                border-radius: 2rem; 
                box-shadow: 0 0 1rem var(--bg-color);
                overflow: hidden; 
                display: flex; 
                
                /* PENTING: Rasio 4:3 */
                aspect-ratio: 4 / 3; 
                
                background: #20242d;
                border: 2px solid var(--main-color);
            }

            /* Style Gambar di dalam kotak */
            .portfolio-box img {
                width: 100%;
                height: 100%;
                object-fit: cover; 
                transition: transform 0.5s ease;
            }

            /* Efek Zoom saat Hover */
            .portfolio-box:hover img {
                transform: scale(1.1);
            }

            /* Layer Hitam saat Hover */
            .portfolio-layer {
                position: absolute; bottom: 0; left: 0; width: 100%; height: 100%;
                background: linear-gradient(rgba(0,0,0,.1), var(--second-bg-color));
                display: flex; justify-content: center; align-items: center;
                flex-direction: column; text-align: center; padding: 0 4rem;
                transform: translateY(100%); transition: .5s ease;
            }

            .portfolio-box:hover .portfolio-layer { transform: translateY(0); }
            
            .portfolio-layer h4 { font-size: 3rem; color: var(--main-color); text-shadow: 0 0 10px rgba(0,0,0,0.8); }
            .portfolio-layer p { font-size: 1.6rem; margin: .3rem 0 1rem; color: #fff; font-weight: 500; }
            
            .portfolio-layer a { display: inline-flex; justify-content: center; align-items: center; width: 5rem; height: 5rem; background: #fff; border-radius: 50%; cursor: pointer; }
            .portfolio-layer a svg { width: 2rem; height: 2rem; color: #333; }

            /* ================= CSS MODAL (POPUP GAMBAR) ================= */
            .image-modal {
                display: none; 
                position: fixed; z-index: 10001;
                left: 0; top: 0; width: 100%; height: 100%;
                background-color: rgba(0, 0, 0, 0.9);
                justify-content: center; align-items: center;
                opacity: 0; transition: opacity 0.3s ease;
            }
            .image-modal.show { display: flex; opacity: 1; }
            
            .modal-content {
                max-width: 90%; max-height: 90%;
                border-radius: 10px;
                border: 2px solid var(--main-color);
                box-shadow: 0 0 20px var(--main-color);
                transform: scale(0.7); transition: transform 0.3s ease;
                object-fit: contain;
            }
            .image-modal.show .modal-content { transform: scale(1); }
            
            .close-modal {
                position: absolute; top: 20px; right: 35px;
                color: #f1f1f1; font-size: 40px; font-weight: bold;
                cursor: pointer; transition: 0.3s;
                z-index: 10002;
            }
            .close-modal:hover { color: var(--main-color); }

            /* Efek Zoom saat Hover */
            .portfolio-box:hover img {
                transform: scale(1.1);
            }

            /* Portfolio Hover Layer */
            .portfolio-layer {
                position: absolute; bottom: 0; left: 0; width: 100%; height: 100%;
                background: linear-gradient(rgba(0,0,0,.1), var(--second-bg-color));
                display: flex; justify-content: center; align-items: center;
                flex-direction: column; text-align: center; padding: 0 4rem;
                transform: translateY(100%); transition: .5s ease;
            }

            .portfolio-box:hover .portfolio-layer { transform: translateY(0); }
            
            .portfolio-layer h4 { font-size: 3rem; color: var(--main-color); text-shadow: 0 0 10px rgba(0,0,0,0.8); }
            .portfolio-layer p { font-size: 1.6rem; margin: .3rem 0 1rem; color: #fff; font-weight: 500; }
            
            .portfolio-layer a { display: inline-flex; justify-content: center; align-items: center; width: 5rem; height: 5rem; background: #fff; border-radius: 50%; }
            .portfolio-layer a svg { width: 2rem; height: 2rem; color: #333; }

            /* Portfolio Hover Effects */
            .portfolio-layer {
                position: absolute; bottom: 0; left: 0; width: 100%; height: 100%;
                background: linear-gradient(rgba(0,0,0,.8), var(--second-bg-color));
                display: flex; justify-content: center; align-items: center;
                flex-direction: column; text-align: center; padding: 0 4rem;
                transform: translateY(100%); transition: .5s ease;
            }
            .portfolio-box:hover .portfolio-layer { transform: translateY(0); }
            .portfolio-layer h4 { font-size: 3rem; color: var(--main-color); }
            .portfolio-layer p { font-size: 1.6rem; margin: .3rem 0 1rem; color: #fff; }
            .portfolio-layer a { display: inline-flex; justify-content: center; align-items: center; width: 5rem; height: 5rem; background: #fff; border-radius: 50%; }
            .portfolio-layer a svg { width: 2rem; height: 2rem; color: #333; }

            /* ================= CONTACT ================= */
            .contact form { max-width: 70rem; margin: 1rem auto; text-align: center; margin-bottom: 3rem; }
            .contact form .input-box { display: flex; justify-content: space-between; flex-wrap: wrap; }
            .contact form .input-box input, .contact form textarea {
                width: 100%; padding: 1.5rem; font-size: 1.6rem; color: var(--text-color);
                background: var(--second-bg-color); border-radius: .8rem; margin: .7rem 0;
            }
            .contact form .input-box input { width: 49%; }
            .contact form textarea { resize: none; height: 200px; }

            /* ================= FOOTER ================= */
            .footer { display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; padding: 2rem 9%; background: var(--second-bg-color); }
            .footer-text p { font-size: 1.6rem; }
            .footer-iconTop a { display: inline-flex; justify-content: center; align-items: center; padding: .8rem; background: var(--main-color); border-radius: .8rem; transition: .5s ease; }
            .footer-iconTop a:hover { box-shadow: 0 0 1rem var(--main-color); }
            .footer-iconTop a svg { width: 2.4rem; height: 2.4rem; color: var(--second-bg-color); }

            /* WA MODAL */
            .wa-modal { position: fixed; inset: 0; background: rgba(15, 25, 47, 0.9); display: flex; align-items: center; justify-content: center; z-index: 9999; opacity: 0; pointer-events: none; transition: .4s ease; }
            .wa-modal.active { opacity: 1; pointer-events: auto; }
            .wa-box { background: var(--second-bg-color); padding: 3rem 4rem; border-radius: 1.5rem; text-align: center; box-shadow: 0 0 25px var(--main-color); border: 1px solid var(--main-color); }
            .wa-box h3 { font-size: 2.4rem; color: var(--main-color); margin-bottom: 1rem; }
            .wa-box p { font-size: 1.6rem; margin-bottom: 2rem; }

            /* ================= THEME SWITCHER (OPTIMIZED RESPONSIVE) ================= */
            .theme-wrapper {
                position: fixed;
                bottom: 30px;
                right: 30px;
                z-index: 9999;
                display: flex;
                flex-direction: column-reverse; /* Menu muncul ke atas */
                align-items: center;
                gap: 15px;
                touch-action: none; 
            }

            /* Tombol Utama (Gear Icon) */
            .theme-btn {
                width: 50px;
                height: 50px;
                background: var(--second-bg-color);
                border: 2px solid var(--main-color);
                border-radius: 50%;
                color: var(--main-color);
                display: flex;
                justify-content: center;
                align-items: center;
                cursor: grab;
                box-shadow: 0 0 15px rgba(0, 0, 0, 0.5);
                transition: transform 0.2s, border-color 0.3s, color 0.3s;
                user-select: none;
                -webkit-tap-highlight-color: transparent;
            }

            .theme-btn:active {
                cursor: grabbing;
                transform: scale(0.95);
            }

            .theme-btn svg {
                width: 24px;
                height: 24px;
                animation: spinGear 8s linear infinite;
            }

            @keyframes spinGear { 100% { transform: rotate(360deg); } }

            /* Daftar Pilihan Warna */
            .theme-colors {
                display: flex;
                flex-direction: column;
                gap: 10px;
                background: rgba(15, 25, 47, 0.9);
                padding: 10px;
                border-radius: 50px;
                border: 1px solid var(--main-color);
                backdrop-filter: blur(5px);
                
                opacity: 0;
                visibility: hidden;
                transform: translateY(20px) scale(0.8);
                transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            }

            .theme-colors.active {
                opacity: 1;
                visibility: visible;
                transform: translateY(0) scale(1);
            }

            /* Tombol Warna Individu */
            .color-box {
                width: 32px;
                height: 32px;
                border-radius: 50%;
                cursor: pointer;
                border: 2px solid rgba(255,255,255,0.8);
                transition: transform 0.2s;
            }

            .color-box:hover {
                transform: scale(1.25);
                border-color: #fff;
            }

            /* Tombol Khusus RGB Loop */
            .rgb-btn {
                background: linear-gradient(135deg, red, orange, yellow, lime, cyan, blue, magenta, red);
                background-size: 400% 400%;
                animation: gradientBG 3s ease infinite;
            }
            @keyframes gradientBG { 0% {background-position: 0% 50%;} 50% {background-position: 100% 50%;} 100% {background-position: 0% 50%;} }


            /* ================= RESPONSIVE QUERY ================= */
            @media (max-width: 1200px) { html { font-size: 55%; } }
            @media (max-width: 991px) {
                .header { padding: 2rem 3%; }
                section { padding: 10rem 3% 2rem; }
                .services { padding-bottom: 7rem; }
                .portfolio { padding-bottom: 7rem; }
                .footer { padding: 2rem 3%; }
                .home { flex-direction: column; gap: 4rem; text-align: center; }
                .home-content { padding-top: 2rem; max-width: 100%; }
                .home-content h3 { font-size: 2.8rem; }
                .home-content h3:nth-of-type(2) { width: auto; min-width: 0; display: block; }
                .home-img { width: 100%; margin: 2rem auto; }
                .home-img .img-gradient img { width: 55vw; max-width: 400px; }
                .about { flex-direction: column; text-align: center; }
                .about-content h2 { text-align: center; }
                .about-img img { width: 70vw; margin-bottom: 2rem; }
            }
            @media (max-width: 768px) {
                #menu-icon { display: block; }
                .header { padding: 1.5rem 4%; }
                .header.sticky { padding: 1.2rem 4%; }
                .navbar {
                    position: absolute; top: 100%; left: 0; width: 100%; padding: 1rem 3%;
                    background: var(--bg-color); border-top: .1rem solid rgba(0,0,0,.2);
                    box-shadow: 0 .5rem 1rem rgba(0,0,0,.2); visibility: hidden; opacity: 0;
                    transform: translateY(-20px); transition: all 0.4s ease-in-out; 
                }
                .navbar.active { visibility: visible; opacity: 1; transform: translateY(0); }
                .navbar a { display: block; font-size: 2rem; margin: 3rem 0; }
                section { padding: 10rem 4% 2rem; }
                .home { gap: 5rem; }
                .home-content { flex-direction: column; align-items: center; }
                .home-content h3 { font-size: 2.4rem; letter-spacing: -0.5px; }
                .home-content h3:nth-of-type(2) { width: auto; min-width: 0; white-space: nowrap; }
                .home-content h1 { font-size: 5rem; }
                .home-img .img-gradient img { width: 75vw; max-width: 350px; }
                .portfolio-container { grid-template-columns: 1fr; }
                .contact form .input-box input { width: 100%; }
                .footer { flex-direction: column; justify-content: center; text-align: center; gap: 1.5rem; padding: 2.5rem 4%; }
                .footer-text { width: 100%; }
                .social-media a { margin: 0 1rem 3rem 1rem; }
            }
            @media (max-width: 450px) {
                html { font-size: 50%; }
                .home-content h3 { font-size: 2.2rem; letter-spacing: -1px; }
                .home-content h1 { font-size: 4rem; }
                .home-img .img-gradient img { width: 85vw; max-width: 320px; } 
                
                /* Tweak untuk tombol floating di HP kecil */
                .theme-wrapper { bottom: 20px; right: 20px; }
                .theme-btn { width: 45px; height: 45px; }
            }
        </style>
    </head>
    
    <body>

        <audio id="bg-music" src="Sound-Welcome.mp3"></audio>

        <div id="intro-overlay">
            <div class="intro-content">
                <img src="Logo-Anto-Relles/Anto-Relles.png" alt="Intro Profile">
                <h2 class="intro-text"></h2>
                <button id="enter-btn" class="btn">Enter Profile</button>
            </div>
        </div>

        <header class="header">
            <a href="https://www.tiktok.com/@antoo769?_r=1&_t=ZS-92ZlS9JbQsm" class="logo">Anto<span>Relles</span>.</a>
            <i id="menu-icon" data-feather="menu"></i>
            <nav class="navbar">
                <a href="#home" class="active">Home</a>
                <a href="#about">About</a>
                <a href="#Portfolio-Showcase">Portfolio Showcase</a>
                <a href="#my-rooms">My Rooms</a>
                <a href="#contact">Contact</a>
            </nav>
        </header>
    
        <section class="home" id="home">
            <div class="home-content">
                <h3>Hello It's Me</h3>
                <h1>Anto <span>Relles</span></h1>
                <h3>And I'm a <span class="multiple-text"></span></h3>
                <p></p>
                
                <div class="social-media">
                    <a href="https://www.tiktok.com/@antoo769?_r=1&_t=ZS-92ZlS9JbQsm" target="_blank"><i class="fa-brands fa-tiktok"></i></a>
                    <a href="https://youtube.com/@residendahu?si=E47sFY490dfRRLS1" target="_blank"><i class="fa-brands fa-youtube"></i></a>
                    <a href="https://www.instagram.com/anto_relles?igsh=MWtsOWhhZ25wOHByNg==" target="_blank"><i class="fa-brands fa-instagram"></i></a>
                    <a href="https://www.facebook.com/share/1FkVgGN3Gq/" target="_blank"><i class="fa-brands fa-facebook-f"></i></a>
                </div>

                <a href="https://wa.me/qr/XR7QMDO5I7FWN1" class="btn">
                    <i class="fa-brands fa-whatsapp fa-xl"></i> Cooperation/Endorsement
                </a>
            </div>

            <div class="home-img">
                <div class="img-gradient">
                    <img src="Logo-Anto-Relles/Anto-Relles.png" alt="Anto-Relles Profile" />
                </div>
            </div>
        </section>
    
        <section class="about" id="about">
            <div class="about-img">
                <img src="Logo-Anto-Relles/Anto-Relles-About.png" alt="Anto Relles About Me" />
            </div>

            <div class="about-content">
                <h2 class="heading">Tentang <span>saya</span></h2>
                <p>Saya adalah Affiliate Marketer, Content Creator, dan YouTuber yang membangun personal branding melalui konten kreatif dan strategi digital. Dengan pendekatan yang autentik dan berbasis pengalaman, saya menghadirkan rekomendasi produk serta konten yang memberikan dampak nyata bagi audiens.</p>
                <a href="main-html/about-me.html" class="btn">Baca selengkapnya</a>
            </div>
        </section>
    
        <section class="Portfolio-Showcase" id="Portfolio-Showcase">
            <h2 class="heading">Portfolio <span>Showcase</span></h2>
            <div class="services-container">
                <div class="services-box">
                    <div class="services-box-content">
                        <i class="fa-brands fa-tiktok fa-5x"></i>
                        <h3>TikTok Content</h3>
                        <p>Menciptakan konten kreatif, informatif, dan konsisten untuk membangun kepercayaan serta engagement audiens.</p>
                    </div>
                    <a href="main-html/tiktok.html" class="btn">View Portfolio</a>
                </div>

                <div class="services-box">
                    <div class="services-box-content">
                        <i class="fa-solid fa-store fa-5x"></i>
                        <h3>Affiliate Marketing</h3>
                        <p>Membantu audiens menemukan produk terbaik melalui rekomendasi yang jujur, relevan, dan bernilai.</p>
                    </div>
                    <a href="main-html/affiliate.html" class="btn">View Portfolio</a>
                </div>

                <div class="services-box">
                    <div class="services-box-content">
                        <i class="fa-brands fa-youtube fa-5x"></i>
                        <h3>YouTube Content</h3>
                        <p>Menyajikan video edukatif dan inspiratif yang membahas pengalaman, insight, dan peluang di dunia digital.</p>
                    </div>
                    <a href="main-html/youtube.html" class="btn">View Portfolio</a>
                </div>
            </div>
        </section>
    
        <section class="portfolio" id="my-rooms">
            <h2 class="heading">My <span>Rooms</span></h2>

            <div class="portfolio-container">
                
                <div class="portfolio-box">
                    <img src="foto-my-rooms/01.png" alt="Room 1">
                    <div class="portfolio-layer">
                        <h4>Gaming Setup</h4>
                        <p>Lihat Detail Gambar</p>
                        <a onclick="return false;"><i data-feather="eye"></i></a>
                    </div>
                </div>

                <div class="portfolio-box">
                    <img src="foto-my-rooms/02.png" alt="Room 2">
                    <div class="portfolio-layer">
                        <h4>Gaming Setup</h4>
                        <p>Lihat Detail Gambar</p>
                        <a onclick="return false;"><i data-feather="eye"></i></a>
                    </div>
                </div>

                <div class="portfolio-box">
                    <img src="foto-my-rooms/03.png" alt="Room 3">
                    <div class="portfolio-layer">
                        <h4>Gaming Setup</h4>
                        <p>Lihat Detail Gambar</p>
                        <a onclick="return false;"><i data-feather="eye"></i></a>
                    </div>
                </div>
                
                <div class="portfolio-box">
                    <img src="foto-my-rooms/04.png" alt="Room 4">
                    <div class="portfolio-layer">
                        <h4>Gaming Setup</h4>
                        <p>Lihat Detail Gambar</p>
                        <a onclick="return false;"><i data-feather="eye"></i></a>
                    </div>
                </div>
                
                <div class="portfolio-box">
                    <img src="foto-my-rooms/05.png" alt="Room 5">
                    <div class="portfolio-layer">
                        <h4>Gaming Setup</h4>
                        <p>Lihat Detail Gambar</p>
                        <a onclick="return false;"><i data-feather="eye"></i></a>
                    </div>
                </div>

                <div class="portfolio-box">
                    <img src="foto-my-rooms/06.png" alt="Room 6">
                    <div class="portfolio-layer">
                        <h4>Gaming Setup</h4>
                        <p>Lihat Detail Gambar</p>
                        <a onclick="return false;"><i data-feather="eye"></i></a>
                    </div>
                </div>
            </div>
        </section>
        <div id="imageModal" class="image-modal">
            <span class="close-modal">&times;</span>
            <img class="modal-content" id="img01">
        </div>
    
        <section class="comments-section" id="komentar-section">
            <h2 class="heading">Komentar <span>Pengunjung</span></h2>

            <div class="comment-form-container">
                <form action="" method="POST" style="max-width: 100%; margin: 0;">
                    <div class="input-box">
                        <input type="text" name="nama_pengunjung" placeholder="Nama Panggilan" required 
                            style="width: 100%; padding: 1.5rem; font-size: 1.6rem; color: var(--text-color); background: var(--second-bg-color); border-radius: .8rem; margin: .7rem 0;">
                    </div>
                    <textarea name="pesan_pengunjung" placeholder="Tulis komentar kamu di sini..." required 
                            style="width: 100%; height: 150px; padding: 1.5rem; font-size: 1.6rem; color: var(--text-color); background: var(--second-bg-color); border-radius: .8rem; margin: .7rem 0; resize: none;"></textarea>
                
                    <button type="submit" name="kirim_komentar" class="btn" style="margin-top: 1rem;">
                        Kirim Komentar
                    </button>
                </form>
            </div>

            <div class="comment-list">
                <?php
                // Mengambil data dari database (Terbaru paling atas)
                $result = mysqli_query($conn, "SELECT * FROM komentar ORDER BY id DESC");
            
                if (mysqli_num_rows($result) > 0) {
                    while ($row = mysqli_fetch_assoc($result)) {
                        // Ambil inisial huruf pertama untuk avatar
                        $inisial = strtoupper(substr($row['nama'], 0, 1));
                ?>
                    <div class="comment-card">
                        <div class="comment-header">
                            <div class="comment-avatar"><?php echo $inisial; ?></div>
                            <div>
                                <div class="comment-name"><?php echo htmlspecialchars($row['nama']); ?></div>
                                <div class="comment-date">
                                    <?php echo date('d F Y, jam H:i', strtotime($row['tanggal'])); ?> WIB
                                </div>
                            </div>
                        </div>
                        <div class="comment-body">
                            <?php echo htmlspecialchars($row['isi_pesan']); ?>
                        </div>
                    </div>
                <?php 
                    } 
                } else {
                    echo "<p style='text-align:center; font-size:1.6rem;'>Belum ada komentar. Jadilah yang pertama!</p>";
                }
                ?>
            </div>
        </section>

        <section class="contact" id="contact">
            <h2 class="heading">Contact <span>Me</span></h2>

            <form id="contactForm">
                <div class="input-box">
                    <input type="text" id="nama" placeholder="Masukan nama Anda" required />
                    <input type="text" id="pembahasan" placeholder="Topik pembicaraan" required />
                </div>
                <textarea id="pesan" cols="30" rows="10" placeholder="Masukan pesan Anda" required></textarea>
                <button type="submit" class="btn">Kirim Pesan</button>
            </form>
        </section>

        <div id="waModal" class="wa-modal">
          <div class="wa-box">
            <h3>✅ Message Sent</h3>
            <p>Your message has been prepared for WhatsApp.</p>
            <button id="waOk" class="btn">OK</button>
          </div>
        </div>

        <footer class="footer">
            <div class="footer-text">
                <p>Copyright &copy; 2026 by AEZeyrss | All Rights Reserved</p>
            </div>
            <div class="footer-iconTop">
                <a href="#home"><i class="fa-solid fa-angles-up fa-bounce fa-2x" style="color: #000000;"></i></a>
            </div>
        </footer>

        <script src="https://unpkg.com/scrollreveal"></script>
        <script src="https://unpkg.com/typed.js@2.1.0/dist/typed.umd.js"></script>

        <div class="theme-wrapper" id="themeWrapper">
            <div class="theme-colors" id="themeColors">
                <div class="color-box" style="background: rgb(18, 227, 255);" onclick="setColor('rgb(18, 227, 255)')"></div>
                <div class="color-box" style="background: rgb(132, 132, 130);" onclick="setColor('rgb(132, 132, 130)')"></div>
                <div class="color-box" style="background: rgb(3, 252, 61);" onclick="setColor('rgb(3, 252, 61)')"></div>
                <div class="color-box" style="background: rgb(255, 0, 13);" onclick="setColor('rgb(255, 0, 13)')"></div>
                <div class="color-box" style="background: rgb(255, 0, 234);" onclick="setColor('rgb(255, 0, 234)')"></div>
                <div class="color-box rgb-btn" onclick="startRgbMode()"></div>
            </div>
    
            <div class="theme-btn" id="themeBtn">
                <i data-feather="settings"></i>
            </div>
        </div>

        <script>
            feather.replace();

            /* ================= LOGIC INTRO & MUSIC (UPDATED) ================= */
            const introOverlay = document.getElementById('intro-overlay');
            const enterBtn = document.getElementById('enter-btn');
            const bgMusic = document.getElementById('bg-music');

            // Cek apakah user sudah melihat intro sebelumnya
            if (!sessionStorage.getItem('introPlayed')) {
                // Jika BELUM (First Visit) -> Tampilkan Intro
                document.body.style.overflow = 'hidden';

                setTimeout(() => {
                    new Typed('.intro-text', {
                        strings: ['Welcome to Website Anto Relles'],
                        typeSpeed: 50,
                        showCursor: false
                    });
                }, 800);

                // Event Listener Tombol Masuk
                enterBtn.addEventListener('click', () => {
                    // 1. Hilangkan Intro
                    introOverlay.classList.add('hide-intro');
                    document.body.style.overflow = 'auto';
                    
                    // 2. Tandai sudah masuk agar tidak muncul lagi saat kembali dari halaman lain
                    sessionStorage.setItem('introPlayed', 'true');

                    // 3. Putar Musik selama 8 detik
                    bgMusic.play().catch(error => {
                        console.log("Autoplay prevented by browser setting, user interaction required.");
                    });

                    setTimeout(() => {
                        bgMusic.pause();
                        bgMusic.currentTime = 0; // Reset ke awal
                    }, 17000); // Stop setelah 8000ms (8 detik)
                });

            } else {
                // Jika SUDAH (Return Visit) -> Sembunyikan intro sepenuhnya
                introOverlay.style.display = 'none';
                document.body.style.overflow = 'auto';
            }

            /* ================= LOGIC GANTI WARNA & RGB LOOP ================= */
            const r = document.querySelector(':root');
            let rgbInterval; // Variabel untuk menyimpan loop animasi

            function setColor(color) {
                // Matikan mode RGB jika user memilih warna statis
                clearInterval(rgbInterval);
                
                r.style.setProperty('--main-color', color);
                localStorage.setItem('preferredColor', color);
                document.getElementById('themeColors').classList.remove('active');
            }

            function startRgbMode() {
                // Hentikan interval sebelumnya jika ada (untuk mencegah double loop)
                clearInterval(rgbInterval);
                
                let hue = 0;
                
                // Jalankan loop perubahan warna setiap 20ms
                rgbInterval = setInterval(() => {
                    hue++;
                    // Menggunakan HSL untuk memutar spektrum warna (0-360 derajat)
                    const color = `hsl(${hue}, 100%, 50%)`;
                    r.style.setProperty('--main-color', color);
                    
                    // Reset hue jika sudah mencapai 360
                    if (hue >= 360) hue = 0;
                }, 20); // Kecepatan ganti warna (semakin kecil angkanya, semakin cepat)

                localStorage.setItem('preferredColor', 'rgb-loop');
                document.getElementById('themeColors').classList.remove('active');
            }

            // Cek penyimpanan saat website dimuat
            const savedColor = localStorage.getItem('preferredColor');
            if(savedColor === 'rgb-loop') {
                startRgbMode();
            } else if(savedColor) {
                setColor(savedColor);
            }

            /* ================= LOGIC DRAGGABLE RESPONSIVE ================= */
            const wrapper = document.getElementById('themeWrapper');
            const btn = document.getElementById('themeBtn');
            const menu = document.getElementById('themeColors');

            let isDragging = false;
            let startX, startY, initialLeft, initialTop;
            let hasMoved = false;

            function constrainToScreen() {
                const rect = wrapper.getBoundingClientRect();
                const winWidth = window.innerWidth;
                const winHeight = window.innerHeight;
                
                let newLeft = rect.left;
                let newTop = rect.top;

                if (newLeft < 10) newLeft = 10;
                if (newLeft + rect.width > winWidth - 10) newLeft = winWidth - rect.width - 10;
                if (newTop < 10) newTop = 10;
                if (newTop + rect.height > winHeight - 10) newTop = winHeight - rect.height - 10;

                wrapper.style.left = `${newLeft}px`;
                wrapper.style.top = `${newTop}px`;
                wrapper.style.right = 'auto'; 
                wrapper.style.bottom = 'auto';
            }

            window.addEventListener('resize', () => {
                wrapper.style.left = '';
                wrapper.style.top = '';
                wrapper.style.right = '20px';
                wrapper.style.bottom = '20px';
            });

            btn.addEventListener('click', (e) => {
                if (!hasMoved) {
                    menu.classList.toggle('active');
                }
            });

            function dragStart(e) {
                if (e.target.classList.contains('color-box')) return;

                isDragging = true;
                hasMoved = false;
                
                const clientX = e.type.includes('touch') ? e.touches[0].clientX : e.clientX;
                const clientY = e.type.includes('touch') ? e.touches[0].clientY : e.clientY;

                startX = clientX;
                startY = clientY;

                const rect = wrapper.getBoundingClientRect();
                initialLeft = rect.left;
                initialTop = rect.top;

                wrapper.style.right = 'auto';
                wrapper.style.bottom = 'auto';
                wrapper.style.left = initialLeft + 'px';
                wrapper.style.top = initialTop + 'px';

                document.body.style.userSelect = 'none';
            }

            function dragMove(e) {
                if (!isDragging) return;
                
                e.preventDefault(); 

                const clientX = e.type.includes('touch') ? e.touches[0].clientX : e.clientX;
                const clientY = e.type.includes('touch') ? e.touches[0].clientY : e.clientY;

                const dx = clientX - startX;
                const dy = clientY - startY;

                if (Math.abs(dx) > 5 || Math.abs(dy) > 5) {
                    hasMoved = true;
                }

                let newLeft = initialLeft + dx;
                let newTop = initialTop + dy;

                wrapper.style.left = `${newLeft}px`;
                wrapper.style.top = `${newTop}px`;
            }

            function dragEnd() {
                isDragging = false;
                document.body.style.userSelect = 'auto';
                constrainToScreen(); 
            }

            btn.addEventListener('mousedown', dragStart);
            window.addEventListener('mousemove', dragMove);
            window.addEventListener('mouseup', dragEnd);

            btn.addEventListener('touchstart', dragStart, { passive: false });
            window.addEventListener('touchmove', dragMove, { passive: false });
            window.addEventListener('touchend', dragEnd);

            /* ================= NAVBAR & SCROLL LOGIC ================= */
            const menuIcon = document.querySelector("#menu-icon");
            const navbar = document.querySelector(".navbar");

            menuIcon.onclick = () => {
                navbar.classList.toggle("active");
                if(navbar.classList.contains("active")) {
                    menuIcon.innerHTML = feather.icons['x'].toSvg();
                } else {
                    menuIcon.innerHTML = feather.icons['menu'].toSvg();
                }
            };

            let sections = document.querySelectorAll("section");
            let navLinks = document.querySelectorAll("header nav a");

            window.onscroll = () => {
                sections.forEach(sec => {
                    let top = window.scrollY;
                    let offset = sec.offsetTop - 150;
                    let height = sec.offsetHeight;
                    let id = sec.getAttribute("id");

                    if(top >= offset && top < offset + height) {
                        navLinks.forEach(link => {
                            link.classList.remove("active");
                            document.querySelector('header nav a[href*=' + id + ']').classList.add("active");
                        });
                    }
                });

                let header = document.querySelector(".header");
                header.classList.toggle("sticky", window.scrollY > 100);

                navbar.classList.remove("active");
                if(menuIcon) menuIcon.innerHTML = feather.icons['menu'].toSvg();
            };

            ScrollReveal({
                reset: true,
                distance: "80px",
                duration: 2000,
                delay: 200,
            });

            ScrollReveal().reveal(".home-content, .heading", { origin: "top" });
            ScrollReveal().reveal(".home-img, .services-container, .contact form", { origin: "bottom" });
            ScrollReveal().reveal(".home-content h1, .about-img", { origin: "left" });
            ScrollReveal().reveal(".home-content p, .about-content", { origin: "right" });
            ScrollReveal().reveal(".portfolio-box", { origin: "bottom", interval: 200 });

            new Typed(".multiple-text", {
                strings: ["Affiliate Marketer", "Content Creator", "YouTuber Gaming"],
                typeSpeed: 100,
                backSpeed: 60,
                backDelay: 1000,
                loop: true,
            });

            /* ================= LOGIC CONTACT FORM (FIXED) ================= */
            const form = document.getElementById("contactForm");
            const modal = document.getElementById("waModal");
            const okBtn = document.getElementById("waOk");

            if(form) {
                form.addEventListener("submit", function(e) {
                    e.preventDefault(); // Mencegah reload halaman

                    // 1. Ambil value dari input sesuai ID di HTML
                    const nama = document.getElementById("nama").value;
                    const pembahasan = document.getElementById("pembahasan").value;
                    const pesan = document.getElementById("pesan").value; // ID di HTML adalah "message"
                    
                    // 2. Nomor WhatsApp Admin (Gunakan format internasional tanpa +)
                    const adminNumber = "6285709011874"; 
                    
                    // 3. Susun Pesan WhatsApp (Gunakan variabel yang benar: nama, pembahasan, message)
                    // Saya tambahkan format tebal (*) dan enter (\n) agar rapi di WA
                    const text = `*Halo Admin Anto Relles, saya ingin bertanya.*\n\nNama: ${nama}\nTopik: ${pembahasan}\nPesan: ${pesan}`;
                    
                    // 4. Buat URL WhatsApp
                    const url = `https://wa.me/${adminNumber}?text=${encodeURIComponent(text)}`;

                    // 5. Buka WhatsApp di tab baru
                    window.open(url, "_blank");
                    
                    // 6. Tampilkan Modal Sukses & Reset Form
                    modal.classList.add("active");
                    form.reset();
                });
            }

            if(okBtn) {
                okBtn.onclick = () => modal.classList.remove("active");
            }

            if(okBtn) {
                okBtn.onclick = () => modal.classList.remove("active");
            }

            // Logic untuk membuka gambar saat ikon mata diklik
            const imgModal = document.getElementById("imageModal");
            const modalImg = document.getElementById("img01");
            const closeBtn = document.querySelector(".close-modal");
        
            // Ambil semua tombol mata di dalam portfolio
            const detailButtons = document.querySelectorAll('.portfolio-layer a');

            detailButtons.forEach(btn => {
                btn.addEventListener('click', function(e) {
                    // Cari gambar asli di dalam kotak yang sama
                    const parentBox = this.closest('.portfolio-box');
                    const imgSource = parentBox.querySelector('img').src;
                
                    // Tampilkan gambar di modal
                    modalImg.src = imgSource;
                    imgModal.classList.add('show');
                });
            });

            // Tutup Modal saat tombol X diklik
            closeBtn.onclick = function() {
                imgModal.classList.remove('show');
            }

            // Tutup Modal saat area hitam diklik
            imgModal.onclick = function(e) {
                if (e.target === imgModal) {
                    imgModal.classList.remove('show');
                }
            }
        </script>
    </body>
</html>
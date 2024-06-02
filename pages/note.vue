<template>
 <div class="container">
    <h1>Nama Project</h1>
    <p class="teks">TO-DO-LIST-APP</p>
    <h2>Kegunaan</h2>
    <p class="teks-dua">
 To Do List ini adalah Project yang sangat berguna untuk mengelola waktu dan tugas Anda dengan efisien. Dengan antarmuka yang intuitif dan fitur-fitur yang dapat disesuaikan, Project ini membantu Anda membuat daftar tugas harian, mingguan, atau bulanan dengan mudah.</p>
  </div>
</template>

<style>
 body {
  font-family: 'Fira sans', sans-serif, arial;
      background-color: rgb(83, 252, 83);
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #333;
      color: #fff;
      padding: 20px;
      text-align: center;
    }
    .container {
      width: 80%;
      margin: 20px auto;
    }
    h1 {
      text-align: center;
      display: flex;
      justify-content: center;
      color: black;
    }
    .container .teks {
      color: black;
      font-size: 1.2rem;
      text-align: right;
      display: flex;
      justify-content: center;
      line-height: 1.2;
      font-style: italic;
      margin: 10px;
    }
    p {
      line-height: 1.6;
    }
    .container .teks-dua {
      font-size: 2rem;
    }
    h2 .teks-dua {
     margin: 20px auto;
    }
    .container h2 {
      font-size: 2rem;
      font-style: italic;
      margin-bottom: 10px;
    }
</style>

<script>
export default {

}
</script>

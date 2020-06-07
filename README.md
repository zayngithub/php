<?php
session_start();
$user = $_POST["usr"];
$pass = $_POST["pass"];
//==============================
$dbuser = "admin";
$dbpass = "admin";
//==============================
if($user == $dbuser && $pass == $dbpass){
	echo "<script>alert('Sucess');window.location = ('dashboard.php')</script>";
} else {
    if(isset($_SESSION["salah"])){
        $_SESSION["salah"]++;
    } else{
        $_SESSION["salah"] = 1;
    }
    echo "<script>alert('Wrong password or username'); window.location = ('index.php')</script>";
}
Penjelasan
Tag inj berisi tentang cara memulai sesi 
Dengan cara memasukan unser pas dan unser name
Jika unser pas dan unser name nya benar maka muncul tulisan aelanjutnya
Jika slaah akan muncul tulisan silahkan coba lagi

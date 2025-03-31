# Temas del Cuatrimestre en la materia de Sistemas Telematicos 

1) Iniciamos con el curso de linux [LINUX](https://www.netacad.com/courses/fundamentos-de-linux?courseLang=es-XL&instance_id=6ba0d05e-8a4c-4303-aceb-9bbd10047548&authuser=0)
2) Seguimos con HESTIA, un panel de control Linux que permite administrar servicios de alojamiento, correo electrónico, base de datos, y más. [HESTIA](https://hestiacp.com/?authuser=0).
3) Continuamos con la creacion de un dominio con ayuda de el siguiente video en youtube [Video para crear dominio](https://www.youtube.com/playlist?list=PL-aSvPEYgSGij1bg9HvlLZAJahMNGunX7&authuser=0)
4) Para ver en que zonas esta disponible tu dominio puedes checarlo con el siguiente link [DNS](https://www.whatsmydns.net/?authuser=0)
5) En este link se  utilizará una cuenta gratuita de Oracle Cloud para configurar una instancia de Ubuntu. Se instalará un servidor web Apache y PHP y accederá al nuevo servidor desde Internet. Por último, este tutorial incluye todos los pasos necesarios para configurar una red virtual para su host y conectar el host a Internet.[INSTALLAPACHE](https://docs.oracle.com/en-us/iaas/developer-tutorials/tutorials/apache-on-ubuntu/01oci-ubuntu-apache-summary.htm?authuser=0)
6) Los comandos de linux mas comunes y utilizados en el entorno [COMANDOSLINUX](https://www.ionos.mx/digitalguide/servidores/configuracion/scp-de-linux/?authuser=0)
7) Para cambiar el hostname de ubuntu te puedes guiar con el siguiente link [CAMBIARHOSTNAMEUBUNTU](https://linuxize.com/post/how-to-change-hostname-on-ubuntu-22-04/?authuser=0)
8) Aqui te dejare algunos pasos para que cambies el nombre de tu dominio para HESTIA mendiante comandos los tienes que ejecutar como root
* cd /usr/local/hestia/bin/
* v-change-sys-hostname luisreylara.tech
* v-add-letsencrypt-host
7) OverTheWire es una plataforma en línea que ofrece una colección de juegos de guerra . Estos juegos te enseñan los fundamentos de la ciberseguridad mediante desafíos prácticos [BANDIT](https://overthewire.org/wargames/bandit/?authuser=0)
8) El wargame de Natas esta diseñado para aprender sobre vulnerabilidades web, estas vulnerabilidades se irán haciendo más sofisticadas con forme subas de nivel [NATAS](Vhttps://overthewire.org/wargames/natas/)
9) PHP para insertar datos 
* $servername = "";
* $username = "";
* $password = "";
* $dbname = "";

* // Create connection
* $conn = new mysqli($servername, $username, $password, $dbname);
* // Check connection
* if ($conn->connect_error) {
* die("Connection failed: " . $conn->connect_error);
* }

* $sql = "INSERT INTO registro (sensor, valor)
* VALUES ('temperatura', 22)";

* if ($conn->query($sql) === TRUE) {
* echo "Nuevo registro creado exitosamente";
* } else {
* echo "Error: " . $sql . "<br>" . $conn->error;
* }

* $conn->close();
* ?>
9) POSTMAN sus principales características y funcionalidades son: Envío de solicitudes. Permite enviar solicitudes GET, POST, PUT, DELETE y otros métodos HTTP a una API especificando los parámetros, encabezados y cuerpo de la solicitud. [POSTMAN](https://www.postman.com/)
10) Este código en PHP sirve para detectar y mostrar el método de solicitud HTTP utilizado en la petición al servidor.
* // r0.php
* $dato = $_SERVER['REQUEST_METHOD'];
* echo $dato;
* switch ($_SERVER['REQUEST_METHOD']){
*case 'POST':
* echo "POST";
* break;
* case 'GET':
* echo "GET";
* break;
* case 'PUT':
* echo "PUT";
* break;
* }
* ?>
11) Este código en PHP maneja una solicitud HTTP de tipo POST y verifica la existencia de ciertos datos enviados al servidor
* // r1.php
* $nombre = $_POST['midato'];
* if($_SERVER['REQUEST_METHOD'] == 'POST')
* {
* if (isset($_REQUEST['dato'])){
* $rfid = $_REQUEST['dato'];
* }else{
* echo "no existe variable";
* }
* echo $rfid;
* }
* ?>
12) Este código en PHP está diseñado para recibir datos enviados mediante POST, específicamente en formato JSON
* //r2.php
* $nombre = $_POST['midato'];
* if($_SERVER['REQUEST_METHOD'] == 'POST')
* {
*  $datos= json_decode(file_get_contents('php://input'));
* echo $datos->nombre;
* echo ("\n");
* echo $datos->ap;
* }
* ?>
13) Este código en C++ está diseñado para ejecutarse en un ESP32 o ESP8266, permitiendo que el microcontrolador se conecte a una red WiFi y envíe datos a un servidor web mediante una solicitud HTTP POST
* #include <WiFi.h>
* #include <HTTPClient.h>
* const char *ssid = "";
* const char *password = "";
* void WiFi_Setup() 
* {
* Serial.print("Conectando a ");
* Serial.println(ssid);
*WiFi.begin(ssid, password);
* int contador = 0;
* while (WiFi.status() != WL_CONNECTED && contador < 20 ) {
* delay(500);
* Serial.print(".");
* contador += 1;
* }
* if (WiFi.status() == WL_CONNECTED) {
* Serial.println("");
* Serial.println("WiFi conectado");
* }else {
* ESP.restart();
* }
* }
* void setup() 
* {
* Serial.begin(115200);
* WiFi_Setup();
* }
* void loop() 
* {
* HTTPClient http;
* String RFID = "valor del sensor";
* String datos_a_enviar = "rfid=" + RFID;
* Serial.println(datos_a_enviar);
* http.begin("https://ip/xxxx.php");       
* http.addHeader("Content-Type", "application/x-www-form-urlencoded");
* int codigo_respuesta = http.POST(datos_a_enviar);   
* if (codigo_respuesta > 0) 
* {
* if (codigo_respuesta == 200) 
* {
* String cuerpo_respuesta = http.getString();
* Serial.println(cuerpo_respuesta);
* }
* } 
* else 
* {
* Serial.println(codigo_respuesta);
* }
* http.end();  
* }
14) Primeros pasos con github [GITHUB](https://codegym.cc/es/groups/posts/es.379.primeros-pasos-con-git-una-guia-completa-para-principiantes?authuser=0)
15) Crear REPOSITORIO en github [REPOSITORIO](https://www.youtube.com/watch?v=vlCXdvcgiE0&authuser=0)
16) Publicar un sitio web gratis con Github pages [CREARPAGINA](https://www.youtube.com/watch?v=OZDKNqMXSxA&authuser=0) [PUBLICARSITIOWEB](https://www.youtube.com/watch?v=sLTNgxxSBR4&authuser=0)
17) Markdown para documentacion tecnica en GITHUB [MARKDOWN](https://experienceleague.adobe.com/es/docs/contributor/contributor-guide/writing-essentials/markdown?authuser=0)


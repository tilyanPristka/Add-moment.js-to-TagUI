<img src="https://1.tilyanpristka.id/images/tP-logo-rounded.png" height="111" align="right">

# Add [moment.js](https://momentjs.com/downloads/moment.min.js) to <img src="https://1.tilyanpristka.id/images/tagui.png" height="45"> TagUI (Date Formater)

#### How to do that
1. Add [moment.js](https://momentjs.com/downloads/moment.min.js) to `/tagui/src`

![image](https://user-images.githubusercontent.com/97102924/159395329-193f4e04-9873-4adb-9138-06515e5d322b.png)

2. Open `/tagui/src/tagui_parse.php`
- Add this code at line 22: `$moment_file = fopen('moment.js','r') or die("ERROR - cannot open moment.js" . "\n");`

![image](https://user-images.githubusercontent.com/97102924/159395597-05acf3e7-f53a-49a8-9990-0f7cac0d2ea0.png)

- Add this code at line 75: `while(!feof($moment_file)) {fwrite($output_file,fgets($moment_file));} fclose($moment_file);`

![image](https://user-images.githubusercontent.com/97102924/159395740-b588715c-ee96-4d02-8372-745156de481d.png)


#### Testing
- Create `test.tag`

![image](https://user-images.githubusercontent.com/97102924/159398966-3901580f-1227-4241-9446-d8ea33475561.png)

- Run `tagui test.tag`

![image](https://user-images.githubusercontent.com/97102924/159399061-ce109a57-9cb0-4968-8533-9ca918e78a15.png)

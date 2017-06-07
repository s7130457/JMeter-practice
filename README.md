# JMeter-practice  
STV JMeter練習  
Testing Tool：   
JMeter：   
http://jmeter.apache.org/download_jmeter.cgi    
選擇Apache JMeter 3.2 -> Binaries -> apache-jmeter-3.2.zip

plugins-manager.jar：     
https://jmeter-plugins.org/install/Install/       
下載完成後，將plugins-manager.jar放入JMeter的lib/ext中     
  
PerfMon：      
點擊JMeter -> bin -> ApacheJMeter.jar 進入JMeter      
Options -> Plugin Manager -> Availabke Plugins -> PerfMon       
  
JSON Plugins：     
點擊JMeter -> bin -> ApacheJMeter.jar 進入JMeter      
Options -> Plugin Manager -> Availabke Plugins -> PerfMon       
  
先開啟Docker後下指令     
docker run -ti -d -P gcaaa31928/2017_ntut_stv_lab4      
docker run -ti -d -p 8081:80 -p 4444:4444 a60814billy/2016_ntut_csie_stv_lab4     
  
測試情境：   
一、Login (The number of concurrent users for the stress testing : maximum 1024 users , minimum 2 users.)     
請將提供的Login腳本，更改成全部人登入完畢再一起登出。   

一組腳本有設Ramp-up，一組腳本沒設Ramp-up。    

請將兩組腳本做一個比較。    

有設定Ramp-up的腳本，請在256使用者設為10秒內讓所有使用者皆登入完成。    
有設定Ramp-up的腳本，請在512使用者設為20秒內讓所有使用者皆登入完成。    
有設定Ramp-up的腳本，請在1024使用者設為40秒內讓所有使用者皆登入完成。   

　

二、ISBN Search books (The number of concurrent users for the stress testing : maximum 1024 users , minimum 2 users.)   
情境1: 請撰寫一個腳本，利用書本的ISBN號碼進行查詢書本，並等全部人都收尋完畢後，再進行登出。   

情境2: 請撰寫一個腳本，等待全部人都登入完成，再進行書本的ISBN號碼查詢書本，並等全部人都收尋完畢後，再進行登出。   

ISBN請利用JMeter隨機挑選 (Do NOT hard code the ISBN. You may need to write a JavaScript code for selecting the ISBN randomly)。   

請將兩組腳本做一個比較。    

兩個腳本皆會設定Ramp-up，請在256使用者設為10秒內讓所有使用者皆登入完成。    
兩個腳本皆會設定Ramp-up，請在512使用者設為20秒內讓所有使用者皆登入完成。    
兩個腳本皆會設定Ramp-up，請在1024使用者設為40秒內讓所有使用者皆登入完成。   
　

三、Check in books / Check out books (The number of concurrent users for the stress testing : maximum 256 users , minimum 2 users.)     (submit two test scripts, 繳交兩個腳本)   
情境1 : 請撰寫一個腳本，利用書本的code號碼進行借書和還書，並等全部人都借完和還完後，再進行登出。    

情境2 : 請撰寫一個腳本，等待全部人都登入完成，在進行利用書本的code號碼借書和還書，並等全部人都借完和還完後，再進行登出。    

書本code請利用JMeter隨機挑選 (Do NOT hard code the book code. You may need to write a JavaScript code for selecting the book code randomly)。   

請借完書馬上進行還書，否則會造成其他使用者無法借書。    

請將兩組腳本做一個比較。    

兩個腳本皆會設定Ramp-up，請在64使用者設為10秒內讓所有使用者皆登入完成。   
兩個腳本皆會設定Ramp-up，請在128使用者設為20秒內讓所有使用者皆登入完成。    
兩個腳本皆會設定Ramp-up，請在256使用者設為40秒內讓所有使用者皆登入完成。    

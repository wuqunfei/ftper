##English
1.Maybe this is the most powerful ftp server library in this world.<br>
2.Developed on Python pyftp lib, thanks for the suggestion from Author in 3 months communication <br>
3.With Multiprocess library, feitp-server uses multi-cpu resources to promote performance. <br>
4.10X times than Vsftp, 5X times than pyftplib (Depend on your hardware capability) <br>
5.Good stability in 5 millions clients in Shanghai TV box ftp product environment. <br>
6.Easy expend and left API to developer like Login,upload,logout etc. <br>

##Deutsch
1.Das ist vielleicht die stärkste ftp-Server-Lib auf dieser Welt. <br>
2.Entwicklung auf Python pyftp lib. Danke für den Vorschlag von Autor während der 3 monatlichen Kommunikation.<br>
3.Mit Hilfe von Multi-Prozess-Lib verwendet feitp-Server Multi-CPU-Ressourcen, um die Leistungen zu fördern. <br>
4.10 Mals schneller als Vsftp, 5 Mals schneller als pyftplib (abhängig von Ihrer Hardware-Fähigkeit) <br>
5.Gute Stabilität für 5 Millionen Kunden in Shanghai TV-Box ftp Produktumgebung. <br>
6.Leicht zur Weiterentwicklung. Es gibt API, damit Entwickler anmelden, hochladen, abmelden, usw. können.<br>

SouceCode is still on GoogleCode https://code.google.com/p/feitp-server/

First lib is pyftpdlib which is a high-level portable interface to easily write asynchronous FTP servers.
Secondly, multiprocessing lib is good method let you to use multi-CPU in your machine replacing the 1 CPU running all threading.Thirdly, I rewrite the pyftpdlib sourcecode.


###Some params need to config

	*1.In Linux
		$ulimit -n max_open_file_number
		$ulimit -s min_buffer_in_one_thread

	*2.In Process
	I suggest that you can use double of your CPU number for yout ftp processes.
	Process(N) = CPU(N) 2

	*3.In FTP code
	tcp_no_delay = True
	max_connection = max_your_can
	use_simply_auth when you login
	the default of income_buffer which you can change with your logic

###Screenshot 1900 TPS for 50 Client together, No failed,Response at 0.005~0.0035 ms.

![image](https://farm7.staticflickr.com/6108/6331353252_8d435a1e0c_b_d.jpg)

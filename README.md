Chào ®™©2014-2020 Virgo Sun +84-387554874.

MULTI-DEVICE MULTI-PLATROM CROSS-PLATFORM 

![image](https://github.com/user-attachments/assets/ee1d75d4-4008-4f7e-9360-0ca787082945)TunnelsMux®™©2014-2020  a ![image](https://github.com/user-attachments/assets/4cd44ede-2ce8-41ff-a8d9-accb333e7069) sibling


iPhone Android Laptop MacBook PC Home/SOHO Server 

Chính chủ, độc quyền TQ (Sim Viettel bất kỳ bạn đang sử dụng, chúng tôi chỉ bán app)

1 app duy nhất WYSIWYG. Viettel 0đ 0 nền. Tốc độ 2Mbps -> 150k / 1 SIM.  Ko limit dung lượng. Đến khi hỏng SIM. (Bạn đã hiểu và đồng ý cam kết Mutual Agreement khi sử dụng app của chúng tôi. Chúng tôi luôn hỗ trợ bền bỉ tối đa, sản phẩm, dịch vụ chuyên nghiệp, độc đáo, có 1-0-2, trong khả năng có thể. Chúng tôi không cam kết các chính sách của nhà mạng. Chúng tôi không cam kết dịch vụ máy chủ VPS V2RAY)

1 app duy nhất WYSIWYG. Viettel 0đ 0 nền. Tốc độ 54Mbps -> 550k /1 SIM. Ko limit dung lượng. Đến khi hỏng SIM. 54mbps (IDM), 10Mbps (Visual Studio Isntaller), 5Mbps (Play Store), 3Mbps (Edge download).... (Bạn đã hiểu và đồng ý cam kết Mutual Agreement khi sử dụng app của chúng tôi. Chúng tôi luôn hỗ trợ bền bỉ tối đa, sản phẩm, dịch vụ chuyên nghiệp, độc đáo, có 1-0-2, trong khả năng có thể. Chúng tôi không cam kết các chính sách của nhà mạng, Chúng tôi không cam kết dịch vụ máy chủ VPS V2RAY)

Multiple SNIs, backup, load balancing, tính năng quét SNIs, test internet nhiều SNIs, trực tiếp bên trong app CORE TunnelsMux

Cảnh báo lừa đảo trên mạng xã hội, Voz.vn, GocMod.com, Openwrt Việt nam Facebook, Nhóm Psiphon Zalo ..v.v.

Termux + aztecrabit's Brainfuck Psiphon Pro Go ko thể chạy trên iOS và iPhone :D
```
Kể từ tháng 10/2023
1 số đối tượng dùng Termux, HC, INPV ăn cắp duy nhất 01 SNI IP xxx.x3x.xxx.x7x
Sẽ bị khóa
Mã code terminal TERMUX scan bug SNI sau là bịp bợm bố láo ăn cắp,
Không thể quét SNI từ TERMUX
void scan(int a, int b, int c, int d, float t) {
    int lv;

    system("date +%H%M >sgr");

    FILE *sG = fopen("sgr", "r");
    fscanf(sG, "%d", &lv);

    if(lv >= nx) {
        printf("\033[1;31mThời gian dùng thử của bạn đã hết, vui lòng liên hệ tác giả.\033[0m\n");
    }
    else {
        char buf[250];
        double m = t;
        snprintf(buf, 250, "\ncurl https://%d.%d.%d.%d --tlsv1.2 --tls-max 1.2 --connect-timeout %.4f -m %.4f -k -o /dev/null -s -w \"%%{remote_ip} timeout!: %%{response_code}\\n\" > host.txt", a, b, c, d, t, m);
        char fast[50];
        char second[50];
        char buk[250];
        int sts;
        system(buf);
        FILE *fptr;
        FILE *fptr1;
        FILE *fptr2;
        FILE *fp1;

        fptr = fopen("host.txt", "a");
        fptr1 = fopen("host.txt", "a");
        fptr2 = fopen("host.txt", "a");

        fptr = fopen("host.txt", "r");
        fscanf(fptr, "%s", fast);

        system("cut -f 2- -d ' ' host.txt > host1.txt");

        fptr1 = fopen("host1.txt", "r");
        fscanf(fptr1, "%s", second);
        system("cut -f 2- -d ' ' host1.txt > host2.txt");

        fptr2 = fopen("host2.txt", "r");
        fscanf(fptr2, "%d", &sts);

        if(sts == 000) {
            printf("\033[1;31m%s\033[0m\n", fast);
        }
        else {
            printf("\033[1;32m%s\033[0m ", fast);
            printf("\033[1;32m√\033[0m\n");
            snprintf(buk, 250, "echo \"%d.%d.%d.%d\" >>bugs", a, b, c, d);
            system(buk);
        }
    }
}
```


Lưu ý, nguyên lý ghép kênh chỉ đạt tốc độ cao với 1 số ứng dụng có hỗ trợ tải đa luồng. Mọi quảng cáo SpeedTest Termux 5Mbps 10Mbps cho tất cả ứng dụng đều là bố láo ăn cắp.
```
Căn cứ vào code snippets 
Termux ko phân chia đa luồng, do ứng dụng tự đảm nhiệm
BrainFuck Psiphon Pro Go của aztecrabbit
ko có cơ chể tự động gộp đa luồng.

package libproxyrotator

import (
	...
	"github.com/armon/go-socks5"
	...
)
...
Dial: func(ctx context.Context, net_, addr string) (net.Conn, error) {
			for i := 0; i < len(p.Proxies); i++ {
				proxyAddress, err := p.GetProxy()
				if err != nil {
					break
				}

				dialer, err := proxy.SOCKS5("tcp", proxyAddress, nil, proxy.Direct)
				if err != nil {
					panic(err)
				}

				data, err := dialer.Dial(net_, addr)
				if err != nil {
					continue
				}
...
if err := server.ListenAndServe("tcp", "0.0.0.0:"+p.Config.Port); err != nil {
		liblog.LogException(err, "INFO")
		os.Exit(0)
	}
			
```


Thanks to the Tor BSD Diversity Project  and inspire from this fork https://github.com/sonvirgo/meek

```
Why TunnelsMux?
Currently 1 tunnel has a speed of ~ 1Mbps.
By multiplex aka MUX tunnels, we get a higher speed.
The key price therefore base on number of muxed tunnels.
Basic key include 3 tunnels .~ 150k.
Muxed tunnels can reach practically as many as 72 tunnels tested ~ 550k
Theory number of tunnels to multiplex is limited by int64 value aka ~ 64k tunnels.
But in practical , MAX SPEED is limited varies according to actual ISP 4G geo-location.
For Viettel - 65Mbps reached with strong 4G signal ~ -100dbm
whilst  some Termux scammer may tell you about 100 cores etc, all is not only wasting resources also blocking your useful data channel..
Moreover, TUNNELS  programming is lightweight compared to simply changing Brainfuck Psiphon EXECUTE cores like scammers are doing.
Lastly, HC and INPV file lack all facility for multiplexing, render them useless.

This TunnelsMux app EXPLOITS the ISP network through MEEK protocol.
```
The app exposes a tunneled port to your VPN app of choice - [open-source SocksDroid v1.0.4 recommended](https://github.com/bndeff/socksdroid) - on Android - or [open-source POTATSO recommended](https://www.potatso.com/) - on iOS - or [Rule based, paid app ShadowRocket](https://shadowrocket-app.com/) 
```
Without an authorization key, app runs in TRIAL mode.
Tunneled port DISCONNECTED and CHANGED every 1 MINUTE.
To activate app to FIXED tunneled port UNINTERRUPTED. Contact the author!!!!
Thanks to all the loyalty customers so far! :D
```


[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/gNp4vhKzqIo/0.jpg)](https://www.youtube.com/watch?v=LSjL13jmjUA)
![image](https://github.com/sonvirgo/sonvirgo/assets/10823037/17d2bacb-67b2-4087-8379-b2f8551fce08)
<img width="762" alt="image" src="https://github.com/sonvirgo/4G-Circumvent/assets/10823037/a81915c6-4b58-4eb6-b931-35bf0df1c1dd">

![image](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/6e0b0e22-37b8-4616-a107-3e5649506f0f)
![image](https://github.com/sonvirgo/sonvirgo/assets/10823037/a5d5c438-39cc-4cfa-aafa-3fa38535d4a2)
# 4G-Circumvent
Sell 4G app to circumvent the prohibition to the internet 

How it works:

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/JdcoDcOBtCI/0.jpg)](https://www.youtube.com/watch?v=JdcoDcOBtCI)
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/kWE9mbjHXgQ/0.jpg)](https://www.youtube.com/watch?v=kWE9mbjHXgQ)

How other FAKE:

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/5z0rwvc-4dw/0.jpg)](https://www.youtube.com/watch?v=5z0rwvc-4dw)

How much does it cost:

[![IMAGE ALT TEXT HERE](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/54ff2872-d053-4c04-9113-89166f208e01)](https://www.youtube.com/watch?v=K3uY3K2k3eg)


![Screenshot_20240315-111410](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/ab83e198-18d5-4db0-8797-917126330a82)

![z5165194400343_7daf64321ece92911539069a9695679c](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/64116b6b-eb25-4cf8-b32f-5b320e999b48)
![Screenshot 2024-02-16 at 15 15 35](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/b229111c-ecf9-4cc0-b9ae-de2d634a83e1)


![image](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/2030d1f0-2926-4a0d-86a2-9a2a0e8dcc8e)

![image](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/b3c86673-4b45-4cbf-80a0-055b260e09b1)
![image](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/01c0fceb-53a0-41f1-9f61-3f272947b008)

![image](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/ae703f7f-cbeb-4f9e-b8f9-6c999c761b66)


![image](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/be99ba1a-c636-40ea-b186-39175506ddf2)

![image](https://github.com/sonvirgo/4G-Curcumvent/assets/10823037/cb1f73fa-2387-48f2-9fe2-1e8118469ae2)


![Screenshot 2024-01-09 110444](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/b3245eff-2c2a-4012-94a1-35edbf13df60)
![Screenshot 2024-01-09 110538](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/3502eb4b-d61a-4d8a-8080-37613a062662)
![Screenshot 2024-01-09 110222](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/f39427ca-dbb1-44b8-aa8e-8e2cdb8b988a)
![Screenshot 2024-01-09 111836](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/38b3a5e2-e74c-439c-be53-0c61890538c9)


![425936998_3273179726320005_7350559048678956135_n](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/6d4f047a-2f72-4db9-b8bd-a7ae90d47bc5)
![Screenshot 2024-02-04 at 21 15 02](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/1737b449-284a-4c2b-9ab1-f9f2cae2837b)
![422624776_3273179519653359_431070138987956855_n](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/d17d6254-0e7a-4892-927a-eae805874f63)

![image](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/10d3d73f-0a50-4977-b1c0-577975c9921a)

![image](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/fcbc9c30-4ef3-479c-bf32-f0aae8c8e2af)

![image](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/fb6073b2-2574-4e4a-98c1-98da58e06459)
![image](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/43c7db9d-b40b-481f-aeeb-adc5771125e0)

![image](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/61ba53f0-9995-4962-ba33-a6c9fbc20110)

![image](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/de75b80a-6e1a-4be5-932d-bd66236e07eb)
![Screenshot_20240628-221545](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/b7f27150-b282-4e92-900d-bf6bf2b28850)


![Screenshot_20240628-221334](https://github.com/sonvirgo/4G-Circumvent/assets/10823037/5d575efc-25d5-49f8-bd50-3fc2f2e824db)
![image](https://github.com/sonvirgo/4G-Circumvent-Commercial-Grade-Number-1-Nation-Wide/assets/10823037/3710a5af-2dff-4468-91c5-b809754bb273)
![image](https://github.com/sonvirgo/4G-Circumvent-Commercial-Grade-Number-1-Nation-Wide/assets/10823037/e699de6f-ef46-48b0-b09e-cd60c4de01b2)
![image](https://github.com/sonvirgo/4G-Circumvent-Commercial-Grade-Number-1-Nation-Wide/assets/10823037/6a294143-c86d-4424-ba29-9125c6c6df59)



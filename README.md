# Arac.Kiralama
#include <stdio.h>
#include <conio.h>
#include <string.h>
#include <stdlib.h>
#include<Windows.h>

void galeri()
{
    int  gun = 1, tutar = 0;
	int secim2;
	char isim[20];
	int Ford, Renault, Bmw, Audi;
	int secim1;
	int sayi;
	int tarihSecim;

	while (1)
	{
	basadon:
		printf("\nLUTFEN KIRALAMAK ISTEDGINIZ MARKA ARACI SECINIZ :\n1-Ford \n2-Renault\n3-Bmw\n4-Audi\n");
		scanf_s("%d", &secim1);
		system("CLS");
		Sleep(900);

		if (secim1 > 4)
		{
			printf("Hatali secim yaptiniz , lutfen dogru tuslari kodlayiniz.\n\n"); goto basadon;
		}if (secim1 < 1)
		{
			printf("Hatali secim yaptiniz , lutfen dogru tuslari kodlayiniz.\n\n"); goto basadon;
		}
		else {
			goto cikis;
		}
	}
cikis:
	switch (secim1)
	{
	case 1:
	OncekiMenuFordAna:
        system("CLS");
		Sleep(900);
		printf("LUTFEN FORD MODELLERIMIZDEN BIRINI SECINIZ:\n----------------\n1-FORD FOCUS:\tMotor hacmi :1.4\tModel Yili: 2016\tGunluk ucret :600 TL \tRenk :Nardo Gri\t Vites:Manuel\nYakit Turu:Benzin\n------------------ \n");
		printf("\n-----------------\n2-FORD PUMA:\tMotor hacmi: 1.0\tModel Yili: 2021\tGunluk Ucret 450 TL\tRenk:Beyaz\tVites:Manuel\nYakit Turu :Dizel\n----------------\n");
		printf("\n-----------------\n3-FORD RANGER :\tMotor hacmi:2.5 \tModel Yili: 2021\tGunluk Ucret 900 TL\tRenk:Siyah\tVites:Otomatik\nYakit Turu:Benzin\n----------------\n");
		scanf_s("%d", &Ford);
		switch (Ford)
		{
		case 1:
			printf("FORD   FOCUS model arabamizi sectiniz\n\n");
			goto TarihSec;

		TarihSec:
			printf("-------------------------------------------------\n");
		OncekiMenu:
			printf("\nLutfen 2023 yili icin gecerli\n");
			printf("Arac Alis ve Teslim Edis Tarihlerrinden birini seciniz :\n\n\tOcak Ayi\n(1)-01.01.2023\t-- 03.01.2023\n(2)-04.01.2023\t-- 10.01.2023\n(3)-11.01.2023\t--20.01.2023\n\n");
			printf("\tSubat Ayi\n(4)-01.02.2023\t-- 10.02.2023\n(5)-11.02.2023\t-- 20.02.2023\n(6)-21.02.2023\t-- 28.02.2023\n\n");

			printf("Onceki Menuye Donmek icin 10 u tuslayiniz:\n");
			scanf_s("%d", &tarihSecim);


			switch (tarihSecim)
			{
			case 1: printf("teslim alis tarihi = 01.01.2023\t-- teslim edis tarihi = 03.01.2023 Tarihini Sectiniz \n");
				tutar = 3 * 600;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 2: printf("teslim alis tarihi = 04.01.2023\t-- teslim edis tarihi =  10.01.2023 Tarihini Sectiniz \n");
				tutar = 7 * 600;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 3: printf("teslim alis tarihi = 11.01.2023\t-- teslim edis tarihi = 20.01.2023 Tarihini Sectiniz \n");
				tutar = 10 * 600;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 4: printf("teslim alis tarihi = 01.02.2023\t-- teslim edis tarihi = 10.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 600;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 5: printf("teslim alis tarihi = 11.02.2023\t-- teslim edis tarihi =  20.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 600;
				printf("Odencek Tutar =  %d tl", tutar); break;


			case 6: printf("teslim alis tarihi = 21.02.2023\t--  teslim edis tarihi =  28.02.2023 Tarihini Sectiniz \n");
				tutar = 8 * 600;
				printf("Odencek Tutar =  %d tl", tutar); break;
			case 10: goto OncekiMenuFordAna;
			default: printf("\n-------------------------------\nHatali Secim Yaptiniz\n"); goto OncekiMenu;

			}



			printf("\n\n-----------------------------------------------------\n");
		MerkezSec:
			printf("\n\nAraci teslim alacaginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 && secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSec;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimizden alabilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz)\n\n");
		MerkezSec2:
			printf("\nAraci teslim edeceginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSec2;
			}
			else {
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimize teslim edebilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz) \n\n");
				printf("-----------------------------------------------------------------------------------\n");
				printf("Bizi Tercih Ettiginiz icin Tesekkur Ederiz\t Saglikli ve keyifli surusler dileriz.\n");
				printf("-----------------------------------------------------------------------------------");




				printf("-----------------------------------------------------\n");

			}break;
		case 2:
			printf("Ford  Puma model arabamizi sectiniz\n\n");
			printf("-------------------------------------------------\n");
		OncekiMenu1:
			printf("\nLutfen 2023 yili icin gecerli\n");
			printf("Arac Alis ve Teslim Edis Tarihlerrinden birini seciniz :\n\n\tOcak Ayi\n(1)-01.01.2023\t-- 03.01.2023\n(2)-04.01.2023\t-- 10.01.2023\n(3)-11.01.2023\t--20.01.2023\n\n");
			printf("\tSubat Ayi\n(4)-01.02.2023\t-- 10.02.2023\n(5)-11.02.2023\t-- 20.02.2023\n(6)-21.02.2023\t-- 28.02.2023\n\n");

			printf("Onceki Menuye Donmek icin 10 u tuslayiniz:\n");
			scanf_s("%d", &tarihSecim);


			switch (tarihSecim)
			{
			case 1: printf("teslim alis tarihi = 01.01.2023\t-- teslim edis tarihi = 03.01.2023 Tarihini Sectiniz \n");
				tutar = 3 * 450;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 2: printf("teslim alis tarihi = 04.01.2023\t-- teslim edis tarihi =  10.01.2023 Tarihini Sectiniz \n");
				tutar = 7 * 450;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 3: printf("teslim alis tarihi = 11.01.2023\t-- teslim edis tarihi = 20.01.2023 Tarihini Sectiniz \n");
				tutar = 10 * 450;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 4: printf("teslim alis tarihi = 01.02.2023\t-- teslim edis tarihi = 10.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 450;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 5: printf("teslim alis tarihi = 11.02.2023\t-- teslim edis tarihi =  20.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 450;
				printf("Odencek Tutar =  %d tl", tutar); break;


			case 6: printf("teslim alis tarihi = 21.02.2023\t--  teslim edis tarihi =  28.02.2023 Tarihini Sectiniz \n\n");
				tutar = 8 * 450;
				printf("Odencek Tutar =  %d tl", tutar); break;
			case 10: goto OncekiMenuFordAna;
			default: printf("\n-------------------------------\nHatali Secim Yaptiniz\n"); goto OncekiMenu1;

			}
			printf("\n\n-----------------------------------------------------\n");
		MerkezSec1:
			printf("\n\nAraci teslim alacaginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSec1;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimizden alabilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz)\n\n");
		MerkezSec3:
			printf("\nAraci teslim edeceginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSec3;
			}
			else {
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimize teslim edebilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz) \n\n");
				printf("-----------------------------------------------------------------------------------\n");
				printf("Bizi Tercih Ettiginiz icin Tesekkur Ederiz\t Saglikli ve keyifli surusler dileriz.\n");
				printf("-----------------------------------------------------------------------------------");








			}break;
		case 3:
			printf("Ford  Ranger  model arabamizi sectiniz\n");
			printf("-------------------------------------------------\n");
		OncekiMenu3:
			printf("\nLutfen 2023 yili icin gecerli\n");
			printf("Arac Alis ve Teslim Edis Tarihlerrinden birini seciniz :\n\n\tOcak Ayi\n(1)-01.01.2023\t-- 03.01.2023\n(2)-04.01.2023\t-- 10.01.2023\n(3)-11.01.2023\t--20.01.2023\n\n");
			printf("\tSubat Ayi\n(4)-01.02.2023\t-- 10.02.2023\n(5)-11.02.2023\t-- 20.02.2023\n(6)-21.02.2023\t-- 28.02.2023\n\n");

			printf("Onceki Menuye Donmek icin 10 u tuslayiniz:\n");
			scanf_s("%d", &tarihSecim);
		default:printf("hatali tercih yaptiniz lutfen isleminize bastan baslayin."); break;

			switch (tarihSecim)
			{
			case 1: printf("teslim alis tarihi = 01.01.2023\t-- teslim edis tarihi = 03.01.2023 Tarihini Sectiniz \n");
				tutar = 3 * 900;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 2: printf("teslim alis tarihi = 04.01.2023\t-- teslim edis tarihi =  10.01.2023 Tarihini Sectiniz \n");
				tutar = 7 * 900;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 3: printf("teslim alis tarihi = 11.01.2023\t-- teslim edis tarihi = 20.01.2023 Tarihini Sectiniz \n");
				tutar = 10 * 900;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 4: printf("teslim alis tarihi = 01.02.2023\t-- teslim edis tarihi = 10.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 900;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 5: printf("teslim alis tarihi = 11.02.2023\t-- teslim edis tarihi =  20.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 900;
				printf("Odencek Tutar =  %d tl", tutar); break;


			case 6: printf("teslim alis tarihi = 21.02.2023\t--  teslim edis tarihi =  28.02.2023 Tarihini Sectiniz \n");
				tutar = 8 * 900;
				printf("Odencek Tutar =  %d tl", tutar); break;
			case 10: goto OncekiMenuFordAna;
			default: printf("\n-------------------------------\nHatali Secim Yaptiniz\n"); goto OncekiMenu3;

			}
			printf("\n\n-----------------------------------------------------\n");
		MerkezSec4:
			printf("\n\nAraci teslim alacaginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 && secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSec4;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimizden alabilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz)\n\n");
		MerkezSec5:
			printf("\nAraci teslim edeceginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSec5;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimize teslim edebilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz) \n\n");
			printf("-----------------------------------------------------------------------------------\n");
			printf("Bizi Tercih Ettiginiz icin Tesekkur Ederiz\t Saglikli ve keyifli surusler dileriz.\n");
			printf("-----------------------------------------------------------------------------------");










		}break;
	case 2: OncekiMenuRenaultAna:
		printf("LUTFEN RENAULT MODELLERIMIZDEN BIRINI SECINIZ:\n----------------\n1-RENAULT CLIO:\tMotor hacmi :1461 CC\tModel Yili: 2019\tGunluk ucret :470 TL \tRenk :Gri\t Vites:Manuel\nYakit Turu:Dizel\n------------------ \n");
		printf("\n-----------------\n2-RENAULT MEGANE:\tMotor hacmi: 1461 CC\tModel Yili: 2018\tGunluk Ucret: 430 TL\tRenk:Beyaz\tVites:Otomatik\nYakit Turu :Dizel\n----------------\n");
		printf("\n-----------------\n3-RENAULT SYMBOL :\tMotor hacmi:1461 CC \tModel yili: 2016\tGunluk Ucret :500 TL\tRenk:Siyah\tVites:Otomatik\nYakit Turu:Benzin\n----------------\n");
		scanf_s("%d", &Renault);
		switch (Renault)
		{
		case 1:
			printf("RENAULT CLIO model arabamizi sectiniz\n\n");

		OncekiMenuClio:
			printf("\nLutfen 2023 yili icin gecerli\n");
			printf("Arac Alis ve Teslim Edis Tarihlerrinden birini seciniz :\n\n\tOcak Ayi\n(1)-01.01.2023\t-- 03.01.2023\n(2)-04.01.2023\t-- 10.01.2023\n(3)-11.01.2023\t--20.01.2023\n\n");
			printf("\tSubat Ayi\n(4)-01.02.2023\t-- 10.02.2023\n(5)-11.02.2023\t-- 20.02.2023\n(6)-21.02.2023\t-- 28.02.2023\n\n");

			printf("Onceki Menuye Donmek icin 10 u tuslayiniz:\n");
			scanf_s("%d", &tarihSecim);


			switch (tarihSecim)
			{
			case 1: printf("teslim alis tarihi = 01.01.2023\t-- teslim edis tarihi = 03.01.2023 Tarihini Sectiniz \n");
				tutar = 3 * 470;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 2: printf("teslim alis tarihi = 04.01.2023\t-- teslim edis tarihi =  10.01.2023 Tarihini Sectiniz \n");
				tutar = 7 * 470;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 3: printf("teslim alis tarihi = 11.01.2023\t-- teslim edis tarihi = 20.01.2023 Tarihini Sectiniz \n");
				tutar = 10 * 470;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 4: printf("teslim alis tarihi = 01.02.2023\t-- teslim edis tarihi = 10.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 470;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 5: printf("teslim alis tarihi = 11.02.2023\t-- teslim edis tarihi =  20.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 470;
				printf("Odencek Tutar =  %d tl", tutar); break;


			case 6: printf("teslim alis tarihi = 21.02.2023\t--  teslim edis tarihi =  28.02.2023 Tarihini Sectiniz \n");
				tutar = 8 * 470;
				printf("Odencek Tutar =  %d tl", tutar); break;
			case 10: goto OncekiMenuRenaultAna;
			default: printf("\n-------------------------------\nHatali Secim Yaptiniz\n"); goto OncekiMenuClio;

			}
			printf("\n\n-----------------------------------------------------\n");
		MerkezSecClio:
			printf("\n\nAraci teslim alacaginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSecClio;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimizden alabilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz)\n\n");

			printf("\nAraci teslim edeceginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSecClio;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimize teslim edebilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz) \n\n");
			printf("-----------------------------------------------------------------------------------\n");
			printf("Bizi Tercih Ettiginiz icin Tesekkur Ederiz\t Saglikli ve keyifli surusler dileriz.\n");
			printf("-----------------------------------------------------------------------------------");




			break;


		case 2:
			printf("RENAULT MEGANE model arabamizi sectiniz\n\n");

		OncekiMenuMegane:
			printf("\nLutfen 2023 yili icin gecerli\n");
			printf("Arac Alis ve Teslim Edis Tarihlerrinden birini seciniz :\n\n\tOcak Ayi\n(1)-01.01.2023\t-- 03.01.2023\n(2)-04.01.2023\t-- 10.01.2023\n(3)-11.01.2023\t--20.01.2023\n\n");
			printf("\tSubat Ayi\n(4)-01.02.2023\t-- 10.02.2023\n(5)-11.02.2023\t-- 20.02.2023\n(6)-21.02.2023\t-- 28.02.2023\n\n");

			printf("Onceki Menuye Donmek icin 10 u tuslayiniz:\n");
			scanf_s("%d", &tarihSecim);


			switch (tarihSecim)
			{
			case 1: printf("teslim alis tarihi = 01.01.2023\t-- teslim edis tarihi = 03.01.2023 Tarihini Sectiniz \n");
				tutar = 3 * 430;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 2: printf("teslim alis tarihi = 04.01.2023\t-- teslim edis tarihi =  10.01.2023 Tarihini Sectiniz \n");
				tutar = 7 * 430;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 3: printf("teslim alis tarihi = 11.01.2023\t-- teslim edis tarihi = 20.01.2023 Tarihini Sectiniz \n");
				tutar = 10 * 430;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 4: printf("teslim alis tarihi = 01.02.2023\t-- teslim edis tarihi = 10.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 430;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 5: printf("teslim alis tarihi = 11.02.2023\t-- teslim edis tarihi =  20.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 430;
				printf("Odencek Tutar =  %d tl", tutar); break;


			case 6: printf("teslim alis tarihi = 21.02.2023\t--  teslim edis tarihi =  28.02.2023 Tarihini Sectiniz \n");
				tutar = 8 * 430;
				printf("Odencek Tutar =  %d tl", tutar); break;
			case 10: goto OncekiMenuRenaultAna;
			default: printf("\n-------------------------------\nHatali Secim Yaptiniz\n"); goto OncekiMenuMegane;

			}
			printf("\n\n-----------------------------------------------------\n");
		MerkezSecMegane:
			printf("\n\nAraci teslim alacaginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSecMegane;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimizden alabilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz)\n\n");

			printf("\nAraci teslim edeceginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSecMegane;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimize teslim edebilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz) \n\n");
			printf("-----------------------------------------------------------------------------------\n");
			printf("Bizi Tercih Ettiginiz icin Tesekkur Ederiz\t Saglikli ve keyifli surusler dileriz.\n");
			printf("-----------------------------------------------------------------------------------");




			break;
		case 3:
			printf("RENAULT SYMBOL model arabamizi sectiniz\n\n");
		OncekiMenuSymbol:
			printf("\nLutfen 2023 yili icin gecerli\n");
			printf("Arac Alis ve Teslim Edis Tarihlerrinden birini seciniz :\n\n\tOcak Ayi\n(1)-01.01.2023\t-- 03.01.2023\n(2)-04.01.2023\t-- 10.01.2023\n(3)-11.01.2023\t--20.01.2023\n\n");
			printf("\tSubat Ayi\n(4)-01.02.2023\t-- 10.02.2023\n(5)-11.02.2023\t-- 20.02.2023\n(6)-21.02.2023\t-- 28.02.2023\n\n");

			printf("Onceki Menuye Donmek icin 10 u tuslayiniz:\n");
			scanf_s("%d", &tarihSecim);


			switch (tarihSecim)
			{
			case 1: printf("teslim alis tarihi = 01.01.2023\t-- teslim edis tarihi = 03.01.2023 Tarihini Sectiniz \n");
				tutar = 3 * 500;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 2: printf("teslim alis tarihi = 04.01.2023\t-- teslim edis tarihi =  10.01.2023 Tarihini Sectiniz \n");
				tutar = 7 * 500;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 3: printf("teslim alis tarihi = 11.01.2023\t-- teslim edis tarihi = 20.01.2023 Tarihini Sectiniz \n");
				tutar = 10 * 500;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 4: printf("teslim alis tarihi = 01.02.2023\t-- teslim edis tarihi = 10.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 500;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 5: printf("teslim alis tarihi = 11.02.2023\t-- teslim edis tarihi =  20.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 500;
				printf("Odencek Tutar =  %d tl", tutar); break;


			case 6: printf("teslim alis tarihi = 21.02.2023\t--  teslim edis tarihi =  28.02.2023 Tarihini Sectiniz \n");
				tutar = 8 * 500;
				printf("Odencek Tutar =  %d tl", tutar); break;
			case 10: goto OncekiMenuRenaultAna;
			default: printf("\n-------------------------------\nHatali Secim Yaptiniz\n"); goto OncekiMenuSymbol;

			}
			printf("\n\n-----------------------------------------------------\n");
		MerkezSecSymbol:
			printf("\n\nAraci teslim alacaginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSecSymbol;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimizden alabilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz)\n\n");

			printf("\nAraci teslim edeceginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSecSymbol;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimize teslim edebilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz) \n\n");
			printf("-----------------------------------------------------------------------------------\n");
			printf("Bizi Tercih Ettiginiz icin Tesekkur Ederiz\t Saglikli ve keyifli surusler dileriz.\n");
			printf("-----------------------------------------------------------------------------------");




			break;
		default:
			printf("Lutfen mevcut araclarimizi seciniz.\n"); break;


		}break;
	case 3:OncekiMenuBmwAna:
		printf("LUTFEN BMW MODELLERIMIZDEN BIRINI SECINIZ:\n----------------\n1-BMW 2.18 CABRIO:\tMotor hacmi :1401-1600 CM(Kup)\tModel Yili:2022\tGunluk ucret :1650 TL \tRenk :Kirmizi\n Vites:Otomatik\nYakit Turu:Dizel\n------------------ \n");
		printf("\n-----------------\n2-BMW 216d  GRAN:\tMotor hacmi:1401 - 1600 CM(KUP)\tModel Yili: 2021\tGunluk Ucret 1700 TL\tRenk:Siyah\nVites:Otomatik\nYakit Turu :Dizel\n----------------\n");
		printf("\n-----------------\n3-Bmw 3.16 M SPORT :\tMotor hacmi:1401-1600 CM(KUP) \tModel Yili: 2012\tGunluk Ucret:800 TL\tRenk:Mavi\nVites:Otomatik\nYakit Turu:Benzin\n----------------\n");
		scanf_s("%d", &Bmw);

		switch (Bmw)
		{
		case 1:
			printf("BMW 2.18 CABRIO model arabamizi sectiniz\n\n");

		OncekiMenuBmw2:
			printf("\nLutfen 2023 yili icin gecerli\n");
			printf("Arac Alis ve Teslim Edis Tarihlerrinden birini seciniz :\n\n\tOcak Ayi\n(1)-01.01.2023\t-- 03.01.2023\n(2)-04.01.2023\t-- 10.01.2023\n(3)-11.01.2023\t--20.01.2023\n\n");
			printf("\tSubat Ayi\n(4)-01.02.2023\t-- 10.02.2023\n(5)-11.02.2023\t-- 20.02.2023\n(6)-21.02.2023\t-- 28.02.2023\n\n");

			printf("Onceki Menuye Donmek icin 10 u tuslayiniz:\n");
			scanf_s("%d", &tarihSecim);


			switch (tarihSecim)
			{
			case 1: printf("teslim alis tarihi = 01.01.2023\t-- teslim edis tarihi = 03.01.2023 Tarihini Sectiniz \n");
				tutar = 3 * 1650;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 2: printf("teslim alis tarihi = 04.01.2023\t-- teslim edis tarihi =  10.01.2023 Tarihini Sectiniz \n");
				tutar = 7 * 1650;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 3: printf("teslim alis tarihi = 11.01.2023\t-- teslim edis tarihi = 20.01.2023 Tarihini Sectiniz \n");
				tutar = 10 * 1650;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 4: printf("teslim alis tarihi = 01.02.2023\t-- teslim edis tarihi = 10.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 1650;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 5: printf("teslim alis tarihi = 11.02.2023\t-- teslim edis tarihi =  20.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 1650;
				printf("Odencek Tutar =  %d tl", tutar); break;


			case 6: printf("teslim alis tarihi = 21.02.2023\t--  teslim edis tarihi =  28.02.2023 Tarihini Sectiniz \n");
				tutar = 8 * 1650;
				printf("Odencek Tutar =  %d tl", tutar); break;
			case 10: goto OncekiMenuBmwAna;
			default: printf("\n-------------------------------\nHatali Secim Yaptiniz\n"); goto OncekiMenuBmw2;

			}
			printf("\n\n-----------------------------------------------------\n");
		MerkezSecBmw2:
			printf("\n\nAraci teslim alacaginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSecBmw2;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimizden alabilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz)\n\n");

			printf("\nAraci teslim edeceginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSecBmw2;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimize teslim edebilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz) \n\n");
			printf("-----------------------------------------------------------------------------------\n");
			printf("Bizi Tercih Ettiginiz icin Tesekkur Ederiz\t Saglikli ve keyifli surusler dileriz.\n\n");
			printf("-----------------------------------------------------------------------------------\n");




			break;
		case 2:
			printf("BMW 216d GRAN model arabamizi sectiniz\n\n");
		OncekiMenuBmw216:
			printf("\nLutfen 2023 yili icin gecerli\n");
			printf("Arac Alis ve Teslim Edis Tarihlerrinden birini seciniz :\n\n\tOcak Ayi\n(1)-01.01.2023\t-- 03.01.2023\n(2)-04.01.2023\t-- 10.01.2023\n(3)-11.01.2023\t--20.01.2023\n\n");
			printf("\tSubat Ayi\n(4)-01.02.2023\t-- 10.02.2023\n(5)-11.02.2023\t-- 20.02.2023\n(6)-21.02.2023\t-- 28.02.2023\n\n");

			printf("Onceki Menuye Donmek icin 10 u tuslayiniz:\n");
			scanf_s("%d", &tarihSecim);


			switch (tarihSecim)
			{
			case 1: printf("teslim alis tarihi = 01.01.2023\t-- teslim edis tarihi = 03.01.2023 Tarihini Sectiniz \n");
				tutar = 3 * 1700;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 2: printf("teslim alis tarihi = 04.01.2023\t-- teslim edis tarihi =  10.01.2023 Tarihini Sectiniz \n");
				tutar = 7 * 1700;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 3: printf("teslim alis tarihi = 11.01.2023\t-- teslim edis tarihi = 20.01.2023 Tarihini Sectiniz \n");
				tutar = 10 * 1700;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 4: printf("teslim alis tarihi = 01.02.2023\t-- teslim edis tarihi = 10.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 1700;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 5: printf("teslim alis tarihi = 11.02.2023\t-- teslim edis tarihi =  20.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 1700;
				printf("Odencek Tutar =  %d tl", tutar); break;


			case 6: printf("teslim alis tarihi = 21.02.2023\t--  teslim edis tarihi =  28.02.2023 Tarihini Sectiniz \n");
				tutar = 8 * 1700;
				printf("Odencek Tutar =  %d tl", tutar); break;
			case 10: goto OncekiMenuBmwAna;
			default: printf("\n-------------------------------\nHatali Secim Yaptiniz\n"); goto OncekiMenuBmw216;

			}
			printf("\n\n-----------------------------------------------------\n");
		MerkezSecBmw216:
			printf("\n\nAraci teslim alacaginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSecBmw216;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimizden alabilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz)\n\n");

			printf("\nAraci teslim edeceginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSecBmw216;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimize teslim edebilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz) \n\n");
			printf("-----------------------------------------------------------------------------------\n");
			printf("Bizi Tercih Ettiginiz icin Tesekkur Ederiz\t Saglikli ve keyifli surusler dileriz.\n");
			printf("-----------------------------------------------------------------------------------\n");




			break;
		case 3:
			printf("BMW 3.16 M SPORT model arabamizi sectiniz\n\n");

		OncekiMenuBmw316:
			printf("\nLutfen 2023 yili icin gecerli\n");
			printf("Arac Alis ve Teslim Edis Tarihlerrinden birini seciniz :\n\n\tOcak Ayi\n(1)-01.01.2023\t-- 03.01.2023\n(2)-04.01.2023\t-- 10.01.2023\n(3)-11.01.2023\t--20.01.2023\n\n");
			printf("\tSubat Ayi\n(4)-01.02.2023\t-- 10.02.2023\n(5)-11.02.2023\t-- 20.02.2023\n(6)-21.02.2023\t-- 28.02.2023\n\n");

			printf("Onceki Menuye Donmek icin 10 u tuslayiniz:\n");
			scanf_s("%d", &tarihSecim);


			switch (tarihSecim)
			{
			case 1: printf("teslim alis tarihi = 01.01.2023\t-- teslim edis tarihi = 03.01.2023 Tarihini Sectiniz \n");
				tutar = 3 * 800;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 2: printf("teslim alis tarihi = 04.01.2023\t-- teslim edis tarihi =  10.01.2023 Tarihini Sectiniz \n");
				tutar = 7 * 800;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 3: printf("teslim alis tarihi = 11.01.2023\t-- teslim edis tarihi = 20.01.2023 Tarihini Sectiniz \n");
				tutar = 10 * 800;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 4: printf("teslim alis tarihi = 01.02.2023\t-- teslim edis tarihi = 10.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 800;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 5: printf("teslim alis tarihi = 11.02.2023\t-- teslim edis tarihi =  20.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 800;
				printf("Odencek Tutar =  %d tl", tutar); break;


			case 6: printf("teslim alis tarihi = 21.02.2023\t--  teslim edis tarihi =  28.02.2023 Tarihini Sectiniz \n");
				tutar = 8 * 800;
				printf("Odencek Tutar =  %d tl", tutar); break;
			case 10: goto OncekiMenuBmwAna;
			default: printf("\n-------------------------------\nHatali Secim Yaptiniz\n"); goto OncekiMenuBmw316;

			}
			printf("\n\n-----------------------------------------------------\n");
		MerkezSecBmw316:
			printf("\n\nAraci teslim alacaginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSecBmw316;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimizden alabilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz)\n\n");

			printf("\nAraci teslim edeceginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSecBmw316;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimize teslim edebilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz) \n\n");
			printf("-----------------------------------------------------------------------------------\n");
			printf("Bizi Tercih Ettiginiz icin Tesekkur Ederiz\t Saglikli ve keyifli surusler dileriz.\n");
			printf("-----------------------------------------------------------------------------------\n");

		default:printf("hatali tercih yaptiniz lutfen isleminize bastan baslayin."); break;

		}break;
	case 4:OncekiMenuAna:

		printf("LUTFEN Audi MODELLERIMIZDEN BIRINI SECINIZ:\n----------------\n1-AUDI A3 SEDAN\tMotor hacmi :1601-1800 CM(Kup)\tModel Yili:2015\tGunluk ucret :750 TL \tRenk :Yesil\n Vites:Otomatik\nYakit Turu:Dizel\n------------------ \n");
		printf("\n-----------------\n2-AUDI Q7 S-LINE  GRAN:\tMotor hacmi:3501 - 4000 CM(KUP)\tModel Yili: 2014\tGunluk Ucret 1250 TL\tRenk:Siyah\nVites:Otomatik\nYakit Turu :Dizel\n----------------\n");
		printf("\n-----------------\n3-AUDI A6 2.0 TDI QUATTRO:\tMotor hacmi:1801-2000 CM(KUP) \tModel Yili: 2021\tGunluk Ucret:3750 TL\tRenk:Siyah\nVites:Otomatik\nYakit Turu:Dizel\n----------------\n");
		scanf_s("%d", &Audi);

		switch (Audi)
		{
		case 1:OncekiMenuA3:
		printf("AUDI A3 SEDAN model arabamizi sectiniz\n\n");


		printf("\nLutfen 2023 yili icin gecerli\n");
		printf("Arac Alis ve Teslim Edis Tarihlerrinden birini seciniz :\n\n\tOcak Ayi\n(1)-01.01.2023\t-- 03.01.2023\n(2)-04.01.2023\t-- 10.01.2023\n(3)-11.01.2023\t--20.01.2023\n\n");
		printf("\tSubat Ayi\n(4)-01.02.2023\t-- 10.02.2023\n(5)-11.02.2023\t-- 20.02.2023\n(6)-21.02.2023\t-- 28.02.2023\n\n");

		printf("Onceki Menuye Donmek icin 10 u tuslayiniz:\n");
		scanf_s("%d", &tarihSecim);


		switch (tarihSecim)
		{
		case 1: printf("teslim alis tarihi = 01.01.2023\t-- teslim edis tarihi = 03.01.2023 Tarihini Sectiniz \n");
			tutar = 3 * 750;
			printf("Odencek Tutar =  %d tl", tutar); break;

		case 2: printf("teslim alis tarihi = 04.01.2023\t-- teslim edis tarihi =  10.01.2023 Tarihini Sectiniz \n");
			tutar = 7 * 750;
			printf("Odencek Tutar =  %d tl", tutar); break;

		case 3: printf("teslim alis tarihi = 11.01.2023\t-- teslim edis tarihi = 20.01.2023 Tarihini Sectiniz \n");
			tutar = 10 * 750;
			printf("Odencek Tutar =  %d tl", tutar); break;

		case 4: printf("teslim alis tarihi = 01.02.2023\t-- teslim edis tarihi = 10.02.2023 Tarihini Sectiniz \n");
			tutar = 10 * 750;
			printf("Odencek Tutar =  %d tl", tutar); break;

		case 5: printf("teslim alis tarihi = 11.02.2023\t-- teslim edis tarihi =  20.02.2023 Tarihini Sectiniz \n");
			tutar = 10 * 750;
			printf("Odencek Tutar =  %d tl", tutar); break;


		case 6: printf("teslim alis tarihi = 21.02.2023\t--  teslim edis tarihi =  28.02.2023 Tarihini Sectiniz \n");
			tutar = 8 * 750;
			printf("Odencek Tutar =  %d tl", tutar); break;
		case 10: goto 	OncekiMenuA3;
		default: printf("\n-------------------------------\nHatali Secim Yaptiniz\n"); goto 	OncekiMenuA3;

		}
		printf("\n\n-----------------------------------------------------\n");
	MerkezSecA3:
		printf("\n\nAraci teslim alacaginiz ofisimizi seciniz lutfen\n\n");
		printf("  1-----ADANA HAVALIMANI\n");
		printf("  2-----ANKARA MERKEZ\n");
		printf("  3-----ANTALYA MERKEZ\n");
		printf("  4-----BODRUM MERKEZ\n ");
		printf("  5-----DENIZLI PAMUKKALE\n");
		scanf_s("%d", &secim2);
		if (secim2 < 1 || secim2>5)
		{
			printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSecA3;
		}
		else
			printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimizden alabilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz)\n\n");

		printf("\nAraci teslim edeceginiz ofisimizi seciniz lutfen\n\n");
		printf("  1-----ADANA HAVALIMANI\n");
		printf("  2-----ANKARA MERKEZ\n");
		printf("  3-----ANTALYA MERKEZ\n");
		printf("  4-----BODRUM MERKEZ\n ");
		printf("  5-----DENIZLI PAMUKKALE\n");
		scanf_s("%d", &secim2);
		if (secim2 < 1 || secim2>5)
		{
			printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto MerkezSecA3;
		}
		else
			printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimize teslim edebilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz) \n\n");
		printf("-----------------------------------------------------------------------------------\n");
		printf("Bizi Tercih Ettiginiz icin Tesekkur Ederiz\t Saglikli ve keyifli surusler dileriz.\n");
		printf("-----------------------------------------------------------------------------------\n");


		break;
		case 2:
		OncekiMenuQ7:
			printf("AUDI Q7 S-LINE model arabamizi sectiniz\n\n");

			printf("\nLutfen 2023 yili icin gecerli\n");
			printf("Arac Alis ve Teslim Edis Tarihlerrinden birini seciniz :\n\n\tOcak Ayi\n(1)-01.01.2023\t-- 03.01.2023\n(2)-04.01.2023\t-- 10.01.2023\n(3)-11.01.2023\t--20.01.2023\n\n");
			printf("\tSubat Ayi\n(4)-01.02.2023\t-- 10.02.2023\n(5)-11.02.2023\t-- 20.02.2023\n(6)-21.02.2023\t-- 28.02.2023\n\n");

			printf("Onceki Menuye Donmek icin 10 u tuslayiniz:\n");
			scanf_s("%d", &tarihSecim);


			switch (tarihSecim)
			{
			case 1: printf("teslim alis tarihi = 01.01.2023\t-- teslim edis tarihi = 03.01.2023 Tarihini Sectiniz \n");
				tutar = 3 * 1250;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 2: printf("teslim alis tarihi = 04.01.2023\t-- teslim edis tarihi =  10.01.2023 Tarihini Sectiniz \n");
				tutar = 7 * 1250;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 3: printf("teslim alis tarihi = 11.01.2023\t-- teslim edis tarihi = 20.01.2023 Tarihini Sectiniz \n");
				tutar = 10 * 1250;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 4: printf("teslim alis tarihi = 01.02.2023\t-- teslim edis tarihi = 10.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 1250;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 5: printf("teslim alis tarihi = 11.02.2023\t-- teslim edis tarihi =  20.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 1250;
				printf("Odencek Tutar =  %d tl", tutar); break;


			case 6: printf("teslim alis tarihi = 21.02.2023\t--  teslim edis tarihi =  28.02.2023 Tarihini Sectiniz \n");
				tutar = 8 * 1250;
				printf("Odencek Tutar =  %d tl", tutar); break;
			case 10: goto 		OncekiMenuAna;
			default: printf("\n-------------------------------\nHatali Secim Yaptiniz\n"); goto 	OncekiMenuQ7;

			}
			printf("\n\n-----------------------------------------------------\n");
		MerkezSecQ7:
			printf("\n\nAraci teslim alacaginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto 	MerkezSecQ7;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimizden alabilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz)\n\n");

			printf("\nAraci teslim edeceginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto 	MerkezSecQ7;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimize teslim edebilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz) \n\n");
			printf("-----------------------------------------------------------------------------------\n");
			printf("Bizi Tercih Ettiginiz icin Tesekkur Ederiz\t Saglikli ve keyifli surusler dileriz.\n");
			printf("-----------------------------------------------------------------------------------\n");


			break;
		case 3:
		OncekiMenuA6:
			printf("AUDI A6 2.0 TDI QUATTRO model arabamizi sectiniz\n\n");

			printf("\nLutfen 2023 yili icin gecerli\n");
			printf("Arac Alis ve Teslim Edis Tarihlerrinden birini seciniz :\n\n\tOcak Ayi\n(1)-01.01.2023\t-- 03.01.2023\n(2)-04.01.2023\t-- 10.01.2023\n(3)-11.01.2023\t--20.01.2023\n\n");
			printf("\tSubat Ayi\n(4)-01.02.2023\t-- 10.02.2023\n(5)-11.02.2023\t-- 20.02.2023\n(6)-21.02.2023\t-- 28.02.2023\n\n");

			printf("Onceki Menuye Donmek icin 10 u tuslayiniz:\n");
			scanf_s("%d", &tarihSecim);


			switch (tarihSecim)
			{
			case 1: printf("teslim alis tarihi = 01.01.2023\t-- teslim edis tarihi = 03.01.2023 Tarihini Sectiniz \n");
				tutar = 3 * 450;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 2: printf("teslim alis tarihi = 04.01.2023\t-- teslim edis tarihi =  10.01.2023 Tarihini Sectiniz \n");
				tutar = 7 * 3750;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 3: printf("teslim alis tarihi = 11.01.2023\t-- teslim edis tarihi = 20.01.2023 Tarihini Sectiniz \n");
				tutar = 10 * 3750;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 4: printf("teslim alis tarihi = 01.02.2023\t-- teslim edis tarihi = 10.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 3750;
				printf("Odencek Tutar =  %d tl", tutar); break;

			case 5: printf("teslim alis tarihi = 11.02.2023\t-- teslim edis tarihi =  20.02.2023 Tarihini Sectiniz \n");
				tutar = 10 * 3750;
				printf("Odencek Tutar =  %d tl", tutar); break;


			case 6: printf("teslim alis tarihi = 21.02.2023\t--  teslim edis tarihi =  28.02.2023 Tarihini Sectiniz \n");
				tutar = 8 * 3750;
				printf("Odencek Tutar =  %d tl", tutar); break;
			case 10: goto 	OncekiMenuAna;
			default: printf("\n-------------------------------\nHatali Secim Yaptiniz\n"); goto 	OncekiMenuA6;

			}
			printf("\n\n-----------------------------------------------------\n");
		MerkezSecA6:
			printf("\n\nAraci teslim alacaginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto 	MerkezSecA6;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimizden alabilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz)\n\n");

			printf("\nAraci teslim edeceginiz ofisimizi seciniz lutfen\n\n");
			printf("  1-----ADANA HAVALIMANI\n");
			printf("  2-----ANKARA MERKEZ\n");
			printf("  3-----ANTALYA MERKEZ\n");
			printf("  4-----BODRUM MERKEZ\n ");
			printf("  5-----DENIZLI PAMUKKALE\n");
			scanf_s("%d", &secim2);
			if (secim2 < 1 || secim2>5)
			{
				printf("hatali tercih yaptiniz , lutfen tekrar deneyin.\n"); goto 	MerkezSecA6;
			}
			else
				printf("Aracimizi sectiginiz tarihte ve sectiginiz ofimize teslim edebilirsiniz\n(Odemeyi Sectiginiz Ofiste Gerceklestireceksiniz) \n\n");
			printf("-----------------------------------------------------------------------------------\n");
			printf("Bizi Tercih Ettiginiz icin Tesekkur Ederiz\t Saglikli ve keyifli surusler dileriz.\n");
			printf("-----------------------------------------------------------------------------------\n");


			break;

		default:printf("lUTFEN Listede mevcut olan araclari seciniz"); break;
		}
		break;
	default:
		printf("Lutfen listede mevcut olan araclarimizdan seciniz.\n"); break;



	}


	printf("Sona geldiniz ");


}


void galerigiris()
{
	int yas;
    int  gun = 1, tutar = 0;
	int secim2;
	char isim[20];
	int Ford, Renault, Bmw, Audi;
	int secim1;
	int sayi;
	int tarihSecim;

    printf("\n --------------------------------------\n");
	printf("   ARAC KIRALAMA OTOMASYONUMUZA HOSGELDINIZ\n --------------------------------------\n");
    printf("Lutfen Adinizi giriniz :\n");
    scanf_s("%s",&isim);
	printf("Yasinizi giriniz\n "); scanf_s("%d", &yas);
	while (yas)
	{
		if (yas<18)
		{
			printf("yasiniz kucuk");
			programkapat();
			break;

		}
		else
		{
			printf("\n      HOSGELDINIZ\t%s  Arac secim ekranina yonlendiriliyorsunuz....", isim);
			Sleep(2000);
			system("CLS");
			galeri();
			break;
		}
	}




}




void programkapat()
{
    system("CLS");
    printf(" Guvenli Cikis Ekrani");
	printf("\n -----");
	printf("\n\n ILAY Otomobil Kiralama Uygulamasi Cikis Yaptiniz.");
	printf("\n ILAY Otomobil Kiralama Uygulamasini Kullandiginiz Icin Tesekkur Ederiz.");
	Sleep(2000);
	system("CLS");
	printf("\n Programi Kapatmak Icin Bir Tusa Basiniz.");
	_getch();
}

  void main()
{

    char islemsec;
    printf("*____________________________________________________*\n");
    printf("*                                                    *\n");
    printf("*      <\4> ILAY Otomobil Kiralama Uygulamasi <\4>        *\n");
    printf("*                                                    *\n");
    printf("*____________________________________________________*\n");
    printf("*\n\tLutfen Yapacaginiz Islemi Seciniz:           *\n");
    printf("*\n\t1-Arac Kiralama                              *\n");
    printf("*\n\t0-Cikis                                      *\n");
    printf("*____________________________________________________*\n");
    scanf("%c", &islemsec);
    switch(islemsec)
    {
    case '1':
        galerigiris() ;
        break;
    case '0':
        programkapat();
        break;
    default:
        system("Cls");
        main();
        break;
    }

    _getch();
}

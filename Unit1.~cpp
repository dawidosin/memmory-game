//---------------------------------------------------------------------------

#include <vcl.h>
#pragma hdrstop
#include <string.h>
#include <iostream>

#include "Unit1.h"
//---------------------------------------------------------------------------
#pragma package(smart_init)
#pragma resource "*.dfm"
TForm1 *Form1;
TImage *i[10],*iu[10],*t_i[2],*t_iu[2],*img;

        // black:1; blue:2; green:3; red:4; yellow:5;

 int c1=10,c2=10,c3=10,c4=10,c5=10;
 int p;//random number var
 int temp;// var who stores number of showed cards
 int color[10];
 int k1,k2;
 int l_prob;
 int muzyka;
 bool restart;
 void wygrana();
 void poczatek();

void check()
{
l_prob++;wygrana();

if(restart==true)
{
muzyka= random(2)+1;
 switch(muzyka)
 {
 case 1:sndPlaySound("snd/cnice.wav",SND_ASYNC);break;
 case 2:sndPlaySound("snd/dobre.wav",SND_ASYNC);
 }

 if(Application->MessageBox("Wygrana! Czy chcesz zagraæ ponownie? ","Wygra³eœ!!!",MB_YESNO|MB_ICONQUESTION)==ID_YES)
 {poczatek();restart=false;}

 else{Application->Terminate();}
 }

for(int a=0;a<=9;a++){iu[a]->Enabled=false;}

 if(color[k1]==color[k2])
 {
  for(int a=0;a<=9;a++){iu[a]->Enabled=true;}
  t_iu[0]->Enabled=false;t_iu[1]->Enabled=false;
  Form1->liczbaposuniec->Caption="Liczba posuniêæ: "+IntToStr(l_prob);
  for(int i=0;i<=1;i++){continue;}
 }
 else
 {
 Application->ProcessMessages();Sleep(1000);
 t_iu[0]->Enabled=true;t_iu[0]->Visible=true;
 t_iu[1]->Enabled=true;t_iu[1]->Visible=true;
 for(int a=0;a<=9;a++){iu[a]->Enabled=true;}
 Form1->liczbaposuniec->Caption="Liczba posuniêæ: "+IntToStr(l_prob);
 }
 }

void licznik()
{
   do
   {
   p=random(5)+1;
   }while((p==c1)||(p==c2)||(p==c3)||(p==c4)||(p==c5));

         switch (p)
        {
        case 1: if(c1==11){c1=1;}else{c1++;};break;
        case 2: if(c2==11){c2=2;}else{c2++;};break;
        case 3: if(c3==11){c3=3;}else{c3++;};break;
        case 4: if(c4==11){c4=4;}else{c4++;};break;
        case 5: if(c5==11){c5=5;}else{c5++;};break;
        }
}
void wygrana()
{
if((iu[0]->Visible==false)&&
(iu[1]->Visible==false)&&
(iu[2]->Visible==false)&&
(iu[3]->Visible==false)&&
(iu[4]->Visible==false)&&
(iu[5]->Visible==false)&&
(iu[6]->Visible==false)&&
(iu[7]->Visible==false)&&
(iu[8]->Visible==false)&&
(iu[9]->Visible==false))
{restart=true;}

}
 void poczatek()
 {
 randomize();
   //Przypisanie kolorów do zdjêc:
   c1=10,c2=10,c3=10,c4=10,c5=10,l_prob=0,temp=0,k2=0;
     for(int a=0;a<=9;a++)
     {
     licznik();
     img = i[a];
     img->Picture->LoadFromFile("img/color"+IntToStr(p)+".bmp");
     color[a]=p;
     }

      for(int a=0;a<=9;a++){iu[a]->Enabled=true;}
      for(int a=0;a<=9;a++){iu[a]->Visible=true;}
 }

//---------------------------------------------------------------------------
__fastcall TForm1::TForm1(TComponent* Owner)
        : TForm(Owner)
{
}
//---------------------------------------------------------------------------
void __fastcall TForm1::FormCreate(TObject *Sender)
{
randomize();
i[0]=i1;i[1]=i2;i[2]=i3;i[3]=i4;i[4]=i5;i[5]=i6;i[6]=i7;i[7]=i8;i[8]=i9;i[9]=i10;
iu[0]=i1u;iu[1]=i2u;iu[2]=i3u;iu[3]=i4u;iu[4]=i5u;iu[5]=i6u;iu[6]=i7u;iu[7]=i8u;iu[8]=i9u;iu[9]=i10u;


    poczatek();
}
//---------------------------------------------------------------------------



void __fastcall TForm1::i10uClick(TObject *Sender)
{
sndPlaySound("snd/dzwiek.wav",SND_ASYNC);

  if(temp==0){t_i[0]=i[9];t_iu[0]=iu[9];k1=9;}

        if(temp==1)
        {
        iu[9]->Visible=false;
        iu[9]->Enabled=false;
        k2=9;
        t_i[1]=i[9];t_iu[1]=iu[9];
        check();
        temp=0;
        }
 else
 {
 iu[9]->Visible=false;
 iu[9]->Enabled=false;
 temp++;
 }

}
//---------------------------------------------------------------------------

void __fastcall TForm1::i9uClick(TObject *Sender)
{
sndPlaySound("snd/dzwiek.wav",SND_ASYNC);
  if(temp==0){t_i[0]=i[8];t_iu[0]=iu[8];k1=8;}

        if(temp==1)
        {
        iu[8]->Visible=false;
        iu[8]->Enabled=false;
        k2=8;
        t_i[1]=i[8];t_iu[1]=iu[8];
        check();
        temp=0;
        }
 else
 {
 iu[8]->Visible=false;
 iu[8]->Enabled=false;
 temp++;
 }
}
//---------------------------------------------------------------------------

void __fastcall TForm1::i8uClick(TObject *Sender)
{
sndPlaySound("snd/dzwiek.wav",SND_ASYNC);
  if(temp==0){t_i[0]=i[7];t_iu[0]=iu[7];k1=7;}

        if(temp==1)
        {
        iu[7]->Visible=false;
        iu[7]->Enabled=false;
        k2=7;
        t_i[1]=i[7];t_iu[1]=iu[7];
        check();
        temp=0;
        }
 else
 {
 iu[7]->Visible=false;
 iu[7]->Enabled=false;
 temp++;
 }
}
//---------------------------------------------------------------------------

void __fastcall TForm1::i7uClick(TObject *Sender)
{
sndPlaySound("snd/dzwiek.wav",SND_ASYNC);
  if(temp==0){t_i[0]=i[6];t_iu[0]=iu[6];k1=6;}

        if(temp==1)
        {
        iu[6]->Visible=false;
        iu[6]->Enabled=false;
        k2=6;
        t_i[1]=i[6];t_iu[1]=iu[6];
        check();
        temp=0;
        }
 else
 {
 iu[6]->Visible=false;
 iu[6]->Enabled=false;
 temp++;
 }
}
//---------------------------------------------------------------------------

void __fastcall TForm1::i6uClick(TObject *Sender)
{
sndPlaySound("snd/dzwiek.wav",SND_ASYNC);
  if(temp==0){t_i[0]=i[5];t_iu[0]=iu[5];k1=5;}

        if(temp==1)
        {
        iu[5]->Visible=false;
        iu[5]->Enabled=false;
        k2=5;
        t_i[1]=i[5];t_iu[1]=iu[5];
        check();
        temp=0;
        }
 else
 {
 iu[5]->Visible=false;
 iu[5]->Enabled=false;
 temp++;
 }
}
//---------------------------------------------------------------------------

void __fastcall TForm1::i5uClick(TObject *Sender)
{
sndPlaySound("snd/dzwiek.wav",SND_ASYNC);
  if(temp==0){t_i[0]=i[4];t_iu[0]=iu[4];k1=4;}

        if(temp==1)
        {
        iu[4]->Visible=false;
        iu[4]->Enabled=false;
        k2=4;
        t_i[1]=i[4];t_iu[1]=iu[4];
        check();
        temp=0;
        }
 else
 {
 iu[4]->Visible=false;
 iu[4]->Enabled=false;
 temp++;
 }
}
//---------------------------------------------------------------------------

void __fastcall TForm1::i4uClick(TObject *Sender)
{
sndPlaySound("snd/dzwiek.wav",SND_ASYNC);
  if(temp==0){t_i[0]=i[3];t_iu[0]=iu[3];k1=3;}

        if(temp==1)
        {
        iu[3]->Visible=false;
        iu[3]->Enabled=false;
        k2=3;
        t_i[1]=i[3];t_iu[1]=iu[3];
        check();
        temp=0;
        }
 else
 {
 iu[3]->Visible=false;
 iu[3]->Enabled=false;
 temp++;
 }
}
//---------------------------------------------------------------------------

void __fastcall TForm1::i3uClick(TObject *Sender)
{
sndPlaySound("snd/dzwiek.wav",SND_ASYNC);
  if(temp==0){t_i[0]=i[2];t_iu[0]=iu[2];k1=2;}

        if(temp==1)
        {
        iu[2]->Visible=false;
        iu[2]->Enabled=false;
        k2=2;
        t_i[1]=i[2];t_iu[1]=iu[2];
        check();
        temp=0;
        }
 else
 {
 iu[2]->Visible=false;
 iu[2]->Enabled=false;
 temp++;
 }
}
//---------------------------------------------------------------------------


void __fastcall TForm1::i2uClick(TObject *Sender)
{
sndPlaySound("snd/dzwiek.wav",SND_ASYNC);
  if(temp==0){t_i[0]=i[1];t_iu[0]=iu[1];k1=1;}

        if(temp==1)
        {
        iu[1]->Visible=false;
        iu[1]->Enabled=false;
        k2=1;
        t_i[1]=i[1];t_iu[1]=iu[1];
        check();
        temp=0;
        }
 else
 {
 iu[1]->Visible=false;
 iu[1]->Enabled=false;
 temp++;
 }
}
//---------------------------------------------------------------------------

void __fastcall TForm1::i1uClick(TObject *Sender)
{
sndPlaySound("snd/dzwiek.wav",SND_ASYNC);
  if(temp==0){t_i[0]=i[0];t_iu[0]=iu[0];k1=0;}

        if(temp==1)
        {
        iu[0]->Visible=false;
        iu[0]->Enabled=false;
        k2=0;
        t_i[1]=i[0];t_iu[1]=iu[0];
        check();
        temp=0;
        }
 else
 {
 iu[0]->Visible=false;
 iu[0]->Enabled=false;
 temp++;
 }
}
//---------------------------------------------------------------------------



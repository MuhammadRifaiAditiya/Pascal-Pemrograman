# Nama      : Muhammad Rifai Aditiya
# Nim       : 312010065
# Kelas     : TI.20.A1

# Latihan

# 1. Program Menghitung Gaji Karywan
 1. Tampilan Utama Program

 ![img](img/Tampilan%20Utama.png)

2. Menghitung Gaji Bersih Direktur Tetap
![img](img/Gaji%20Tetap%20Direktur.png)

3. Menghitung Gaji Bersih Manager Tetap

[img](img/Gaji%20Tetap%20Manager.png)

4. Menghitung Gaji Bersih Karyawan Tetap
[img](img/Gaji%20Karyawan.png)

5. Menghitung Gaji Bersih Direktur Honorer
[img](img/Gaji%20Honorer%20Direktur.png)
6. Menghitung Gaji Bersih Manager Honorer
[img](img/Gaji%20Honorer%20Direktur.png)
7. Menghitung Gaji Bersih Karyawan Honorer
[img](img/Gaji%20Honorer%20Karyawan.png)

Berikut ini source Code Menghitung Gaji Bersih

```pascal

procedure TForm1.btnHitungClick(Sender: TObject);
var
  GajiPokok, TotalGaji, GajiBersih: Double;
  StatusTunjangan: Double;


begin
  GajiPokok := StrToFloat(edtGapok.Text);
  StatusTunjangan := StrToFloat(edtTunjangan.Text);

  TotalGaji := GajiPokok + StatusTunjangan;

  GajiBersih := TotalGaji;

  edtTotalGaji.Text := FormatFloat('#,##0.00', TotalGaji);

end;              

```

<li>Source code Gaji Pokok Otomatis Sesuai Dengan Jabatan</li></br>

```pascal

procedure TForm1.cbJabatanChange(Sender: TObject);
var
  Jabatan: string;
  GajiPokok: Double;

begin
  Jabatan := cbJabatan.Items[cbJabatan.ItemIndex];

  case Jabatan of
    'Direktur': GajiPokok := 5000000;
    'Manager': GajiPokok := 3000000;
    'Karyawan': GajiPokok := 1000000;
  else
    GajiPokok := 0; // Nilai default jika jabatan tidak ada
  end;

  edtGapok.Text := FloatToStr(GajiPokok);
end;

end.     


```

<li>Source code Status Tunjangan Otomatis Sesuai Dengan Status</li></br>

```pascal

procedure TForm1.rbHonorerChange(Sender: TObject);
begin
  if rbHonorer.Checked then
    edtTunjangan.Caption := '500000';

end;

procedure TForm1.rbTetapChange(Sender: TObject);
begin
  if rbTetap.Checked then
    edtTunjangan.Caption := '1500000';
end; 


```

<li>Full Source Code Programnya</li></br>

```pascal

unit Unit1;

{$mode objfpc}{$H+}

interface

uses
  Classes, SysUtils, Forms, Controls, Graphics, Dialogs, StdCtrls, ExtCtrls;

type

  { TForm1 }

  TForm1 = class(TForm)
    btnHitung: TButton;
    btnIsiData: TButton;
    btnClose: TButton;
    cbJabatan: TComboBox;
    edtTotalGaji: TEdit;
    edtTunjangan: TEdit;
    edtGapok: TEdit;
    edtNama: TEdit;
    Label1: TLabel;
    Label2: TLabel;
    Label3: TLabel;
    Label4: TLabel;
    Label5: TLabel;
    rbHonorer: TRadioButton;
    rbTetap: TRadioButton;
    rgStatus: TRadioGroup;
    procedure btnHitungClick(Sender: TObject);
    procedure cbJabatanChange(Sender: TObject);
    procedure rbHonorerChange(Sender: TObject);
    procedure rbTetapChange(Sender: TObject);
    procedure rgStatusClick(Sender: TObject);
  private

  public

  end;

var
  Form1: TForm1;

implementation

{$R *.lfm}

{ TForm1 }

procedure TForm1.rbHonorerChange(Sender: TObject);
begin
  if rbHonorer.Checked then
    edtTunjangan.Caption := '500000';

end;

procedure TForm1.rbTetapChange(Sender: TObject);
begin
  if rbTetap.Checked then
    edtTunjangan.Caption := '1500000';
end;

procedure TForm1.rgStatusClick(Sender: TObject);
begin


end;

procedure TForm1.btnHitungClick(Sender: TObject);
var
  GajiPokok, TotalGaji, GajiBersih: Double;
  StatusTunjangan: Double;


begin
  GajiPokok := StrToFloat(edtGapok.Text);
  StatusTunjangan := StrToFloat(edtTunjangan.Text);

  TotalGaji := GajiPokok + StatusTunjangan;

  GajiBersih := TotalGaji;

  edtTotalGaji.Text := FormatFloat('#,##0.00', TotalGaji);

end;

procedure TForm1.cbJabatanChange(Sender: TObject);
var
  Jabatan: string;
  GajiPokok: Double;

begin
  Jabatan := cbJabatan.Items[cbJabatan.ItemIndex];

  case Jabatan of
    'Direktur': GajiPokok := 5000000;
    'Manager': GajiPokok := 3000000;
    'Karyawan': GajiPokok := 1000000;
  else
    GajiPokok := 0; // Nilai default jika jabatan tidak ada
  end;

  edtGapok.Text := FloatToStr(GajiPokok);
end;

end.

end;

end.

end;

end;

end.


```

# Tugas 2 

# Ouput Tugas 2

1. Penjualan 

![img](img/penjualan.png)

2. Tampilan Harga Mouse Pad

![img](img/Mouse%20Pad.png)

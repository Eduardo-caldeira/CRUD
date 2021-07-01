unit Unit1;

interface

uses
  Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
  Dialogs, DBXpress, DB, Grids, DBGrids, DBClient, SimpleDS, StdCtrls,
  SqlExpr, Buttons, FMTBcd, Menus, ComCtrls;

type
  TForm1 = class(TForm)
    SQLConnection1: TSQLConnection;
    Label1: TLabel;
    SimpleDataSet1: TSimpleDataSet;
    ds1: TDataSource;
    SQLQuery1: TSQLQuery;
    IntegerFieldSimpleDataSet1idCondomino: TIntegerField;
    StringFieldSimpleDataSet1email: TStringField;
    IntegerFieldSimpleDataSet1celular: TIntegerField;
    SmallintFieldSimpleDataSet1sindico: TSmallintField;
    SmallintFieldSimpleDataSet1subsindico: TSmallintField;
    IntegerFieldSimpleDataSet1idPessoa: TIntegerField;
    StringFieldSimpleDataSet1senha: TStringField;
    IntegerFieldSimpleDataSet1fixo: TIntegerField;
    IntegerFieldSimpleDataSet1idCondominio: TIntegerField;
    pgc1: TPageControl;
    ts1: TTabSheet;
    ts2: TTabSheet;
    Label2: TLabel;
    Label3: TLabel;
    Label4: TLabel;
    Label5: TLabel;
    Label6: TLabel;
    Label7: TLabel;
    Label8: TLabel;
    Label9: TLabel;
    Label10: TLabel;
    Label11: TLabel;
    Label12: TLabel;
    Label13: TLabel;
    Label14: TLabel;
    Label15: TLabel;
    Label16: TLabel;
    Label18: TLabel;
    Label19: TLabel;
    Label21: TLabel;
    Label22: TLabel;
    Label23: TLabel;
    edt1: TEdit;
    edt2: TEdit;
    edt3: TEdit;
    edt4: TEdit;
    edt5: TEdit;
    edt6: TEdit;
    edt7: TEdit;
    cbb1: TComboBox;
    cbb2: TComboBox;
    btn1: TBitBtn;
    dbgrd1: TDBGrid;
    edt8: TEdit;
    edt9: TEdit;
    edt10: TEdit;
    edt12: TEdit;
    edt13: TEdit;
    cbb3: TComboBox;
    cbb4: TComboBox;
    edt15: TEdit;
    btn3: TBitBtn;
    btn4: TBitBtn;
    SimpleDataSet2: TSimpleDataSet;
    ds2: TDataSource;
    SQLQuery2: TSQLQuery;
    dbgrd2: TDBGrid;
    Label17: TLabel;
    Label20: TLabel;
    Label24: TLabel;
    Label25: TLabel;
    Label26: TLabel;
    Label27: TLabel;
    Label28: TLabel;
    Label29: TLabel;
    Label30: TLabel;
    Label31: TLabel;
    btn2: TBitBtn;
    btn5: TBitBtn;
    btn6: TBitBtn;
    edt11: TEdit;
    edt14: TEdit;
    edt16: TEdit;
    edt17: TEdit;
    edt18: TEdit;
    edt19: TEdit;
    edt20: TEdit;
    procedure btn1Click(Sender: TObject);
    procedure btn2Click(Sender: TObject);
    procedure btn3Click(Sender: TObject);
    procedure btn4Click(Sender: TObject);
    procedure FormCreate(Sender: TObject);
    procedure btn5Click(Sender: TObject);
    procedure btn6Click(Sender: TObject);
  private
    { Private declarations }
  public
    { Public declarations }
  end;

var
  Form1: TForm1;

implementation

{$R *.dfm}

procedure TForm1.btn1Click(Sender: TObject);
var
   sql : TStrings;
   sindico: String;
   subsindico: String;
begin
   sql:= TStringList.Create;
   if(cbb1.text = 'Não') then
   begin
    sindico := '0';
   end
   else
   begin
    sindico := '1';
   end;

   if(cbb2.text = 'Não') then
   begin
    subsindico := '0';
   end
   else
   begin
    subsindico := '1';
   end;
  sql.Text := 'INSERT INTO condomino values (' + edt1.Text +','+ QuotedStr(edt2.Text) +','+ edt3.Text +','+ sindico + ',' + subsindico + ',' + edt4.Text +','+ QuotedStr(edt5.Text) +','+ edt6.Text +','+ edt7.Text + ')';
  SQLQuery1.SQL := sql;
  SQLQuery1.ExecSQL();
  SimpleDataSet1.Refresh;
  dbgrd1.Update;
  edt1.Text:='';
  edt2.Text:='';
  edt3.Text:='';
  edt4.Text:='';
  edt5.Text:='';
  edt6.Text:='';
  edt7.Text:='';
end;

procedure TForm1.btn2Click(Sender: TObject);
var
   sql : TStrings;
begin
  sql:= TStringList.Create;
  sql.Text := 'INSERT INTO objeto values (' + edt11.Text +','+ QuotedStr(edt14.Text) +','+ edt16.Text +','+ edt17.Text +')';
  SQLQuery2.SQL := sql;
  SQLQuery2.ExecSQL();
  SimpleDataSet2.Refresh;
  dbgrd2.Update;
  edt11.Text :='';
  edt14.Text :='';
  edt16.Text :='';
  edt17.Text :='';
end;



procedure TForm1.btn3Click(Sender: TObject);
var
  sql : TStrings;

begin
  sql:= TStringList.Create;
  sql.Text := 'DELETE FROM condomino WHERE idCondomino =' + edt15.Text;
  SQLQuery1.SQL := sql;
  SQLQuery1.ExecSQL();
  SimpleDataSet1.Refresh;
  dbgrd1.Update;
  edt15.Text := '';
end;

procedure TForm1.btn4Click(Sender: TObject);
var
  sql : TStrings;
  sindico: String;
  subsindico: String;
begin
  sql:= TStringList.Create;
  if(cbb3.text = 'Não') then
   begin
    sindico := '0';
   end
   else
   begin
    sindico := '1';
   end;

   if(cbb4.text = 'Não') then
   begin
    subsindico := '0';
   end
   else
   begin
    subsindico := '1';
   end;
  sql.Text := 'UPDATE condomino SET email = '+ QuotedStr(edt9.Text)+', celular = '+ edt10.Text + ', sindico = '+ sindico + ',subsindico = '+ subsindico + ',senha = '+ QuotedStr(edt12.Text) +', fixo = ' +  edt13.Text + ' WHERE idCondomino =' + edt8.Text;
  SQLQuery1.SQL := sql;
  SQLQuery1.ExecSQL();
  SimpleDataSet1.Refresh;
  dbgrd1.Update;
  edt9.Text:='';
  edt10.Text:='';
  edt12.Text:='';
  edt13.Text:='';
  edt8.Text:='';
end;

procedure TForm1.FormCreate(Sender: TObject);
begin
 SimpleDataSet1.DataSet.CommandText := 'SELECT * FROM condomino';
end;

procedure TForm1.btn5Click(Sender: TObject);
var
  sql : TStrings;

begin
  sql:= TStringList.Create;
  sql.Text := 'DELETE FROM objeto WHERE idObjeto =' + edt18.Text;
  SQLQuery2.SQL := sql;
  SQLQuery2.ExecSQL();
  SimpleDataSet2.Refresh;
  dbgrd2.Update;
  edt18.Text := '';
end;

procedure TForm1.btn6Click(Sender: TObject);
var
  sql : TStrings;
begin
  sql:= TStringList.Create;
  sql.Text := 'UPDATE objeto SET descricao = '+ QuotedStr(edt20.Text) + ' WHERE idObjeto =' + edt19.Text;
  SQLQuery2.SQL := sql;
  SQLQuery2.ExecSQL();
  SimpleDataSet2.Refresh;
  dbgrd1.Update;
  edt19.Text := '';
  edt20.Text := '';
end;

end.

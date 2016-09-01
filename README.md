# de
 //http://hq.sinajs.cn/list=sh601006

var
  Form1: TForm1;
   h: THandle;
   hEdit1: THandle;
     hEdit2: THandle;
     hEdit3: THandle;
     hEdit4: THandle;


implementation

{$R *.dfm}

procedure TForm1.Button1Click(Sender: TObject);
begin
    h:= FindWindow(nil,'网上股票交易系统5.0');
    hEdit1 := GetDlgItem(h,$0000E900);

    hEdit2 := GetDlgItem(hEdit1,$0000E901);

    hEdit3 := GetDlgItem(hEdit2,$00007533);
      // if  hEdit3<>0 then
//MessageBox(self.handle,'没找到该窗口句柄','提示',0);

     //SendMessage(hEdit3,WM_SETTEXT,255,Integer(PChar('609999')));

          SendMessage(hEdit3, BM_CLICK, 0, 0);








          for I := 1 to 100 do
  begin

          s := IdHTTP1.Get('http://hq.sinajs.cn/list=sh601288');
          Memo2.Text := s ;
          p :=MidStr(s,39,5) ;
          Memo1.Text := p;
          // ShowMessage(p);

           sleep(1500);

           sleep(1500);

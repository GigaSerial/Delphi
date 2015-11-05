procedure TMusica.Execute;
begin
  Form1.MediaPlayer1.FileName := 'music.mp3';
  Form1.MediaPlayer1.Open;
  Form1.MediaPlayer1.Play;
end;


procedure TForm1.FormCreate(Sender: TObject);
var
  Thread:TMusica;
begin
//Bloco de Códigos
  Thread := TMusica.Create(False);
  Thread.FreeOnTerminate := True;
  Thread.Resume;
//Outros códigos...
end;

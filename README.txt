var
  A: array[1..10, 1..10] of integer;
  i, j, k, M: byte;

begin
  writeln('������� ������ �������:');
  readln(M);
  writeln('��������� ������� ������� ', M, ' x ', M, ':');
  { ��������� � ������� �������: }
  randomize; { ��������� ��������������� ����� }
  for i := 1 to M do begin
    for j := 1 to M do begin
     { ��������� ����� � ��������� [0, 49]: }
      a[i, j] := random(50);
      write(a[i, j]:4)
    end;
    writeln
  end;
  writeln;
  writeln('������� �������� "��������":');
  for i := 1 to M do begin
    for j := 1 to M + 1 - i do
      write(' ', a[i, j]);
    for k := i + 1 to M do
      write(' ', a[k, M + 1 - i])
  end;
  readln
end.
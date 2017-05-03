var
  A: array[1..10, 1..10] of integer;
  i, j, k, M: byte;

begin
  writeln('Введите размер матрицы:');
  readln(M);
  writeln('Случайная матрица порядка ', M, ' x ', M, ':');
  { Формируем и выводим матрицу: }
  randomize; { генератор псевдослучайных чисел }
  for i := 1 to M do begin
    for j := 1 to M do begin
     { Случайное число с интервала [0, 49]: }
      a[i, j] := random(50);
      write(a[i, j]:4)
    end;
    writeln
  end;
  writeln;
  writeln('Выводим элементы "уголками":');
  for i := 1 to M do begin
    for j := 1 to M + 1 - i do
      write(' ', a[i, j]);
    for k := i + 1 to M do
      write(' ', a[k, M + 1 - i])
  end;
  readln
end.
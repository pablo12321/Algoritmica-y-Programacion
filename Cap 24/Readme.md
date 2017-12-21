## Recursividad
Se dice una accion es recursiva cuando se llama a si misma. 

Una operacion recursiva puede ser directa o indirecta.

Una accion o funcion recursiva directa se llama a si misma.

A→A

En cambio, las indirectas llaman a otra y esta llama a la primera

A→B

B=(B→A)
### Recursión en aumento



```pascal
function factorial_aumento(n,sum:Integer):Integer
begin
  if(n =1) then
    factorial_aumento:= n;
  else
    factorial_aumento:= n * factorial_aumento(n-1);
end;
```
    
### Recursión de cola

La recursion de cola es una tecnica que se usa para optimizar la recursividad, evitando llamar constantemente a la función recursiva.

Ademas, debe cumplir la condición de que en la parte donde realiza la llamada recursiva, no debe haber ninuna otra sentencia.

Una ventaja de la recursion de cola es que evitamos la sobrecarga de cada llamada a la funcion y evitamos el gasto de memoria innecesario.

```pascal
function factorial_cola(n,sum:Integer):Integer
begin
  if(n =1) then
    factorial_cola:= sum;
  else
    factorial_cola:=factorial_cola(n-1,sum*n);
end;
```


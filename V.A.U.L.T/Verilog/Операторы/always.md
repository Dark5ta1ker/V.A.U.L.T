В общем случае оператор `always` языка System­ Verilog имеет вид
```verilog
always @(sensitivity list)
	statement;
```
Оператор выполняется, только когда случается событие, заданное в списке чувствительности.
Или регистр. Зависит от разрядности входа.
```Verilog
always @(posedge clk or posedge reset) begin
    if (reset)     //Проверяем импульс сброса
        q <= 0;
    else if (clk)  //Проверяем синхроимпульс
        q <= d;
end
```

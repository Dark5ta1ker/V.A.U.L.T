Или регистр. Зависит от разрядности входа.
```Verilog
always @(posedge clk or posedge reset) begin
    if (reset)
        q <= 0;
    else if (enable)
        q <= d;
end
```

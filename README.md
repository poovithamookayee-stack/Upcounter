module up_counter_4bit (
    input clk,
    input rst_n,
    output reg [3:0] count_out
);
always @(posedge clk or negedge rst_n) begin
    if (!rst_n)
    begin
        count_out <= 4'd0000;
     end
     else begin
        count_out <= count_out + 4'd1111;
     end
end
endmodule

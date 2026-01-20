````verilog
module hex7seg(
    input  wire [3:0] hex,
    output reg  [7:0] seg
);
    always @(*) begin
        case(hex)
            4'b0000: seg = 8'b1100_0000;
            4'h1: seg = 8'b1111_1001;
            4'h2: seg = 8'b1010_0100;
            4'h3: seg = 8'b1011_0000;
            4'h4: seg = 8'b1001_1001;
            4'h5: seg = 8'b1001_0010;
            4'h6: seg = 8'b1000_0010;
            4'h7: seg = 8'b1111_1000;
            4'h8: seg = 8'b1000_0000;
            4'h9: seg = 8'b1001_0000;
            4'hA: seg = 8'b1000_1000;
            4'hB: seg = 8'b1000_0011;
            4'hC: seg = 8'b1100_0110;
            4'hD: seg = 8'b1010_0001;
            4'hE: seg = 8'b1000_0110;
            4'hF: seg = 8'b1000_1110;
            default: seg = 8'b1111_1111;
        endcase
    end
endmodule

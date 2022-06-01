# HW_LCU_IME_FOR_AVS3
A demo for paper titled "A Hardware-friendly Algorithm for LCU-level Pipe-lined Integer Motion Estimation"

The following items are given to perform a test run.
app_encoder:
  An encoder applying proposed algorithm in paper. 
  The encoder is based on AVS3 reference software High Performance Model (HPM) 4.0.1.
app_decoder:
  The decoder is for AVS3 reference software High Performance Model (HPM) 4.0.1.
encode_IPPP.cfg:
  A configuration file of the test condition described in paper. 
BQSquare_416x240_60.yuv:
  A simple sequence to be coded. 

The demo should be tested on Linux OS with the following cmd lines:
Encoding sequence "BQSquare_416x240_60.yuv" :
"./app_encoder --cfg ./encode_IPPP.cfg -i ./BQSquare_416x240_60.yuv -o ./test.bin -r ./rec.yuv"
Decoding bit stream :
"./app_decoder -i ./test.bin -o ./test.bin -r ./dec.yuv"

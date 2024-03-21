
i) echo "Enter employee name:"
read name,
echo"Enter hours worked:"
read hours
echo"Enter rate per hour:"
read rate
ii) basic pay
basic_pay=$((hours*rate))
iii) if [$basic_pay -gt 15000]; then
tax=$((basic_pay*25/100))
else if($basic_pay -gt 700]; then
tax=$((basic_pay*15/100)) else
tax=0
iv) net pay=$((basic_pay -tax))
results

echo"Employee name:$name" 
echo"Basic pay:$basic_pay"
echo"Tax:$tax"
echo "Net pay:$net_pay"




2

#include <stdio.h> //standard input/output functions #include <stdlib.h> // standard library functions
#include <fcntl.h> //file control functions
#include <unistd.h> // unix standard functions definitions.
int main(){
int file_description; //file descriptor to handle the opened file
file_descriptor = open("example.txt", O_RDWR/ O_CREAT/O_TRUNC,0644);//open a file name ""example.txt" with the r
write permission
// check if the file was successfully opened
if (file_descriptor==-1){
perror("open"); // print error message if opening failed exit(EXIT_FAILURE); // exit the program with the failure status
}
char*message="Hello World";//message to be written inthe file size_t message_len=strlen(message) // length of the message // write the message to the file using the file descriptor
ssize_t bytes_written-write (file_descriptor,message,message_len);

// check if the writing was succesful
if (bytes_written==-1){
perror("write"); // print error message if writing failed exit(EXIT_FAILURE); // Exit the failure program
// move the file pointer to the beginning of the file Iseek(file_descriptor,0,SEEK_SET);
char buffer [256]; //buffer to store the read content
ssize_t bytes -read;//variable to store the number of the bytes read bytes_read=read(file_descriptor, buffer,sizeof(buffer));if (bytes_read==-1
perror ("read");//print error message if reading failed
exit(EXIT_FAILURE);// exit the program with error status
}
//null _terminate the buffer to treat it as a string
buffer[bytes_read]=`\0`;
//print the read content
printf("Read from the file:%s\n", buffer);
//close the file

close(file_descriptor);
close(file_descriptor);
return 0; //exit the program successfully
}




3

#!/bin/bash
i) read -p "Enter Customer ID:"customer_id
read -p"Enter Customer Name:"customer_name
read -p" Enter Units Counsumed:" units_consumed
//initialization
charge_per_unit=0
total_bill=0
ii) if [ $units_consumed -It 200]; then
charge_per_unit=120
elseif[$ units_consumed -ge 200]&&[$units-consumed -It 400]; then
charge_per_unit=150
elseif[$units_consumed -ge 400]&&[$units_consumed -It 600];
 then charge_per_unit=180
else
charge_per_unit=200
fi


total_bill=$((units_consumed*charge_per_unit))
results /display
echo"customer ID:$customer_id"
echo"customer
Name:$customer_name"
echo"Units consumed:$units_consumed"
echo"Charge per unit;$charge_per_unit'
echo "Total Bill:$total_bill KSH"

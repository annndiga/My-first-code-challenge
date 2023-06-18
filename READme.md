## Net Salary Calculator

 # project description

*The project aims at creating a calculator that would calculate the Payee Tax, NHIF, NSSF duductions and net salary



# project set up 

*The Net Salary calculator code provided consists of several functions that calculate the payee tax, NHIF deduction, NSSF deduction, and net salary based on the given gross salary, basic salary, and benefits.

explanation of determining payee tax is as follows:

1) let

//Declares that the payeeTax variable to 0. It hplds the calculated payee tax amount.

let payeeTax = 0;

2) if... , else if... , else ... statetement

//Determine the payee tax based on different gross salary ranges.

//If the gross salary is less than or equal to 2400, the payee tax is set to 0.

if (grossSalary <= 2400){
        payeeTax = 0;

// If the gross salary is betweem 2401 and 32333, the payee tax is calculated by multiplying the difference between the gross salary and 24000 by 0.1(10%) .        

} else if (grossSalary <= 32333){
        payeeTax = (grossSalary - 24000) * 0.1;
}

 /* else statement evaaluates where the gross salary exceeds the declared value.   
Here, the payee tax is calculated by multiplying the difference between the gross salary  and 115833 by 0.35(35%) and adding 28943.
*/

else {
        payeeTax = (grossSalary - 115833) * 0.35 + 28943;
      }


explanation of determining NHIF is as follows:

1) let

// Declares  the NHIF variable as 0.

let nhif = 0;

2)if... ,else if... , else.... statements

// determine the NHIF deduction based on different gross salary ranges

 if (grossSalary <= 5999) {
    nhif = 150;
  }

- The calculated NHIF deduction is returned using the return statement.


Explanation for calculating net salary;

   /* function calculateNetSalary(basicSalary, benefits) { ... }: This is the function definition for calculating the net salary. It takes two values, basicSalary and benefits.
   */

   1)  const ....

    const grossSalary = basicSalary + benefits; {
  const payeeTax = calculatePayeeTax(grossSalary);
  const nhif = calculateNHIF(grossSalary);
  const nssf = calculateNSSF(grossSalary);

  const deductions = payeeTax + nhif + nssf;
  const netSalary = grossSalary - deductions;

  return netSalary;
}

const basicSalary = 40000;
const benefits = 600000;

const netSalary = calculateNetSalary(basicSalary, benefits);



   2) console.log();

//It logs the net salary value to the console, along with a descriptive message.

    console.log("Net Salary:", netSalary);



In my case  my Net salary was : 423498.55 .

/home/ann/.nvm/versions/node/v20.2.0/bin/node ./index.js
Net Salary: 423498.55000000005



Thankyou for reading through!!!.



























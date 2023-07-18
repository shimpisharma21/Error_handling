# Error_handling
### EmployeeContract

This contract defines an employee contract where only the designated employee is allowed to call certain functions.

#### Functions

##### 'onlyEmployee()'
function onlyEmployee() public view
This function is a view function with no return value. It is a modifier that can be applied to other functions to restrict access to the employee. It checks whether the caller is the designated employee and reverts with an error message if not.

##### 'employeeIsHere()'
function employeeIsHere() public view
This function is a view function with no return value. It checks if the caller is the designated employee. If the caller is not the employee, it reverts with an error message.

##### 'Employee()'
function Employee() public view
This function is a view function with no return value. It uses an assert statement to ensure that the caller is the designated employee. If the caller is not the employee, it will cause the transaction to fail.

#### Usage

The address that deploys the contract will be set as the employee.
The employee can then call functions with the onlyEmployee modifier to perform restricted actions.
Other addresses will receive an error if they try to call restricted functions.



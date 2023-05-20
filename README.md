# Problem statement

A company wants a program that will calculate the weekly paycheck for an employee based on how many hours they worked. For this company, an employee earns $20 an hour for the first 40 hours that they work. The employee earns overtime, $30 an hour, for each hour they work above 40 hours.

Example: If an employee works 60 hours in a week, they would earn $20/hr for the first 40 hours. Then they would earn $30/hr for the 20 hours they worked overtime. Therefore, they earned: ($20/hr * 40hrs) + ($30/hr * 20 hrs) = $800 + $600 = $1400 total.

## Pseusdocode

```
function validateInput(number_of_hours_worked, base_hourly_wage, overtime_hourly_wage):
    INITIALIZE message to 'all inputs are valid'
    INITIALIZE is_valid to TRUE
    IF number_of_hours_worked is less than zero or is not an number THEN
        SET message to 'number_of_hours_worked must be a non-negative integer'
        SET is_valid to FALSE
    ELSE IF base_hourly_wage is less than zero or is not a number THEN
        SET message to 'base_hourly_wage must be a non-negative integer'
        SET is_valid to FALSE
    ELSE IF overtime_hourly_wage is less than zero or is not a number THEN
        SET message to 'overtime_hourly_wage must be a non-negative integer'
        SET is_valid to FALSE
    END IF
    RETURN a namedtuple with is_valid and message as elements


function calculateWage(number_of_hours_worked, base_hourly_wage, overtime_hourly_wage):
    INITIALIZE wage_result to zero
    IF number_of_hours_worked is greater than forty THEN
        ADD forty multiplied by base_hourly_wage to wage_result
        SET the number_of_hours_worked to number_of_hours_worked minus forty
        ADD the number_of_hours_worked times the overtime_hourly_wage to wage_result
    ELSE
        ADD the number_of_hours_worked times the base_hourly_wage to wage_result
    END IF
    RETURN wage_result


function main():
    INITIALIZE final_result to None
    INITIALIZE validation_result to None
    INITIALIZE number_of_hours_worked_by_employee, base_hourly_wage, and overtime_hourly_wage to zero
    GET the number_of_hours_worked_by_employee, base_hourly_wage, and overtime_hourly_wage from standard input
    SET number_of_hours_worked_by_employee, base_hourly_wage, and overtime_hourly_wage to values recieved from standard input
    CALL the validateInput function, passing in number_of_hours_worked, base_hourly_wage, and overtime_hourly_wage
    SET the validation_result result to the output of the valideInput function
    IF validation_result.is_valid is TRUE THEN
        CALL the calculateWage function, passing in number_of_hours_worked, base_hourly_wage, and overtime_hourly_wage
        SET the final_result to the output of the calculageWage function
    ELSE
        SET the final_result to validation_result.message
    END IF
    PRINT the final_result


CALL the main function
```

## Program Flowchart

![Flow Chart](WeeklyWageFlowchart.jpeg)
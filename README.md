# Problem statement

A company wants a program that will calculate the weekly paycheck for an employee based on how many hours they worked. For this company, an employee earns $20 an hour for the first 40 hours that they work. The employee earns overtime, $30 an hour, for each hour they work above 40 hours.

Example: If an employee works 60 hours in a week, they would earn $20/hr for the first 40 hours. Then they would earn $30/hr for the 20 hours they worked overtime. Therefore, they earned: ($20/hr * 40hrs) + ($30/hr * 20 hrs) = $800 + $600 = $1400 total.

## Pseusdocode

```
function validateInput(number_of_hours_worked, base_hourly_wage, overtime_hourly_wage):
    SET message variable to a string indicating success
    SET is_valid variable to TRUE
    IF number_of_hours_worked is less than 0 or is not an number THEN
        SET message to a string indicating number_of_hours_worked is invalid
        SET is_valid_variable to FALSE
    ELSE IF base_hourly_wage is less than 0 or is not a number THEN
        SET message to a string indicating bas_hourly_wage is invalid
        SET is_valid_variable to FALSE
    ELSE IF overtime_hourly_wage is less than 0 or is not a number THEN
        SET message to a string indicating overtime_hourly_wage is invalid
        SET is_valid_variable to FALSE
    END IF
    RETURN a namedtuple with is_valid and message as elements


function calculateWage(number_of_hours_worked, base_hourly_wage, overtime_hourly_wage):
    SET wage_result variable to 0
    IF number_of_hours_worked is greater than 40 THEN
        ADD 40 multiplied by base_hourly_wage to wage_result
        SET the number_of_hours_worked variable to number_of_hours_worked minus 40
        ADD the number_of_hours_worked times the overtime_hourly_wage to wage_result
    ELSE
        ADD the number_of_hours_worked times the base_hourly_wage to wage_result
    END IF
    RETURN wage_result


function main():
    SET final_result variable to an empty string
    SET validation_result variable to None
    SET number_of_hours_worked_by_employee, base_hourly_wage, and overtime_hourly_wage variables to 0
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
## Pseusdocode

```
function validateInput(number of hours worked, base hourly wage, overtime hourly wage):
    IF any of the inputs are invalid THEN
        RETURN FALSE and an error message indicating the invalid input
    ELSE
        RETURN TRUE and a message indicating success
    END IF


function calculateWage(number of hours worked, base hourly wage, overtime hourly wage):
    SET the initial result to 0
    IF the number of hours worked is greater than 40 THEN
        ADD 40 multiplied by the base hourly wage to result
        SUBTRACT the number of hours worked by 40
        ADD the number of hours worked remaining times the overtime hourly wage to result
    ELSE
        ADD the number of hours worked times the base hourly wage to result
    END IF
    RETURN result


function main():
    SET the result to an empty string
    GET the number of hours worked by employee, base hourly wage, and overtime hourly wage from standard input
    CALL the validateInput function, passing in the number of hours worked, base hourly wage, and overtime hourly wage
    IF the validateInput function returns TRUE THEN
        CALL the calculateWage function, passing in the number of hours worked, base hourly wage, and overtime hourly wage
        SET the result to a string containing the employee's wages for the week
    ELSE
        SET the result to the error message recieved from the validateInput function
    END IF
    PRINT the result to standard output


CALL the main function
```

## Flowchart

![Flow Chart](WeeklyWageFlowchart.jpeg)
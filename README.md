## Pseusdocode

```
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
    GET the number of hours worked by employee
    GET the base hourly wage
    GET the overtime hourly wage
    CALL the calculateWage function, passing in the number of hours worked, base hourly wage, and overtime hourly wage
    GET the weekly wages result from the calculateWage function
    PRINT the result
```

## Flowchart

![Flow Chart](WeeklyWageFlowchart.jpeg)
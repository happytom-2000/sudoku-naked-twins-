# sudoku-naked-twins-
"""Eliminate values using the naked twins strategy.      Parameters     ----------     values(dict)      
a dictionary of the form {'box_name': '123456789', ...}      Returns     -------     dict       
The values dictionary with the naked twins eliminated from peers      Notes     -----     
Your solution can either process all pairs of naked twins from the input once,    
or it can continue processing pairs of naked twins until there are no such     
pairs remaining -- the project assistant test suite will accept either    
convention. However, it will not accept code that does not process all pairs   

of naked twins from the original input. (For example, if you start processing     
pairs of twins and eliminate another pair of twins before the second pair    
is processed then your code will fail the PA test suite.)      
The first convention is preferred for consistency with the other strategies,   
and because it is simpler (since the reduce_puzzle function already calls this    
strategy repeatedly).     """


def naked_twins(values):
    # TODO: Implement this function!
    for unit in unitlist:
        for box1 in peers:
            for box2 in peers:
                if (box1 == box2) and  len(box1) == 2 and len(box2) == 2:
                   possible_value1 = box1[0]
                   possible_value2 = box1[1]
        for box in unitlist:
          for peer in peers[box]:
             for number in box:
                if number == possible_value1 or value == possible_value2:
                   values[peer] = values[peer].replace(number,'' )
    return values


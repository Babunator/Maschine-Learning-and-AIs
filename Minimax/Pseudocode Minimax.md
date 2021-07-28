# Pseudocode Minimax (for e.g Tic-Tac-Toe)

```
function findBestMove(board):
    bestMove = NULL
    # Traverse all cells, evaluate minimax function for all empty cells. And return the cell with optimal value
    for each move in board :
        if current move is better than bestMove
            bestMove = current move
    return bestMove
    
function minimax(board, depth, isMaximizingPlayer):
       
    #If  Maximizer has won the game return positive value, for Minimizer negative, for tie 0
    if current board state is a terminal state :
        return value of the board
    
    if isMaximizingPlayer :
        bestVal = -INFINITY 
        # Traverse through all cells/board positions
        for each move in board :
            #Call minimax recursively and choose the maximum value
            value = minimax(board, depth+1, false)
            bestVal = max( bestVal, value) 
        return bestVal

    else :
        bestVal = +INFINITY 
        for each move in board :
            #Call minimax recursively and choose the minimum value
            value = minimax(board, depth+1, true)
            bestVal = min( bestVal, value) 
        return bestVal 
        
if maximizer has won:
    return WIN_SCORE – depth

else if minimizer has won:
    return LOOSE_SCORE + depth
```

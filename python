class Board():
    def __init__(self):
        self.game = ['','','','','','','','','','']
        print("Welcome to Tic-Tac-Toe\n")

        
    def display(self):
        print(" %s  |  %s | %s" %(self.game[1],self.game[2],self.game[3]))
        print("-----------")
        print(" %s  |  %s | %s" %(self.game[4],self.game[5],self.game[6]))
        print("-----------")
        print(" %s  |  %s | %s" %(self.game[7],self.game[8],self.game[9]))
    
    
    def update_board(self,cell_no, player):
        if self.game[cell_no] == '':
            self.game[cell_no] = player
    
    
    def is_winner(self,player):
        if self.game[1] == self.game[2] == self.game[3] == player:
            return True
        if self.game[4] == self.game[5] == self.game[6] == player:
            return True
        if self.game[7] == self.game[8] == self.game[9] == player:
            return True
        if self.game[1] == self.game[4] == self.game[7] == player:
            return True
        if self.game[2] == self.game[5] == self.game[8] == player:
            return True
        if self.game[3] == self.game[6] == self.game[9] == player:
            return True
        if self.game[1] == self.game[5] == self.game[9] == player:
            return True
        if self.game[3] == self.game[5] == self.game[7] == player:
            return True
        return False 
    
    
    def is_tie(self):
        cells_used = 0
        for i in self.game:
            if i != '':
                cells_used+=1
        if cells_used == 9:
            return True
        else:
            return False    
    
    
    def reset(self):
        self.game = ['','','','','','','','','','']
board = Board()        


while True: 
    board.display()

    X_choice = int(input("\nX Choose a no between 1-9 :\n "))
    board.update_board(X_choice,'X')
    if board.is_winner('X'):
        print("\n X wins! \n")
        play_again = input("Would you like to play again (Y/N) ? \n").upper()
        if play_again == 'Y':
            board.reset()
            continue
        else:
            break


    if board.is_tie():
        print("\n Tie game! \n")
        play_again = input("Would you like to play again (Y/N) ? \n").upper()
        if play_again == 'Y':
            board.reset()
            continue
        else:
            break    


    O_choice = int(input("\nO Choose a no between 1-9 :\n "))
    board.update_board(O_choice,'O')
    if board.is_winner('O'):
        print("\n O wins! \n")
        play_again = input("Would you like to play again (Y/N) ? \n").upper()
        if play_again == 'Y':
            board.reset()
            continue
        else:
            break


    if board.is_tie():
        print("\n Tie game! \n")
        play_again = input("Would you like to play again (Y/N) ? \n").upper()
        if play_again == 'Y':
            board.reset()
            continue
        else:
            break     


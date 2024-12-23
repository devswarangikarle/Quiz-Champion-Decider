# Quiz-Champion-Decider

As the judge of an intense science quiz, Neha was in charge of overseeing a contest between two teams over N rounds. In each round, one of the two teams secured a win. The team that won the most rounds would be declared the quiz champion. Now, Neha needs to determine which team came out on top. Can you help her find the winning team?

def find_quiz_champion(n, winners):
    # Dictionary to store the count of wins for each team
    win_count = {}
    
    # Count wins
    for team in winners:
        if team in win_count:
            win_count[team] += 1
        else:
            win_count[team] = 1
    
    # Find the team with the maximum wins
    champion = max(win_count, key=win_count.get)
    return champion

# Input
n = int(input())
winners = [input().strip() for _ in range(n)]
print(find_quiz_champion(n, winners))

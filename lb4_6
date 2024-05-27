import random

# Граф с одной компонентой
graph = {
    1: [(0.3, 1), (0.5, 2), (0.1, 3), (0.1, 8)],
    2: [(0.4, 1), (0.3, 2), (0.3, 6)],
    3: [(0.4, 1), (0.1, 3), (0.4, 6), (0.1, 8)],
    6: [(0.4, 2), (0.3, 3), (0.2, 6), (0.1, 8)],
    8: [(0.1, 1), (0.1, 2), (0.2, 3), (0.4, 6), (0.2, 8)],
} 

# счетчик переходов между состояниями
states = {
    1: 0,
    2: 0,
    3: 0,
    6: 0,
    8: 0
}

#функция поиска следующего шага
def nextStep(cur_class):
    curr_mass = graph[cur_class]
    probabilities, values = zip(*curr_mass)
    selected_value = random.choices(values, probabilities)[0]
    return selected_value

#Основная функция выполнения задания
def solve(steps, start_node):
    mass_steps = []
    for i in range(steps):
        states[start_node] += 1
        mass_steps.append(start_node)
        start_node = nextStep(start_node)
    return mass_steps

steps = [10, 100, 1000]
start_nodes = [1,2,3,6,8]
for j in start_nodes:
  for i in steps:
      mass = solve(i, j)
      print(mass)

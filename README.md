import math

def f(x):
    return x - math.atan(x**(1/3))

a = 0.0
b = 1.0
epsilon = 1e-5

while (b - a) / 2 > epsilon:
    m = (a + b) / 2
    if f(m) == 0:
        break
    elif f(a) * f(m) < 0:
        b = m
    else:
        a = m

print("Təqribi kök:", (a + b) / 2)

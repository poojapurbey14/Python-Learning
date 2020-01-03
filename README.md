# Generate the first 20 Fibonacci numbers
def gen_fib():
    a,b = 1,1
    yield a
    yield b
    while True:
        a,b = b,a+b
        yield b
g = gen_fib()

fibs = [next(g) for _ in range(20)]
print(fibs)

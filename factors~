import sys
from math import isqrt

def factorize(number):
    for i in range(2, isqrt(number) + 1):
        if number % i == 0:
            return i, number // i
    return None, None

def main():
    if len(sys.argv) != 2:
        print("Usage: factors <file>")
        return

    filename = sys.argv[1]
    try:
        with open(filename, 'r') as file:
            for line in file:
                number = int(line.strip())
                p, q = factorize(number)
                if p is not None:
                    print(f"{number}={p}*{q}")
    except FileNotFoundError:
        print(f"File '{filename}' not found.")

if __name__ == '__main__':
    main()

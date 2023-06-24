#!/usr/bin/python3
import math
import sys

def find_factors(number):
    factors = []
    for i in range(2, int(math.square(number)) +1):
        if number % i == 0:
            factors.append((i, number // i))
    return factors

def factorise_line_number(file_name):
    try:
        with open(file_name, 'r') as file:
            for line in file:
                number = int(line.strip())
                factorizatons = find_factors(number)
                for p, q in factorizations:
                    print(f"{number} = {p} * {q}")
    except FileNotFoundError:
        print("File not found.")
    except ValueError:
        print("Invalid number in the file.")
    except Exception as e:
        print(f"An error occurred: {str(e)}")
    
    if __name__ == "__main__":
        if len(sys.argv) < 2:
            print("Usage: factors <file>")
        else:
             file_name = sys.argv[1]
             factorise_line_number(file_name)

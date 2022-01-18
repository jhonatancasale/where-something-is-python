# Brain dump of Python learning notes

## Basic data types

```python
integer: int = 42            # We can use type hints, Python interpreter tends do ignore it entirely
another_integer = 42_000_000 # We can safely ignore the _, it's just for visual convenience

floating: float = .42        # We can be lazy and omit the 0 before 0.42

string: str = "This is a string"
another_string: str = 'This is another string'
f_string: str = f"4! equals to {4 * 3 * 2 * 1}"

boolean: bool = True
another_bollean: bool = False
```

## Functions
```python
def func1() -> None:
    print("Do something")


def func2() -> str:
    return "Return something"


def func3(a: int, b: int) -> None:
    print(f"Inside: {a} + {b} => {a + b}")


def func4(a: int, b: int) -> int:
    print(f"Inside: {a} + {b} => {a + b}")

    return a + b


def func5(a: int, b: int) -> int:
    return a ** b


def func6(*args, times=1) -> int:
    return sum([arg for arg in args]) * times


print(f"func1: {func1()}")
# We do something inside the function and implicitly return None

print(f"func2: {func2()}")
# We return something to the caller

print(f"func3: {func3(2, 5)}")
# We do something inside with the given params but we return implicitly None

print(f"func4: {func4(3, 39)}")
# We do something inside with the given param and return some relevant value to the caller

print(f"func5: {func5(2, 10)}")
print(
    f"func5: {func5(b=10, a=2)}"
)  # we can change the param order provided by the names

# And we can pass an undefined list of unnamed arguments
print(f"func6: {func6(1, 2, 3)}")
print(f"func6: {func6(1, 2, 3, 4, 5, 6)}")
print(f"func6: {func6(1, 2, 3, 4, 5, 6, 7, 8, 9, 0)}")
print(f"func6: {func6(1, 2, 3, 4, 5, 6, 7, 8, 9, 0, times=2)}")
```

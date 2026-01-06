import unittest
from typing import Union

# Type Alias for clarity (accepts integers and floats)
Number = Union[int, float]

def add_numbers(a: Number, b: Number) -> Number:
    """
    Calculates the sum of two numbers.

    Args:
        a (int or float): The first number.
        b (int or float): The second number.

    Returns:
        int or float: The sum of a and b.
    """
    return a + b

class TestAddNumbers(unittest.TestCase):
    """Unit tests for the add_numbers function."""

    def test_add_positive_integers(self):
        """Test addition of two positive integers."""
        self.assertEqual(add_numbers(2, 2), 4)

    def test_add_negative_integers(self):
        """Test addition involving negative numbers."""
        self.assertEqual(add_numbers(-1, 100), 99)

    def test_add_floats(self):
        """Test addition of floating point numbers."""
        self.assertAlmostEqual(add_numbers(0.1, 0.2), 0.3, places=1)

    def test_incorrect_sum(self):
        """Ensure incorrect sums are identified as not equal."""
        self.assertNotEqual(add_numbers(1, 3), 5)

if __name__ == '__main__':
    unittest.main()

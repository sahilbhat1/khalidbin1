import unittest

def add_numbers(a, b):
    return a + b

class TestAddNumbers(unittest.TestCase):
    def test_add_numbers(self):
        self.assertEqual(add_numbers(2, 2), 4)
        self.assertEqual(add_numbers(-1, 100), 99)
        self.assertNotEqual(add_numbers(1, 3), 5)

if __name__ == '__main__':
    unittest.main() 

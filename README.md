# leetcode-Excel-sheet-column-number.py
problem-171

class Solution:
    def titleToNumber(self, columnTitle: str) -> int:
        multiplier = 1
        column = 0
        for i in range(len(columnTitle) - 1, -1, -1):
            column += (ord(columnTitle[i]) - 64) * multiplier
            multiplier *= 26
        return column

        # Solution 2
        # ans, pos = 0, 0
        # for letter in reversed(columnTitle):
        #     digit = ord(letter)-64
        #     ans += digit * 26**pos
        #     pos += 1
            
        # return ans

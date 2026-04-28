# Bingo_Kata
### 關於這個套路 
- [TDD BUDDY](https://www.tddbuddy.com/katas/bingo.html) 
- [codewars](https://www.codewars.com/kata/566d5e2e57d8fae53c00000c) 

### 規則
- 賓果卡有 25 格
  - B 列範圍 1 - 15 
  - I 列範圍 16 - 30
  - N 列範圍 31 - 45 (第3格必須是 FREE SPACE)
  - G 列範圍 46 - 60
  - O 列範圍 61 - 75
- 賓果號碼
  - 數字介於 1 - 75 (遊戲中號碼不會重複)
- 檢查賓果卡
  - 賓果號碼在賓果卡必須連成垂直、水平或對角線才有賓果

### 測試案例
#### 賓果卡 (Bingo Card)
<img src="images/bingo-card.jpg" alt="image" width="50%">

#### 賓果線 (Bingo Line)
<img src="images/bingo-line.jpg" alt="image" width="50%">

#### `Vertical Line`
| FakePickBallNumbers | Output |
| :----: | :----: |
| [10, 2, 1, 11, 15] | [ "V1" ] |
| [28, 17, 29, 16, 22] | [ "V2" ] |
| [31, 45, 35, 41] | [ "V3" ] |
| [55, 59, 51, 48, 54] | [ "V4" ] |
| [61, 70, 74, 67, 66] | [ "V5" ] |

#### `Horizontal Line`
| FakePickBallNumbers | Output |
| :----: | :----: |
| [10, 28, 31, 55, 61] | [ "H1" ] |
| [2, 17, 45, 59, 70] | [ "H2" ] |
| [1, 29, 51, 74] | [ "H3" ] |
| [11, 16, 35, 48, 67] | [ "H4" ] |
| [15, 22, 41, 54, 66] | [ "H5" ] |

#### `Diagonal Line`
| FakePickBallNumbers | Output |
| :----: | :----: |
| [10, 17, 48, 66] | [ "D1" ] |
| [61, 59, 16, 15] | [ "D2" ] |

#### `Multiple Lines`
| FakePickBallNumbers | Output |
| :----: | :----: |
| [31, 45, 35, 41, 1, 29, 51, 74] | [ "V3", "H3" ] |
| [10, 2, 1, 11, 15, 22, 41, 54, 66, 61, 59, 16, 15] | [ "V1", "H5", "D2" ] |
| [10, 17, 48, 66, 61, 59, 16, 15, 31, 45, 35, 41, 1, 29, 51, 74] | [ "V3", "H3", "D1", "D2" ] |
| [28, 17, 29, 16, 22, 55, 59, 51, 48, 54, 2, 45, 70, 11, 35, 67, 10, 66] | [ "V2", "V4", "H2", "H4", "D1" ] |

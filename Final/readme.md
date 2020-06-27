
## An AI version of Snake
### Concept
給予一張地圖，蛇在不碰壁與不碰撞自己身體的狀態下，吃到得分點。吃到得分點之後，長度會增加一並進入下一張地圖。
### Upload files
* TA ans 
    1. 只有前後左右是否可以往前走，同一排遇到障礙的話會選擇其他路徑
    2. 有判斷是否會撞到自己
* version_1
    1. 將過去走過的路也記錄下來，避免重複同樣道路
    2. 吃到得分點後，走過的道路會消除
### Other files
* writing_map.py - 將助教的map 獨進之後輸出成c++ vector的格式
* random_map.py - 自己製作地圖，製造不只一個分數點，與不只一個障礙，隨機分佈在地圖中
* record_map.txt - 記錄不同版本的函數的效果
### Notes
* 如果是在 private 的參數，要直接呼叫才能對他作出改變，經過函數呼叫會做出一個copy constructor，這樣在進行計算的時候就不會動到原值

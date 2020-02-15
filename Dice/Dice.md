# ลูกเต๋า @boardname@

## เกริ่นนำ @unplugged
**ลูกเต๋า** เป็นอุปกรณ์สำหรับเล่นเกมต่างๆ หรือคุณครูอาจใช้เป็นสื่อการสอนเรื่อง **ความน่าจะเป็น** ก็ได้

เราจะมาลองสร้างลูกเต๋าด้วย @boardname@ แล้วทอยลูกเต๋า ด้วยการ**เขย่า** (**Shake**) บอร์ด @boardname@ กัน

## ขั้นที่ 1 @fullscreen
เมื่อเราเขย่าบอร์ด @boardname@ ก็จะเกิด**อีเวนต์** ``||input:on shake||`` ขึ้นมา เราก็จะมาเริ่มเขียนโปรแกรมจาก**อีเวนต์**นี้

## ขั้นที่ 2
คลิ้กกลุ่ม ``||input:Input||`` แล้วลากอีเวนต์ ``||input:on shake||`` มาวาง

```blocks
input.onGesture(Gesture.Shake, function () {})
```

## ขั้นที่ 3
ให้คุณสร้างตัวแปร (``variable``) เพื่อเก็บตัวเลข **1-6** ที่เราจะสุ่มขึ้นมาในขั้นต่อไป

## ขั้นที่ 4
คลิ้กกลุ่ม ``||variables:Variables||`` แล้วคลิ้กปุ่ม **Make a Variable...** จากนั้นตั้งชื่อตัวแปรว่า **Dice** เสร็จแล้วคลิ้กปุ่ม **OK**

![Steps to Create Variable](https://github.com/narongporn/microbitTutorial/raw/master/Dice/image/2020-02-15_2120.png)

## ขั้นที่ 5

คลิ้กกลุ่ม ``||variables:Variables||`` แล้วลากบล็อก ``||variables:set Dice to 0||`` มาใส่ในอีเวนต์ ``||input:on shake||``

```blocks
let Dice = 0
input.onGesture(Gesture.Shake, function () {
    Dice = 0
})
```

## ขั้นที่ 6

```blocks
let Dice = 0
input.onGesture(Gesture.Shake, function () {
    Dice = Math.randomRange(1, 6)
    if (Dice == 1) {
        basic.showLeds(`
            . . . . .
            . . . . .
            . . # . .
            . . . . .
            . . . . .
            `)
    } else if (Dice == 2) {
        basic.showLeds(`
            # . . . .
            . . . . .
            . . . . .
            . . . . .
            . . . . #
            `)
    } else if (Dice == 3) {
        basic.showLeds(`
            # . . . .
            . . . . .
            . . # . .
            . . . . .
            . . . . #
            `)
    } else if (Dice == 4) {
        basic.showLeds(`
            # . . . #
            . . . . .
            . . . . .
            . . . . .
            # . . . #
            `)
    } else if (Dice == 5) {
        basic.showLeds(`
            # . . . #
            . . . . .
            . . # . .
            . . . . .
            # . . . #
            `)
    } else {
        basic.showLeds(`
            # . . . #
            . . . . .
            # . . . #
            . . . . .
            # . . . #
            `)
    }
})
```

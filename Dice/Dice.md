# ลูกเต๋า @boardname@

## เกริ่นนำ @unplugged

## ขั้นที่ 1 @fullscreen

ในการทอยลูกเต๋า เราจะใช้วิธี**เขย่า** (**Shake**) บอร์ด @boardname@ โดยเมื่อเราเขย่าบอร์ด ก็จะเกิด**เหตุการณ์** หรือ**อีเวนต์** (``Event``) ขึ้น

ให้คุณคลิ้กกลุ่ม ``||input:Input||`` แล้วลากอีเวนต์ ``||input:on shake||`` มาวาง

```blocks
input.onGesture(Gesture.Shake, function () {})
```

## ขั้นที่ 2

ให้คุณสร้างตัวแปร (``variable``) เพื่อเก็บตัวเลข **1-6** ที่เราจะสุ่มขึ้นมาในขั้นต่อไป

ในการสร้างตัวแปร คุณต้องคลิ้กกลุ่ม ``||variables:variables||``

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

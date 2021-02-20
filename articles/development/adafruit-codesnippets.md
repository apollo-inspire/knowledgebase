# Arduino Codesnippets

sonar sensor

```ts
let distance = 0
loops.forever(function () {
   pins.A2.digitalWrite(false)
   control.waitMicros(2)
   pins.A2.digitalWrite(true)
   control.waitMicros(10)
   pins.A2.digitalWrite(false)
   distance = pins.A1.pulseIn(PulseValue.High) / 58
   light.graph(distance, 30)
   if (distance >= 0.25 && distance <= 50) {
       
   }
   console.logValue("distancecm", distance)
})
```

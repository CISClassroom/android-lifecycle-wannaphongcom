# รายงานผลการทดลอง

นายวรรณพงษ์ ภัททิยไพบูลย์ 603410214-3

## คำสั่งการแสดงผลผ่าน Logcat


```kotlin
import android.util.Log
```

Debug log

```kotlin
Log.debug("tag", "Log")
```

Error log

```kotlin
Log.error("tag", "This is an error message")
```

Info log

```kotlin
Log.info("tag", "This is an info message")
Log.i("tag", "This is an info message")
```

Verbose log

```kotlin
Log.v("tag", "This is an info message") 
```

Warning log

```kotlin
Log.warning("tag", "Hello World")
```

## SNACKBAR และ TOST

คำสั่งแสดง Snackbar

```kotlin
Snackbar.make(view, "ทดสอบระบบ Snackbar", Snackbar.LENGTH_LONG).setAction("Action", null).show()
```

คำสั่งแสดง Tost

```kotlin
Toast.makeText(this, "Hi", Toast.LENGTH_LONG).show()
```

## Android LiveCycle Activity

จงอธิบายการทำงานของเมธอทต่อไปนี้ ว่าเกิดขึ้นเมื่อใดของโปรแกรม พร้อมแสดงตัวอย่างโค้ดการทำงานของเมธอท (กำหนดให้แสดง log message เมื่อมีการทำงานของเมธอท)

1. onCreate() -> เป็นเมธอทไว้กำหนดการทำงานเมื่อ Activity ถูกเรียกขึ้นมา

```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        setSupportActionBar(toolbar)

        Log.i("onCreate","Activity created")
    }
```

2. onStart() -> เป็นเมธอทที่ถูกเรียกหลังจาก onCreate และจะทำงานหลังจากที่แอปทำงานเบื้องหลังกลับมาที่ Application อีกครั้ง

```kotlin
override fun onResume() {
        super.onResume()
        Log.d("Activity State ", "onResume")
    }
```

3. onResume() -> เป็นเมธอทที่ถูกเรียกเมื่อ Activity ปรากฎให้ผู้ใช้เห็นและเริ่มโต้ตอบกับผู้ใช้ ซึ่งจุดนี้ activity ของเราจะอยู่บนสุดของ stack และรับ input ต่าง ๆ จากผู้ใช้ได้

```kotlin
override fun onResume() {
        super.onResume()
        Log.i("onResume", "Activity resume")
    }
```

4. onPause() -> เป็นเมธอทไว้กำหนดการทำงานเมื่อ Activity ถูกรันไปเบื้องหลัง

```kotlin
override fun onPause() {
        super.onPause()
        Log.d("Activity State ", "onPause")
    }
```

5. onStop() -> เป็นเมธอทไว้กำหนดการทำงานเมื่อ Activity ถูกรันไปเบื้องหลังนาน ๆ Android จะหยุดการทำงานนั้น

```kotlin
    override fun onStop() {
        super.onStop()
        Log.d("Activity State ", "onStop")
    }
```

6. onDestroy() -> เป็นเมธอทจะทำงานเมื่อ User ออกจาก App ก่อนที่ activity ถูกทำลายไป

```kotlin
override fun onDestroy() {
        super.onDestroy()
        Log.d("Activity State ", "onDestroy")
    }
```

7. onRestart() -> เป็นเมธอทที่จะถูกเรียกเมื่อ Activity กำลังจะกลับมาแสดงผลให้ผู้ใช้เห็นอีกครั้งหลังจากที่ถูก activity อื่นบังอยู่

```kotlin
override fun onRestart() {
        super.onRestart()
        Log.d("Activity State ", "onRestart")
    }
```

## Start new Activity

คำสั่งสำหรับเปิด activity ใหม่

```kotlin
var i = Intent(this,NameOfActivity::class.java)
startActivity(i)
```

คำสั่งสำหรับเปิด activity ใหม่ ผ่านเมนู setting

```kotlin
override fun onOptionsItemSelected(item: MenuItem): Boolean {
        // Handle action bar item clicks here. The action bar will
        // automatically handle clicks on the Home/Up button, so long
        // as you specify a parent activity in AndroidManifest.xml.
        return when (item.itemId) {
            R.id.action_settings -> {
                var i = Intent(this,Main2Activity::class.java)
                startActivity(i)
                return true
            }
            else -> super.onOptionsItemSelected(item)
        }
    }
```

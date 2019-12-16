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
//Add your code here
```

คำสั่งแสดง Tost

```kotlin
//Add your code here
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
        fab.setOnClickListener { view ->
            Log.i("onClick","FAB Clicked")
            Snackbar.make(view, "ทดสอบระบบ", Snackbar.LENGTH_LONG)
                .setAction("Action", null).show()
        }
    }
```

2. onStart() ->

```kotlin
//Add your code here
```

3. onResume() ->

```kotlin
override fun onResume() {
        super.onResume()
        Log.i("onResume", "Activity resume")
    }
```

4. onPause() -> เป็นเมธอทไว้กำหนดการทำงานเมื่อ Activity ถูกรันไปเบื้องหลัง

```kotlin
//Add your code here
```

5. onStop() -> เป็นเมธอทไว้กำหนดการทำงานเมื่อ Activity ถูกรันไปเบื้องหลังนาน ๆ Android จะหยุดการทำงานนั้น

```kotlin
//Add your code here
```

6. onDestroy() ->

```kotlin
//Add your code here
```

7. onRestart() ->

```kotlin
//Add your code here
```

## Start new Activity

คำสั่งสำหรับเปิด activity ใหม่

```kotlin
//Add your code here
```

คำสั่งสำหรับเปิด activity ใหม่ ผ่านเมนู setting

```kotlin
//Add your code here
```

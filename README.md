# Android Practical – Set A

8 Marks | Questions 1 to 20 | Complete XML and Kotlin solutions

**How to use:** Each question has an XML layout and a Kotlin Activity. Copy the XML into `activity_main.xml` and the Kotlin code into `MainActivity.kt`. Use the copy button at the top right of each code block.

**Important:** In every Kotlin file, change `com.example.myapplication` to the package name at the top of your own `MainActivity.kt`. Do not change XML IDs unless you also change the matching Kotlin IDs.

**Input note:** Questions that accept whole numbers use integer input. Other calculation questions use decimal input.

## Contents

1. [Q.1 – Addition of Two Numbers](#q1)
2. [Q.2 – Subtraction of Two Numbers](#q2)
3. [Q.3 – Multiplication of Two Numbers](#q3)
4. [Q.4 – Division of Two Numbers](#q4)
5. [Q.5 – Area of Rectangle](#q5)
6. [Q.6 – Area of Square](#q6)
7. [Q.7 – Area of Circle](#q7)
8. [Q.8 – Square of a Number](#q8)
9. [Q.9 – Cube of a Number](#q9)
10. [Q.10 – Even or Odd](#q10)
11. [Q.11 – Area of Triangle](#q11)
12. [Q.12 – Average of Two Numbers](#q12)
13. [Q.13 – Celsius to Fahrenheit Conversion](#q13)
14. [Q.14 – Positive, Negative or Zero](#q14)
15. [Q.15 – Largest of Two Numbers](#q15)
16. [Q.16 – Largest of Three Numbers](#q16)
17. [Q.17 – Pass or Fail with Marks Validation](#q17)
18. [Q.18 – Simple Interest](#q18)
19. [Q.19 – Perimeter of Rectangle](#q19)
20. [Q.20 – Percentage Calculation](#q20)

<a id="q1"></a>
## Q.1 – Addition of Two Numbers

Accept two numbers and display their sum when the Add button is clicked.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/num1"
        android:hint="Enter first number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/num2"
        android:hint="Enter second number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnAdd"
        android:text="Add"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnAdd)
        button.setOnClickListener {
            val num1 = findViewById<EditText>(R.id.num1)
            val num2 = findViewById<EditText>(R.id.num2)
            val result = findViewById<TextView>(R.id.txtResult)

            val a = num1.text.toString().toDouble()
            val b = num2.text.toString().toDouble()

            result.text = "Sum = ${a + b}"
        }
    }
}
```

Sample input: 10, 20  
Expected output: Sum = 30.0

---

<a id="q2"></a>
## Q.2 – Subtraction of Two Numbers

Accept two numbers and display their difference when the Subtract button is clicked.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/num1"
        android:hint="Enter first number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/num2"
        android:hint="Enter second number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnSubtract"
        android:text="Subtract"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnSubtract)
        button.setOnClickListener {
            val num1 = findViewById<EditText>(R.id.num1)
            val num2 = findViewById<EditText>(R.id.num2)
            val result = findViewById<TextView>(R.id.txtResult)

            val a = num1.text.toString().toDouble()
            val b = num2.text.toString().toDouble()

            result.text = "Difference = ${a - b}"
        }
    }
}
```

Sample input: 20, 8  
Expected output: Difference = 12.0

---

<a id="q3"></a>
## Q.3 – Multiplication of Two Numbers

Accept two numbers and display their product when the Multiply button is clicked.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/num1"
        android:hint="Enter first number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/num2"
        android:hint="Enter second number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnMultiply"
        android:text="Multiply"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnMultiply)
        button.setOnClickListener {
            val num1 = findViewById<EditText>(R.id.num1)
            val num2 = findViewById<EditText>(R.id.num2)
            val result = findViewById<TextView>(R.id.txtResult)

            val a = num1.text.toString().toDouble()
            val b = num2.text.toString().toDouble()

            result.text = "Product = ${a * b}"
        }
    }
}
```

Sample input: 5, 4  
Expected output: Product = 20.0

---

<a id="q4"></a>
## Q.4 – Division of Two Numbers

Accept two numbers and display their quotient when the Divide button is clicked. Display an appropriate message if the second number is zero.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/num1"
        android:hint="Enter first number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/num2"
        android:hint="Enter second number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnDivide"
        android:text="Divide"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnDivide)
        button.setOnClickListener {
            val num1 = findViewById<EditText>(R.id.num1)
            val num2 = findViewById<EditText>(R.id.num2)
            val result = findViewById<TextView>(R.id.txtResult)

            val a = num1.text.toString().toDouble()
            val b = num2.text.toString().toDouble()

            if (b == 0.0) {
                result.text = "Cannot divide by zero"
            } else {
                result.text = "Quotient = ${a / b}"
            }
        }
    }
}
```

Sample input: 10, 2  
Expected output: Quotient = 5.0; if second number is 0: Cannot divide by zero

---

<a id="q5"></a>
## Q.5 – Area of Rectangle

Accept the length and breadth of a rectangle and calculate its area.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/length"
        android:hint="Enter length"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/breadth"
        android:hint="Enter breadth"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnCalculate"
        android:text="Calculate"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnCalculate)
        button.setOnClickListener {
            val length = findViewById<EditText>(R.id.length)
            val breadth = findViewById<EditText>(R.id.breadth)
            val result = findViewById<TextView>(R.id.txtResult)

            val l = length.text.toString().toDouble()
            val b = breadth.text.toString().toDouble()

            val area = l * b
            result.text = "Area = $area"
        }
    }
}
```

Sample input: 5, 3  
Expected output: Area = 15.0

---

<a id="q6"></a>
## Q.6 – Area of Square

Accept the side of a square and calculate its area.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/side"
        android:hint="Enter side"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnCalculate"
        android:text="Calculate"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnCalculate)
        button.setOnClickListener {
            val side = findViewById<EditText>(R.id.side)
            val result = findViewById<TextView>(R.id.txtResult)

            val s = side.text.toString().toDouble()

            val area = s * s
            result.text = "Area = $area"
        }
    }
}
```

Sample input: 4  
Expected output: Area = 16.0

---

<a id="q7"></a>
## Q.7 – Area of Circle

Accept the radius of a circle and calculate its area.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/radius"
        android:hint="Enter radius"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnCalculate"
        android:text="Calculate"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnCalculate)
        button.setOnClickListener {
            val radius = findViewById<EditText>(R.id.radius)
            val result = findViewById<TextView>(R.id.txtResult)

            val r = radius.text.toString().toDouble()

            val area = 3.14 * r * r
            result.text = "Area = $area"
        }
    }
}
```

Sample input: 2  
Expected output: Area = 12.56

Formula: Area of circle = 3.14 × radius × radius.

---

<a id="q8"></a>
## Q.8 – Square of a Number

Accept a number and calculate its square.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/number"
        android:hint="Enter number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnCalculate"
        android:text="Calculate"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnCalculate)
        button.setOnClickListener {
            val number = findViewById<EditText>(R.id.number)
            val result = findViewById<TextView>(R.id.txtResult)

            val n = number.text.toString().toDouble()

            val square = n * n
            result.text = "Square = $square"
        }
    }
}
```

Sample input: 6  
Expected output: Square = 36.0

---

<a id="q9"></a>
## Q.9 – Cube of a Number

Accept a number and calculate its cube.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/number"
        android:hint="Enter number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnCalculate"
        android:text="Calculate"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnCalculate)
        button.setOnClickListener {
            val number = findViewById<EditText>(R.id.number)
            val result = findViewById<TextView>(R.id.txtResult)

            val n = number.text.toString().toDouble()

            val cube = n * n * n
            result.text = "Cube = $cube"
        }
    }
}
```

Sample input: 3  
Expected output: Cube = 27.0

---

<a id="q10"></a>
## Q.10 – Even or Odd

Accept a number and check whether it is even or odd.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/number"
        android:hint="Enter an integer"
        android:inputType="number"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnCheck"
        android:text="Check"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnCheck)
        button.setOnClickListener {
            val number = findViewById<EditText>(R.id.number)
            val result = findViewById<TextView>(R.id.txtResult)

            val n = number.text.toString().toInt()

            if (n % 2 == 0) {
                result.text = "Even Number"
            } else {
                result.text = "Odd Number"
            }
        }
    }
}
```

Sample input: 7  
Expected output: Odd Number

---

<a id="q11"></a>
## Q.11 – Area of Triangle

Accept the base and height of a triangle and calculate its area.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/base"
        android:hint="Enter base"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/height"
        android:hint="Enter height"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnCalculate"
        android:text="Calculate"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnCalculate)
        button.setOnClickListener {
            val base = findViewById<EditText>(R.id.base)
            val height = findViewById<EditText>(R.id.height)
            val result = findViewById<TextView>(R.id.txtResult)

            val b = base.text.toString().toDouble()
            val h = height.text.toString().toDouble()

            val area = (b * h) / 2
            result.text = "Area = $area"
        }
    }
}
```

Sample input: 6, 4  
Expected output: Area = 12.0

---

<a id="q12"></a>
## Q.12 – Average of Two Numbers

Accept two numbers and calculate their average.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/num1"
        android:hint="Enter first number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/num2"
        android:hint="Enter second number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnAverage"
        android:text="Average"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnAverage)
        button.setOnClickListener {
            val num1 = findViewById<EditText>(R.id.num1)
            val num2 = findViewById<EditText>(R.id.num2)
            val result = findViewById<TextView>(R.id.txtResult)

            val a = num1.text.toString().toDouble()
            val b = num2.text.toString().toDouble()

            val average = (a + b) / 2
            result.text = "Average = $average"
        }
    }
}
```

Sample input: 10, 20  
Expected output: Average = 15.0

---

<a id="q13"></a>
## Q.13 – Celsius to Fahrenheit Conversion

Accept temperature in Celsius and convert it into Fahrenheit.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/celsius"
        android:hint="Enter temperature in Celsius"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnConvert"
        android:text="Convert"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnConvert)
        button.setOnClickListener {
            val celsius = findViewById<EditText>(R.id.celsius)
            val result = findViewById<TextView>(R.id.txtResult)

            val c = celsius.text.toString().toDouble()

            val fahrenheit = (c * 9 / 5) + 32
            result.text = "Fahrenheit = $fahrenheit"
        }
    }
}
```

Sample input: 0  
Expected output: Fahrenheit = 32.0

Formula: Fahrenheit = (Celsius × 9/5) + 32.

---

<a id="q14"></a>
## Q.14 – Positive, Negative or Zero

Accept a number and check whether it is positive, negative or zero.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/number"
        android:hint="Enter number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnCheck"
        android:text="Check"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnCheck)
        button.setOnClickListener {
            val number = findViewById<EditText>(R.id.number)
            val result = findViewById<TextView>(R.id.txtResult)

            val n = number.text.toString().toDouble()

            if (n > 0) {
                result.text = "Positive Number"
            } else if (n < 0) {
                result.text = "Negative Number"
            } else {
                result.text = "Zero"
            }
        }
    }
}
```

Sample input: -5  
Expected output: Negative Number

---

<a id="q15"></a>
## Q.15 – Largest of Two Numbers

Accept two numbers and display the largest number.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/num1"
        android:hint="Enter first number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/num2"
        android:hint="Enter second number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnFind"
        android:text="Find Largest"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnFind)
        button.setOnClickListener {
            val num1 = findViewById<EditText>(R.id.num1)
            val num2 = findViewById<EditText>(R.id.num2)
            val result = findViewById<TextView>(R.id.txtResult)

            val a = num1.text.toString().toDouble()
            val b = num2.text.toString().toDouble()

            if (a > b) {
                result.text = "Largest = $a"
            } else if (b > a) {
                result.text = "Largest = $b"
            } else {
                result.text = "Both numbers are equal"
            }
        }
    }
}
```

Sample input: 12, 8  
Expected output: Largest = 12.0

---

<a id="q16"></a>
## Q.16 – Largest of Three Numbers

Accept three numbers and display the largest number.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/num1"
        android:hint="Enter first number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/num2"
        android:hint="Enter second number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/num3"
        android:hint="Enter third number"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnFind"
        android:text="Find Largest"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnFind)
        button.setOnClickListener {
            val num1 = findViewById<EditText>(R.id.num1)
            val num2 = findViewById<EditText>(R.id.num2)
            val num3 = findViewById<EditText>(R.id.num3)
            val result = findViewById<TextView>(R.id.txtResult)

            val a = num1.text.toString().toDouble()
            val b = num2.text.toString().toDouble()
            val c = num3.text.toString().toDouble()

            if (a >= b && a >= c) {
                result.text = "Largest = $a"
            } else if (b >= a && b >= c) {
                result.text = "Largest = $b"
            } else {
                result.text = "Largest = $c"
            }
        }
    }
}
```

Sample input: 10, 25, 15  
Expected output: Largest = 25.0

---

<a id="q17"></a>
## Q.17 – Pass or Fail with Marks Validation

Accept student marks out of 100 and display Pass or Fail. Accept marks only between 0 and 100.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/marks"
        android:hint="Enter marks (0 to 100)"
        android:inputType="number"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnCheck"
        android:text="Check Result"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnCheck)
        button.setOnClickListener {
            val marks = findViewById<EditText>(R.id.marks)
            val result = findViewById<TextView>(R.id.txtResult)

            val m = marks.text.toString().toInt()

            if (m < 0 || m > 100) {
                result.text = "Enter marks between 0 and 100"
            } else if (m >= 40) {
                result.text = "Pass"
            } else {
                result.text = "Fail"
            }
        }
    }
}
```

Sample input: 75  
Expected output: Pass (this example uses 40 as the passing mark; follow your college's rule if different)

Passing-mark note: The question paper says Pass or Fail but does not specify the passing threshold. This example uses 40 as a common illustrative threshold. Change 40 if your teacher specifies another value.

---

<a id="q18"></a>
## Q.18 – Simple Interest

Accept Principal, Rate and Time and calculate Simple Interest.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/principal"
        android:hint="Enter principal"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/rate"
        android:hint="Enter rate"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/time"
        android:hint="Enter time"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnCalculate"
        android:text="Calculate"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnCalculate)
        button.setOnClickListener {
            val principal = findViewById<EditText>(R.id.principal)
            val rate = findViewById<EditText>(R.id.rate)
            val time = findViewById<EditText>(R.id.time)
            val result = findViewById<TextView>(R.id.txtResult)

            val p = principal.text.toString().toDouble()
            val r = rate.text.toString().toDouble()
            val t = time.text.toString().toDouble()

            val si = (p * r * t) / 100
            result.text = "Simple Interest = $si"
        }
    }
}
```

Sample input: 1000, 5, 2  
Expected output: Simple Interest = 100.0

Formula: Simple Interest = (Principal × Rate × Time) / 100.

---

<a id="q19"></a>
## Q.19 – Perimeter of Rectangle

Accept the length and breadth of a rectangle and calculate its perimeter.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/length"
        android:hint="Enter length"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/breadth"
        android:hint="Enter breadth"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnCalculate"
        android:text="Calculate"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnCalculate)
        button.setOnClickListener {
            val length = findViewById<EditText>(R.id.length)
            val breadth = findViewById<EditText>(R.id.breadth)
            val result = findViewById<TextView>(R.id.txtResult)

            val l = length.text.toString().toDouble()
            val b = breadth.text.toString().toDouble()

            val perimeter = 2 * (l + b)
            result.text = "Perimeter = $perimeter"
        }
    }
}
```

Sample input: 5, 3  
Expected output: Perimeter = 16.0

---

<a id="q20"></a>
## Q.20 – Percentage Calculation

Accept marks obtained and maximum marks and calculate the percentage. Handle maximum marks equal to zero.

### 1. XML – activity_main.xml

```xml
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/obtained"
        android:hint="Enter marks obtained"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <EditText
        android:id="@+id/maximum"
        android:hint="Enter maximum marks"
        android:inputType="numberDecimal"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/btnCalculate"
        android:text="Calculate"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <TextView
        android:id="@+id/txtResult"
        android:textSize="20sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:paddingTop="12dp" />
</LinearLayout>
```

### 2. Kotlin – MainActivity.kt

```kotlin
package com.example.myapplication

import android.os.Bundle
import android.widget.Button
import android.widget.EditText
import android.widget.TextView
import androidx.appcompat.app.AppCompatActivity

class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.btnCalculate)
        button.setOnClickListener {
            val obtained = findViewById<EditText>(R.id.obtained)
            val maximum = findViewById<EditText>(R.id.maximum)
            val result = findViewById<TextView>(R.id.txtResult)

            val obtainedMarks = obtained.text.toString().toDouble()
            val maximumMarks = maximum.text.toString().toDouble()

            if (maximumMarks == 0.0) {
                result.text = "Maximum marks cannot be zero"
            } else {
                val percentage = (obtainedMarks / maximumMarks) * 100
                result.text = "Percentage = $percentage%"
            }
        }
    }
}
```

Sample input: 80, 100  
Expected output: Percentage = 80.0%

Formula: Percentage = (Marks obtained / Maximum marks) × 100.

---

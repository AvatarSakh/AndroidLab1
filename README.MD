<h2 align="center">  МИНИСТЕРСТВО НАУКИ И ВЫСШЕГО ОБРАЗОВАНИЯ РОССИЙСКОЙ ФЕДЕРАЦИИ ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ БЮДЖЕТНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯ «САХАЛИНСКИЙ ГОСУДАРСТВЕННЫЙ УНИВЕРСИТЕТ» </h2>
<div align="center">
<h3>Институт естественных наук и техносферной безопасности
<br>
Кафедра информатики
<br>
Половников Владислав Олегович</h3>

<br>
<h3>Лабораторная работа №1
<br>
“Первое Android-приложение”
<br>
01.03.02 Прикладная математика и информатика</h3>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<h3 align="right">Научный руководитель
<br>
Соболев Евгений Игоревич
</h3>

<h3 align="center">Южно-Сахалинск
<br>
2023г.
</h3>
<hr>
</div>
<p>
Kotlin - это высокоэффективный современный язык программирования, разработанный компанией JetBrains. Он имеет очень чёткий и лаконичный синтаксис, что делает ваш код лёгким для чтения. Kotlin широко используется во всём мире, и его популярность среди разработчиков постоянно растёт. Многие разработчики, использующие Kotlin, отмечают, что это делает их работу быстрее и увлекательнее.
</p>

<h3 align="center">Задание</h3>

Измените уведомление так, чтобы оно отображалось в верхней, а не в нижней части экрана. Для изменения способа отображения уведомления воспользуйтесь функцией setGravity класса Toast. Выберите режим Gravity.TOP. За дополнительнной информацией обращайтесь к документации разработчика по адресу developer. 
android.com/reference/kotlin/android/widget/Toast#setgravity.


<h2 align="center">Решение</h2>

```kotlin
package com.example.lab1

import androidx.appcompat.app.AppCompatActivity
import android.os.Bundle
import android.view.Gravity
import android.view.View
import android.widget.Button
import android.widget.Toast


class MainActivity : AppCompatActivity() {

    private lateinit var trueButton: Button
    private lateinit var falseButton: Button

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        trueButton = findViewById(R.id.true_button)
        falseButton = findViewById(R.id.false_button)

        trueButton.setOnClickListener { view: View ->
            val toast = Toast.makeText(
                this,
                R.string.correct_toast,
                Toast.LENGTH_SHORT)
            toast.setGravity(Gravity.TOP,0,0)
            toast.show()
        }
        falseButton.setOnClickListener { view: View ->
            val toast = Toast.makeText(
                this,
                R.string.incorrect_toast,
                Toast.LENGTH_SHORT)
            toast.setGravity(Gravity.TOP,0,0)
            toast.show()
        }
    }

}

```

<h2 align="center">Вывод</h2>
Я научился создавать примитивное android-приложение.
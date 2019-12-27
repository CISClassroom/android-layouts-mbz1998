# รายงานผลการทดลอง

<นางสาวอาทิตยา ฉิมมาแก้ว> <603410321-2>

## Relative Layout

แสดง Control `title` และ `Detail`

```xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".RelativeActivity">

    <EditText
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:inputType="textPersonName"
        android:text="Name"
        android:ems="10"
        android:id="@+id/editText4" android:layout_marginTop="28dp" android:layout_alignParentTop="true"
        android:layout_alignParentStart="true" android:layout_marginStart="5dp"/>
    <EditText
        android:layout_width="218dp"
        android:layout_height="wrap_content"
        android:inputType="textPersonName"
        android:text="Name"
        android:ems="10"
        android:id="@+id/editText5" android:layout_alignParentStart="true"
        android:layout_marginStart="3dp" android:layout_alignParentEnd="true" android:layout_marginEnd="190dp"
        android:layout_marginTop="154dp" android:layout_alignParentTop="true"/>
    <EditText
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:inputType="textPersonName"
        android:text="Name"
        android:ems="10"
        android:id="@+id/editText" android:layout_alignParentTop="true" android:layout_marginTop="94dp"
        android:layout_alignStart="@+id/editText5" android:layout_marginStart="0dp"/>
</RelativeLayout>
```

แอดทริบิ้วที่แสดงความสัมพันธ์ระหว่าง control ทั้งสอง

```xml
android:layout_above = "id/editText" หมายความว่า กำหนดให้  editText อยู่ด้านบนจากตัวที่อ้างอิง
```

## Linear Layout

แสดง Control `to`, `subject`, `tag` และ `message`

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".LinearActivity">
    <EditText
        android:id="@+id/editText"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:ems="10"
        android:inputType="textPersonName"
        android:text="Name"
        tools:layout_editor_absoluteX="14dp"
        tools:layout_editor_absoluteY="20dp" />

    <LinearLayout
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="horizontal">

        <EditText
            android:id="@+id/editText2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:ems="10"
            android:inputType="textPersonName"
            android:text="Name"
            tools:layout_editor_absoluteX="16dp"
            tools:layout_editor_absoluteY="86dp" />

        <EditText
            android:id="@+id/editText3"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:ems="10"
            android:inputType="textPersonName"
            android:text="Name"
            tools:layout_editor_absoluteX="14dp"
            tools:layout_editor_absoluteY="151dp" />
    </LinearLayout>

    <EditText
        android:id="@+id/editText4"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="1"
        android:ems="10"
        android:gravity="start|top"
        android:inputType="textMultiLine" />

    <Button
        android:id="@+id/button"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Button"
        tools:layout_editor_absoluteX="17dp"
        tools:layout_editor_absoluteY="210dp" />
</LinearLayout>
```

อธิบายความแตกต่างระหว่าง vertical และ horizontal orientation

```
vertical orientation คือ คำสั่งในการจัด layout ให้อยู่ในแนวตั้ง
ส่วน horizontal orientation คือ คำสั่งในการจัด layout ให้อยู่ในแนวนอน

```

## Constrant Layout

จงออกแบบและสร้างหน้า Constrant layout สำหรับแสดงข้อมูลนักศึกษา ประกอบไปด้วย รูปโปรไฟล์ รูปพื้นหลัง ชื่อ-นามสกุล รหัสนักศึกษา และเกรดเฉลี่ยรวม

```xml
<!--your Profile Activity Layout-->
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".ConstraintActivity">

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="417dp"
        android:layout_height="244dp"
        android:scaleType="fitXY"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.96"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:srcCompat="@drawable/cover" />

    <ImageView
        android:id="@+id/imageView2"
        android:layout_width="253dp"
        android:layout_height="262dp"
        android:layout_marginStart="84dp"
        android:layout_marginTop="96dp"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:srcCompat="@drawable/fah" />

    <TextView
        android:id="@+id/textView2"
        android:layout_width="233dp"
        android:layout_height="35dp"
        android:layout_marginStart="84dp"
        android:text="ชื่อ : นางสาวอาทิตยา ฉิมมาแก้ว"
        android:textColor="#F08080"
        android:textSize="18sp"
        app:layout_constraintStart_toStartOf="parent"
        tools:layout_editor_absoluteY="426dp" />

    <TextView
        android:id="@+id/textView3"
        android:layout_width="216dp"
        android:layout_height="18dp"
        android:layout_marginStart="84dp"
        android:layout_marginTop="24dp"
        android:text="รหัสนักศึกษา  603410321-2"
        android:textColor="#F08080"
        android:textSize="18sp"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView2" />

    <TextView
        android:id="@+id/textView4"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="84dp"
        android:layout_marginTop="28dp"
        android:text="เกรดเฉลี่ย 2.89"
        android:textColor="#F08080"
        android:textSize="18sp"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView3" />

    <Button
        android:id="@+id/button4"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="160dp"
        android:layout_marginBottom="92dp"
        android:text="Back"
        android:textColor="#020202"
        android:textSize="18sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintStart_toStartOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>
```

# Tippy
App used for calculating the total amount with respect to the percentage of tip offered.

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <!-- Views on left side -->

    <TextView
        android:id="@+id/tvBaseLabel"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="32dp"
        android:layout_marginTop="52dp"
        android:text="Base"
        android:textAppearance="@style/TextAppearance.AppCompat.Medium"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/tvTipPercentLabel"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="32dp"
        android:textAppearance="@style/TextAppearance.AppCompat.Medium"
        android:textStyle="bold"
        app:layout_constraintEnd_toEndOf="@id/tvBaseLabel"
        app:layout_constraintTop_toBottomOf="@+id/tvBaseLabel"
        tools:text="24%" />

    <TextView
        android:id="@+id/tvTipLabel"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="56dp"
        android:text="Tip"
        android:textAppearance="@style/TextAppearance.AppCompat.Medium"
        app:layout_constraintEnd_toEndOf="@id/tvBaseLabel"
        app:layout_constraintTop_toBottomOf="@+id/tvTipPercentLabel" />

    <TextView
        android:id="@+id/tvTotalLabel"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="32dp"
        android:text="Total"
        android:textAppearance="@style/TextAppearance.AppCompat.Medium"
        app:layout_constraintEnd_toEndOf="@id/tvBaseLabel"
        app:layout_constraintTop_toBottomOf="@+id/tvTipLabel" />

    <!-- Views on right side -->
    <EditText
        android:id="@+id/etBaseAmount"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="32dp"
        android:ems="8"
        android:hint="Bill Amount"
        android:inputType="numberDecimal"
        android:textSize="24sp"
        app:layout_constraintBottom_toBottomOf="@id/tvBaseLabel"
        app:layout_constraintStart_toEndOf="@+id/tvBaseLabel"
        app:layout_constraintTop_toTopOf="@id/tvBaseLabel"
        tools:layout_editor_absoluteY="30dp" />

    <SeekBar
        android:id="@+id/seekBarTip"
        android:layout_width="200dp"
        android:layout_height="wrap_content"
        android:max="30"
        app:layout_constraintBottom_toBottomOf="@+id/tvTipPercentLabel"
        app:layout_constraintStart_toStartOf="@+id/etBaseAmount"
        app:layout_constraintTop_toTopOf="@+id/tvTipPercentLabel" />

    <TextView
        android:id="@+id/tvTipAmount"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:textAppearance="@style/TextAppearance.AppCompat.Large"
        app:layout_constraintBottom_toBottomOf="@+id/tvTipLabel"
        app:layout_constraintStart_toStartOf="@+id/seekBarTip"
        app:layout_constraintTop_toTopOf="@+id/tvTipLabel"
        tools:text="19.96" />

    <TextView
        android:id="@+id/tvTotalAmount"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:textAppearance="@style/TextAppearance.AppCompat.Large"
        app:layout_constraintBottom_toBottomOf="@+id/tvTotalLabel"
        app:layout_constraintStart_toStartOf="@+id/tvTipAmount"
        app:layout_constraintTop_toTopOf="@+id/tvTotalLabel"
        tools:text="103.11" />

    <TextView
        android:id="@+id/tvFooter"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="32dp"
        android:fontFamily="sans-serif-condensed-light"
        android:text="Made with ❤ ️by Abrar"
        android:textAllCaps="true"
        android:textAppearance="@style/TextAppearance.AppCompat.Medium"
        android:textStyle="italic"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

    <TextView
        android:id="@+id/tvTipDescription"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="8dp"
        android:textStyle="bold"
        app:layout_constraintEnd_toEndOf="@+id/seekBarTip"
        app:layout_constraintStart_toStartOf="@+id/seekBarTip"
        app:layout_constraintTop_toBottomOf="@+id/seekBarTip"
        tools:text="Acceptable" />

</androidx.constraintlayout.widget.ConstraintLayout>

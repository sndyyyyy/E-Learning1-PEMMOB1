# TUGAS E-LEARNING
Tugas ini berisikan projek sederhana yang di dalamnya terdapat input control berupa Date Time dan Alert

## DATE TIME
Date time merupakan salah satu input control untuk memilih tanggal yang terdapat pada kalender
Untuk source codenya sendiri sebagai berikut:
```
    private fun showDatePicker() {
        val calendar = Calendar.getInstance()
        val datePickerDialog = DatePickerDialog(
            this,
            { _, year, month, dayOfMonth ->
                val selectedDate = "$dayOfMonth/${month + 1}/$year"
                tvResult.text = getString(R.string.label_selected_date, selectedDate)
            },
            calendar.get(Calendar.YEAR),
            calendar.get(Calendar.MONTH),
            calendar.get(Calendar.DAY_OF_MONTH)
        )
        datePickerDialog.show()
    }

```

## ALERT
Alert sendiri berarti peringatan, di mana alert ini seperti validasi yang di mana akan memunculkan pilihan YES atau No ketika akan melakukan suatu activity
Untuk source codenya sendiri sebagai berikut:
```
    private fun showAlertDialog() {
        val builder = AlertDialog.Builder(this)
        builder.setTitle(getString(R.string.alert_title))
        builder.setMessage(getString(R.string.alert_message))
        builder.setPositiveButton(getString(R.string.alert_yes)) { _, _ ->
            Toast.makeText(this, getString(R.string.toast_yes), Toast.LENGTH_SHORT).show()
        }
        builder.setNegativeButton(getString(R.string.alert_no)) { _, _ ->
            Toast.makeText(this, getString(R.string.toast_no), Toast.LENGTH_SHORT).show()
        }
        builder.show()
    }
}
```

Namun, sebelumnya pastikan untuk menginisialisasikan terlebih dahulu kedua kelas di atas

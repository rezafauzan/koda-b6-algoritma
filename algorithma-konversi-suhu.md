# Algorithma Program Konversi Suhu

## Algorithma Descriptive

1. Mulai
2. Masukan angka suhu dalam satuan celcius
3. Konversi angka suhu ke fahrenheit dengan rumus angka suhu dikali sembilan per lima kemudian hasilnya ditambah dengan tiga puluh dua kemudian tampilkan hasilnya
4. konversi angka suhu ke kelvin dengan rumus angka suhu ditambah dua ratus tujuh puluh tiga koma lima belas kemudian tampilkan hasilnya
5. konversi angka suhu ke reamur dengan rumus angka suhu dikali empat per lima kemudian tampilkan hasilnya
6. Selesai

```mermaid
flowchart TD

start@{"shape": circle, "label": "Mulai"}
input@{"shape": lean-l, "label": "Input: suhuCelcius"}
isNumber@{"shape": diamond, "label": "typeOf suhuCelcius == number"}
outputNotNumber@{"shape": lean-l, "label": "Output: #quot;Inputan harus berupa angka#quot;"}
toFahrenheit@{"shape": rectangle, "label": "fahrenheit = suhuCelcius * 1.8"}
outputFahrenheit@{"shape": lean-l, "label": "Output: suhuCelcius + #quot;celcius sama dengan #quot; + fahrenheit + #quot; dalam fahrenheit#quot;"}
toKelvin@{"shape": rectangle, "label": "kelvin = suhuCelcius + 273.15"}
outputKelvin@{"shape": lean-l, "label": "Output: suhuCelcius + #quot;celcius sama dengan #quot; + kelvin + #quot; dalam kelvin#quot;"}
toReamur@{"shape": rectangle, "label": "reamur = suhuCelcius *0.8"}
outputReamur@{"shape": lean-l, "label": "Output: suhuCelcius + #quot;celcius sama dengan #quot; + reamur + #quot; dalam reamur#quot;"}
stop@{"shape": dbl-circ, "label": "Selesai"}

start-->input-->isNumber--True-->toFahrenheit-->outputFahrenheit
-->toKelvin-->outputKelvin
-->toReamur-->outputReamur-->stop

isNumber--False-->outputNotNumber-->stop

```
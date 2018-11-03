---
title: DataTypeEnum Enumeration (DAO)
TOCTitle: DataTypeEnum Enumeration
ms:assetid: 59ead483-52fc-53cd-02e6-084814f961ac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194420(v=office.15)
ms:contentKeyID: 48545028
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a1c576d44a0c91c92072ddf5c61a11e7cd38457
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937556"
---
# <a name="datatypeenum-enumeration-dao"></a>DataTypeEnum Enumeration (DAO)


**Применимо к**: Access 2013, Office 2013

Указывает тип объекта рабочих данных.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbAttachment</p></td>
<td><p>101</p></td>
<td><p>Данные вложения</p></td>
</tr>
<tr class="even">
<td><p>dbBigInt</p></td>
<td><p>16</p></td>
<td><p>Большие объемы данных Integer</p></td>
</tr>
<tr class="odd">
<td><p>dbBinary</p></td>
<td><p>9</p></td>
<td><p>Двоичные данные</p></td>
</tr>
<tr class="even">
<td><p>dbBoolean</p></td>
<td><p>1</p></td>
<td><p>Данных Boolean (ИСТИНА/ЛОЖЬ)</p></td>
</tr>
<tr class="odd">
<td><p>dbByte</p></td>
<td><p>2</p></td>
<td><p>Данные (8 бит)</p></td>
</tr>
<tr class="even">
<td><p>dbChar</p></td>
<td><p>18</p></td>
<td><p>Текстовые данные (Фиксированная ширина)</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexByte</p></td>
<td><p>102</p></td>
<td><p>Многозначные байтов данных</p></td>
</tr>
<tr class="even">
<td><p>dbComplexDecimal</p></td>
<td><p>108</p></td>
<td><p>Многозначный данных decimal</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexDouble</p></td>
<td><p>106</p></td>
<td><p>Многозначный данных с плавающей запятой двойной точности</p></td>
</tr>
<tr class="even">
<td><p>dbComplexGUID</p></td>
<td><p>107</p></td>
<td><p>Многозначный GUID данных</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexInteger</p></td>
<td><p>103</p></td>
<td><p>Целое число Многозначный данных</p></td>
</tr>
<tr class="even">
<td><p>dbComplexLong</p></td>
<td><p>104</p></td>
<td><p>Длинное целое Многозначный данных</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexSingle</p></td>
<td><p>105</p></td>
<td><p>Многозначный данных с плавающей запятой одиночной точности</p></td>
</tr>
<tr class="even">
<td><p>dbComplexText</p></td>
<td><p>109</p></td>
<td><p>Многозначный текстовые данные (переменной ширины)</p></td>
</tr>
<tr class="odd">
<td><p>dbCurrency</p></td>
<td><p>5</p></td>
<td><p>Данных валюты</p></td>
</tr>
<tr class="even">
<td><p>dbDate</p></td>
<td><p>8</p></td>
<td><p>Данные значения даты</p></td>
</tr>
<tr class="odd">
<td><p>dbDecimal</p></td>
<td><p>20</p></td>
<td><p>Данных decimal (технология ODBCDirect только)</p><p><strong>Примечание</strong>: технология ODBCDirect рабочие области, не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</p>
</td>
</tr>
<tr class="even">
<td><p>dbDouble</p></td>
<td><p>7</p></td>
<td><p>Данные с плавающей запятой двойной точности</p></td>
</tr>
<tr class="odd">
<td><p>dbFloat</p></td>
<td><p>21</p></td>
<td><p>Данных с плавающей запятой (технология ODBCDirect только)</p>

<br/>


</td>
</tr>
<tr class="even">
<td><p>dbGUID</p></td>
<td><p>15</p></td>
<td><p>Идентификатор GUID данных</p></td>
</tr>
<tr class="odd">
<td><p>dbInteger</p></td>
<td><p>3</p></td>
<td><p>Целое число данных</p></td>
</tr>
<tr class="even">
<td><p>dbLong</p></td>
<td><p>4</p></td>
<td><p>Длинное целое число данных</p></td>
</tr>
<tr class="odd">
<td><p>dbLongBinary</p></td>
<td><p>11</p></td>
<td><p>Двоичные данные (растровое изображение)</p></td>
</tr>
<tr class="even">
<td><p>dbMemo</p></td>
<td><p>12</p></td>
<td><p>Заметка данных (расширенный текст)</p></td>
</tr>
<tr class="odd">
<td><p>dbNumeric</p></td>
<td><p>19</p></td>
<td><p>Числовые данные (технология ODBCDirect только)</p>

<br/>


</td>
</tr>
<tr class="even">
<td><p>dbSingle</p></td>
<td><p>6</p></td>
<td><p>Данные с плавающей запятой одиночной точности</p></td>
</tr>
<tr class="odd">
<td><p>dbText</p></td>
<td><p>10</p></td>
<td><p>Текстовые данные (переменной ширины)</p></td>
</tr>
<tr class="even">
<td><p>dbTime</p></td>
<td><p>22</p></td>
<td><p>Данные в формате времени (технология ODBCDirect только)</p>

<br/>


</td>
</tr>
<tr class="odd">
<td><p>dbTimeStamp</p></td>
<td><p>23</p></td>
<td><p>Данные в формат даты и времени (технология ODBCDirect только)</p>

<br/>


</td>
</tr>
<tr class="even">
<td><p>dbVarBinary</p></td>
<td><p>17</p></td>
<td><p>Двоичные данные переменной (технология ODBCDirect только)</p>

<br/>


</td>
</tr>
</tbody>
</table>


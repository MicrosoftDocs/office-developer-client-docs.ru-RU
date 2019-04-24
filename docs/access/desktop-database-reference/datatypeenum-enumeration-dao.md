---
title: Перечисление DataTypeEnum (DAO)
TOCTitle: DataTypeEnum Enumeration
ms:assetid: 59ead483-52fc-53cd-02e6-084814f961ac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194420(v=office.15)
ms:contentKeyID: 48545028
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 499513d706b254e72433d37d4eb5452ccbbaa257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294451"
---
# <a name="datatypeenum-enumeration-dao"></a>Перечисление DataTypeEnum (DAO)


**Область применения**: Access 2013, Office 2013

Задает тип рабочих данных для объекта.

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
<td><p>Большие целочисленные данные</p></td>
</tr>
<tr class="odd">
<td><p>dbBinary</p></td>
<td><p>9</p></td>
<td><p>Двоичные данные</p></td>
</tr>
<tr class="even">
<td><p>dbBoolean</p></td>
<td><p>1</p></td>
<td><p>Логические данные (ИСТИНА/ЛОЖЬ)</p></td>
</tr>
<tr class="odd">
<td><p>dbByte</p></td>
<td><p>2</p></td>
<td><p>Данные в форме байтов (8-битных)</p></td>
</tr>
<tr class="even">
<td><p>dbChar</p></td>
<td><p>18</p></td>
<td><p>Текстовые данные (фиксированная ширина)</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexByte</p></td>
<td><p>102</p></td>
<td><p>Многозначные данные в форме байтов</p></td>
</tr>
<tr class="even">
<td><p>dbComplexDecimal</p></td>
<td><p>108</p></td>
<td><p>Многозначные десятичные данные</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexDouble</p></td>
<td><p>106</p></td>
<td><p>Многозначные данные с плавающей запятой двойной точности</p></td>
</tr>
<tr class="even">
<td><p>dbComplexGUID</p></td>
<td><p>107</p></td>
<td><p>Многозначные GUID данные</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexInteger</p></td>
<td><p>103</p></td>
<td><p>Многозначные целочисленные данные</p></td>
</tr>
<tr class="even">
<td><p>dbComplexLong</p></td>
<td><p>104</p></td>
<td><p>Многозначные длинные целочисленные данные</p></td>
</tr>
<tr class="odd">
<td><p>dbComplexSingle</p></td>
<td><p>105</p></td>
<td><p>Многозначные данные с плавающей запятой одиночной точности</p></td>
</tr>
<tr class="even">
<td><p>dbComplexText</p></td>
<td><p>109</p></td>
<td><p>Многозначные текстовые данные (переменной ширины)</p></td>
</tr>
<tr class="odd">
<td><p>dbCurrency</p></td>
<td><p>5</p></td>
<td><p>Данныхтипа "Валюта"</p></td>
</tr>
<tr class="even">
<td><p>dbDate</p></td>
<td><p>8</p></td>
<td><p>Данные значения даты</p></td>
</tr>
<tr class="odd">
<td><p>dbDecimal</p></td>
<td><p>20</p></td>
<td><p>Десятичные данные (только для ODBCDirect)</p><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
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
<td><p>Данные с плавающей запятой (только для ODBCDirect)</p>

<br/>


</td>
</tr>
<tr class="even">
<td><p>dbGUID</p></td>
<td><p>15</p></td>
<td><p>GUID данные</p></td>
</tr>
<tr class="odd">
<td><p>dbInteger</p></td>
<td><p>3</p></td>
<td><p>Целочисленные данные</p></td>
</tr>
<tr class="even">
<td><p>dbLong</p></td>
<td><p>4</p></td>
<td><p>Длинные целочисленные данные</p></td>
</tr>
<tr class="odd">
<td><p>dbLongBinary</p></td>
<td><p>11</p></td>
<td><p>Двоичные данные (bitmap)</p></td>
</tr>
<tr class="even">
<td><p>dbMemo</p></td>
<td><p>12</p></td>
<td><p>Данные MEMO (расширенный текст)</p></td>
</tr>
<tr class="odd">
<td><p>dbNumeric</p></td>
<td><p>19</p></td>
<td><p>Числовые данные (только для ODBCDirect)</p>

<br/>


</td>
</tr>
<tr class="even">
<td><p>dbSingle</p></td>
<td><p>6</p></td>
<td><p>Данные с плавающей запятой одинарной точности</p></td>
</tr>
<tr class="odd">
<td><p>dbText</p></td>
<td><p>10</p></td>
<td><p>Текстовые данные (переменной ширины)</p></td>
</tr>
<tr class="even">
<td><p>dbTime</p></td>
<td><p>22</p></td>
<td><p>Данные в формате времени (только для ODBCDirect)</p>

<br/>


</td>
</tr>
<tr class="odd">
<td><p>dbTimeStamp</p></td>
<td><p>23</p></td>
<td><p>Данные в формате времени и даты (только для ODBCDirect)</p>

<br/>


</td>
</tr>
<tr class="even">
<td><p>dbVarBinary</p></td>
<td><p>17</p></td>
<td><p>Переменные двоичные данные (только для ODBCDirect)</p>

<br/>


</td>
</tr>
</tbody>
</table>


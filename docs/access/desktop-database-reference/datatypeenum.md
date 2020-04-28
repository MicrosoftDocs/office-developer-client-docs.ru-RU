---
title: DataTypeEnum (Справочник по базам данных Access на компьютере)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ffba234ed1c5dc56138a665d6dd07038f55da7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294444"
---
# <a name="datatypeenum"></a>DataTypeEnum

**Область применения**: Access 2013, Office 2013

Указывает тип данных [поля](field-object-ado.md), [параметра](parameter-object-ado.md)или [Свойства](property-object-ado.md). Соответствующий индикатор типа OLE DB отображается в круглых скобках в столбце Описание следующей таблицы. Дополнительные сведения о типах данных OLE DB приведены в главе 13 и приложении A *Справочника программиста OLE DB*.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>адаррай<br />
</strong>(Не применяется к ADOX.)</p></td>
<td><p>0x2000</p></td>
<td><p>Значение флага, всегда скомбинированное с другой константой типа данных, которое указывает массив другого типа данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>адбигинт</strong></p></td>
<td><p>двадцать</p></td>
<td><p>Указывает 8-разрядное целое число со знаком (DBTYPE_I8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>адбинари</strong></p></td>
<td><p>128</p></td>
<td><p>Указывает двоичное значение (DBTYPE_BYTES).</p></td>
</tr>
<tr class="even">
<td><p><strong>адбулеан</strong></p></td>
<td><p>11 </p></td>
<td><p>Указывает логическое значение (DBTYPE_BOOL).</p></td>
</tr>
<tr class="odd">
<td><p><strong>адбстр</strong></p></td>
<td><p>8 </p></td>
<td><p>Указывает строку символов (Юникод), заканчивающуюся нулем (DBTYPE_BSTR).</p></td>
</tr>
<tr class="even">
<td><p><strong>адчаптер</strong></p></td>
<td><p>136</p></td>
<td><p>Указывает значение главы из четырех байт, которое определяет строки в дочернем наборе строк (DBTYPE_HCHAPTER).</p></td>
</tr>
<tr class="odd">
<td><p><strong>адчар</strong></p></td>
<td><p>129</p></td>
<td><p>Указывает строковое значение (DBTYPE_STR).</p></td>
</tr>
<tr class="even">
<td><p><strong>адкурренци</strong></p></td>
<td><p>6 </p></td>
<td><p>Показывает значение валюты (DBTYPE_CY). Currency — это число с фиксированной запятой, сопоставленное с четырьмя цифрами справа от десятичной точки. Он хранится в виде целого числа со знаком длиной 8 байт, масштабированное на 10 000.</p></td>
</tr>
<tr class="odd">
<td><p><strong>аддате</strong></p></td>
<td><p>7 </p></td>
<td><p>Указывает значение даты (DBTYPE_DATE). Дата хранится в виде Double, целой части, которая представляет собой количество дней с 30 декабря 1899 г., и дробная часть, представляющая долю дня.</p></td>
</tr>
<tr class="even">
<td><p><strong>аддбдате</strong></p></td>
<td><p>133</p></td>
<td><p>Указывает значение даты (DBTYPE_DBDATE).</p></td>
</tr>
<tr class="odd">
<td><p><strong>аддбтиме</strong></p></td>
<td><p>134</p></td>
<td><p>Указывает значение времени (ЧЧММСС) (DBTYPE_DBTIME).</p></td>
</tr>
<tr class="even">
<td><p><strong>аддбтиместамп</strong></p></td>
<td><p>135</p></td>
<td><p>Указывает отметку даты и времени (ГГГГММДДЧЧММСС плюс дробь в биллионсс) (DBTYPE_DBTIMESTAMP).</p></td>
</tr>
<tr class="odd">
<td><p><strong>аддеЦимал</strong></p></td>
<td><p>14 </p></td>
<td><p>Указывает точное числовое значение с фиксированной точностью и масштабом (DBTYPE_DECIMAL).</p></td>
</tr>
<tr class="even">
<td><p><strong>аддаубле</strong></p></td>
<td><p>5 </p></td>
<td><p>Указывает значение двойной точности с плавающей запятой (DBTYPE_R8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>адемпти</strong></p></td>
<td><p>нуль</p></td>
<td><p>Значение не задано (DBTYPE_EMPTY).</p></td>
</tr>
<tr class="even">
<td><p><strong>адеррор</strong></p></td>
<td><p>10 </p></td>
<td><p>Указывает 32-разрядный код ошибки (DBTYPE_ERROR).</p></td>
</tr>
<tr class="odd">
<td><p><strong>адфилетиме</strong></p></td>
<td><p>64</p></td>
<td><p>Указывает 64-разрядное значение, представляющее количество интервалов 100-наносекундных с 1 января 1601 г. (DBTYPE_FILETIME).</p></td>
</tr>
<tr class="even">
<td><p><strong>адгуид</strong></p></td>
<td><p>72</p></td>
<td><p>Указывает глобальный уникальный идентификатор (GUID) (DBTYPE_GUID).</p></td>
</tr>
<tr class="odd">
<td><p><strong>адидиспатч</strong></p></td>
<td><p>9 </p></td>
<td><p>Показывает указатель на интерфейс <strong>IDispatch</strong> объекта COM (DBTYPE_IDISPATCH).</p><p><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO. Использование может привести к непредсказуемым результатам.</p>
</td>
</tr>
<tr class="even">
<td><p><strong>адинтежер</strong></p></td>
<td><p>4</p></td>
<td><p>Указывает 4-разрядное целое число со знаком (DBTYPE_I4).</p></td>
</tr>
<tr class="odd">
<td><p><strong>адиункновн</strong></p></td>
<td><p>13</p></td>
<td><p>Показывает указатель на интерфейс <strong>IUnknown</strong> для объекта COM (DBTYPE_IUNKNOWN).</p><p><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO. Использование может привести к непредсказуемым результатам.
</p></td>
</tr>
<tr class="even">
<td><p><strong>адлонгварбинари</strong></p></td>
<td><p>205</p></td>
<td><p>Указывает длинное двоичное значение.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адлонгварчар</strong></p></td>
<td><p>201</p></td>
<td><p>Указывает длинное строковое значение.</p></td>
</tr>
<tr class="even">
<td><p><strong>адлонгварвчар</strong></p></td>
<td><p>203</p></td>
<td><p>Указывает длинное строковое значение Юникода с завершающим нулем.</p></td>
</tr>
<tr class="odd">
<td><p><strong>аднумерик</strong></p></td>
<td><p>131</p></td>
<td><p>Указывает точное числовое значение с фиксированной точностью и масштабом (DBTYPE_NUMERIC).</p></td>
</tr>
<tr class="even">
<td><p><strong>адпропвариант</strong></p></td>
<td><p>138</p></td>
<td><p>Указывает ПРОПВАРИАНТ автоматизации (DBTYPE_PROP_VARIANT).</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсингле</strong></p></td>
<td><p>4 </p></td>
<td><p>Показывает значение одиночной точности с плавающей запятой (DBTYPE_R4).</p></td>
</tr>
<tr class="even">
<td><p><strong>адсмаллинт</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает 2-байтовое целое число со знаком (DBTYPE_I2).</p></td>
</tr>
<tr class="odd">
<td><p><strong>адтининт</strong></p></td>
<td><p>16 </p></td>
<td><p>Указывает Однобайтовое целое со знаком (DBTYPE_I1).</p></td>
</tr>
<tr class="even">
<td><p><strong>адунсигнедбигинт</strong></p></td>
<td><p>21</p></td>
<td><p>Указывает целое число без знака длиной 8 байт (DBTYPE_UI8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>адунсигнединт</strong></p></td>
<td><p>19</p></td>
<td><p>Указывает целое число без знака длиной 4 байта (DBTYPE_UI4).</p></td>
</tr>
<tr class="even">
<td><p><strong>адунсигнедсмаллинт</strong></p></td>
<td><p>18 </p></td>
<td><p>Указывает на неподписанное 2-разрядное целое число (DBTYPE_UI2).</p></td>
</tr>
<tr class="odd">
<td><p><strong>адунсигнедтининт</strong></p></td>
<td><p>17 </p></td>
<td><p>Указывает Однобайтовое целое число без знака (DBTYPE_UI1).</p></td>
</tr>
<tr class="even">
<td><p><strong>адусердефинед</strong></p></td>
<td><p>132</p></td>
<td><p>Указывает пользовательскую переменную (DBTYPE_UDT).</p></td>
</tr>
<tr class="odd">
<td><p><strong>адварбинари</strong></p></td>
<td><p>204</p></td>
<td><p>Указывает двоичное значение (только для объекта<strong>Parameter</strong> ).</p></td>
</tr>
<tr class="even">
<td><p><strong>адварчар</strong></p></td>
<td><p>200</p></td>
<td><p>Указывает строковое значение.</p></td>
</tr>
<tr class="odd">
<td><p><strong>адвариант</strong></p></td>
<td><p>12 </p></td>
<td><p>Указывает на <strong>вариант</strong> автоматизации (DBTYPE_VARIANT).</p><p><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO. Использование может привести к непредсказуемым результатам.</p></td>
</tr>
<tr class="even">
<td><p><strong>адварнумерик</strong></p></td>
<td><p>139</p></td>
<td><p>Указывает числовое значение (только для объекта<strong>Parameter</strong> ).</p></td>
</tr>
<tr class="odd">
<td><p><strong>адварвчар</strong></p></td>
<td><p>202</p></td>
<td><p>Указывает строку символов Юникода, заканчивающуюся нулем.</p></td>
</tr>
<tr class="even">
<td><p><strong>адвчар</strong></p></td>
<td><p>130</p></td>
<td><p>Указывает строку символов Юникода, заканчивающуюся нулем (DBTYPE_WSTR).</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com. MS. WFC. Data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Адоенумс. DataType. ARRAY</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. BIGINT</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. BINARY</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. BOOLEAN</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. BSTR</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. CHAPTER</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. CHAR</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. CURRENCY</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. DATE</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. ДБДАТЕ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. ДБТИМЕ</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. ДБТИМЕСТАМП</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. DECIMAL</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. DOUBLE</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. EMPTY</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. ERROR</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. FILETIME</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. GUID</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. IDISPATCH</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. INTEGER</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. IUNKNOWN</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. ЛОНГВАРБИНАРИ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. ЛОНГВАРЧАР</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. ЛОНГВАРВЧАР</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. NUMERIC</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. ПРОПВАРИАНТ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. SINGLE</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. SMALLINT</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. TINYINT</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. УНСИГНЕДБИГИНТ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. УНСИГНЕДИНТ</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. УНСИГНЕДСМАЛЛИНТ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. УНСИГНЕДТИНИНТ</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. USERDEFINED типа</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. VARBINARY</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. VARCHAR</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. VARIANT</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. ВАРНУМЕРИК</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. DataType. ВАРВЧАР</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. DataType. WCHAR</p></td>
</tr>
</tbody>
</table>


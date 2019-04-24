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
<td><p><strong>Адаррай<br />
</strong>(Не применяется к ADOX.)</p></td>
<td><p>0x2000</p></td>
<td><p>Значение флага, всегда скомбинированное с другой константой типа данных, которое указывает массив другого типа данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адбигинт</strong></p></td>
<td><p>двадцать</p></td>
<td><p>Указывает 8-разрядное целое число со знаком (DBTYPE_I8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адбинари</strong></p></td>
<td><p>128</p></td>
<td><p>Указывает двоичное значение (ДБТИПЕ_БИТЕС).</p></td>
</tr>
<tr class="even">
<td><p><strong>Адбулеан</strong></p></td>
<td><p>-11:00</p></td>
<td><p>Указывает логическое значение (ДБТИПЕ_БУЛ).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адбстр</strong></p></td>
<td><p>8,5</p></td>
<td><p>Указывает строку символов (Юникод), заканчивающуюся нулем (ДБТИПЕ_БСТР).</p></td>
</tr>
<tr class="even">
<td><p><strong>Адчаптер</strong></p></td>
<td><p>136</p></td>
<td><p>Указывает значение главы из четырех байт, которое определяет строки в дочернем наборе строк (ДБТИПЕ_ХЧАПТЕР).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адчар</strong></p></td>
<td><p>129</p></td>
<td><p>Указывает строковое значение (ДБТИПЕ_СТР).</p></td>
</tr>
<tr class="even">
<td><p><strong>Адкурренци</strong></p></td>
<td><p>ICMPv6</p></td>
<td><p>Показывает значение валюты (ДБТИПЕ_ЦИ). Currency — это число с фиксированной запятой, сопоставленное с четырьмя цифрами справа от десятичной точки. Он хранится в виде целого числа со знаком длиной 8 байт, масштабированное на 10 000.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Аддате</strong></p></td>
<td><p>см</p></td>
<td><p>Указывает значение даты (ДБТИПЕ_ДАТЕ). Дата хранится в виде Double, целой части, которая представляет собой количество дней с 30 декабря 1899 г., и дробная часть, представляющая долю дня.</p></td>
</tr>
<tr class="even">
<td><p><strong>Аддбдате</strong></p></td>
<td><p>133</p></td>
<td><p>Указывает значение даты (ГГГГММДД) (ДБТИПЕ_ДБДАТЕ).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Аддбтиме</strong></p></td>
<td><p>134</p></td>
<td><p>Указывает значение времени (ЧЧММСС) (ДБТИПЕ_ДБТИМЕ).</p></td>
</tr>
<tr class="even">
<td><p><strong>Аддбтиместамп</strong></p></td>
<td><p>135</p></td>
<td><p>Указывает отметку даты и времени (ГГГГММДДЧЧММСС плюс дробь в биллионсс) (ДБТИПЕ_ДБТИМЕСТАМП).</p></td>
</tr>
<tr class="odd">
<td><p><strong>АддеЦимал</strong></p></td>
<td><p>14</p></td>
<td><p>Указывает точное числовое значение с фиксированной точностью и масштабом (ДБТИПЕ_ДЕЦИМАЛ).</p></td>
</tr>
<tr class="even">
<td><p><strong>Аддаубле</strong></p></td>
<td><p>17:00</p></td>
<td><p>Указывает значение удвоенной точности с плавающей запятой (DBTYPE_R8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адемпти</strong></p></td>
<td><p>нуль</p></td>
<td><p>Задает значение No (ДБТИПЕ_ЕМПТИ).</p></td>
</tr>
<tr class="even">
<td><p><strong>Адеррор</strong></p></td>
<td><p>десяти</p></td>
<td><p>Указывает 32-разрядный код ошибки (ДБТИПЕ_ЕРРОР).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адфилетиме</strong></p></td>
<td><p>64</p></td>
<td><p>Указывает 64-разрядное значение, представляющее количество интервалов 100-наносекундных, начиная с 1 января 1601 (ДБТИПЕ_ФИЛЕТИМЕ).</p></td>
</tr>
<tr class="even">
<td><p><strong>Адгуид</strong></p></td>
<td><p>72</p></td>
<td><p>Указывает глобальный уникальный идентификатор (GUID) (ДБТИПЕ_ГУИД).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адидиспатч</strong></p></td>
<td><p>10</p></td>
<td><p>Показывает указатель на интерфейс <strong>IDispatch</strong> объекта COM (дбтипе_идиспатч).</p><p><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO. Использование может привести к непредсказуемым результатам.</p>
</td>
</tr>
<tr class="even">
<td><p><strong>Адинтежер</strong></p></td>
<td><p>4</p></td>
<td><p>Указывает 4-разрядное целое число со знаком (DBTYPE_I4).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адиункновн</strong></p></td>
<td><p>13</p></td>
<td><p>Показывает указатель на интерфейс <strong>IUnknown</strong> для объекта COM (дбтипе_иункновн).</p><p><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO. Использование может привести к непредсказуемым результатам.
</p></td>
</tr>
<tr class="even">
<td><p><strong>Адлонгварбинари</strong></p></td>
<td><p>205</p></td>
<td><p>Указывает длинное двоичное значение.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адлонгварчар</strong></p></td>
<td><p>201</p></td>
<td><p>Указывает длинное строковое значение.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адлонгварвчар</strong></p></td>
<td><p>203</p></td>
<td><p>Указывает длинное строковое значение Юникода с завершающим нулем.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Аднумерик</strong></p></td>
<td><p>131</p></td>
<td><p>Указывает точное числовое значение с фиксированной точностью и масштабом (ДБТИПЕ_НУМЕРИК).</p></td>
</tr>
<tr class="even">
<td><p><strong>Адпропвариант</strong></p></td>
<td><p>138</p></td>
<td><p>Указывает ПРОПВАРИАНТ автоматизации (ДБТИПЕ_ПРОП_ВАРИАНТ).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адсингле</strong></p></td>
<td><p>SP4</p></td>
<td><p>Показывает значение одиночной точности с плавающей запятой (DBTYPE_R4).</p></td>
</tr>
<tr class="even">
<td><p><strong>Адсмаллинт</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает 2-байтовое целое число со знаком (DBTYPE_I2).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адтининт</strong></p></td>
<td><p>столбцов</p></td>
<td><p>Указывает Однобайтовое целое со знаком (DBTYPE_I1).</p></td>
</tr>
<tr class="even">
<td><p><strong>Адунсигнедбигинт</strong></p></td>
<td><p>21</p></td>
<td><p>Указывает 8-байтовое целое число без знака (DBTYPE_UI8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адунсигнединт</strong></p></td>
<td><p>19</p></td>
<td><p>Указывает на значение из четырех байтов без знака (DBTYPE_UI4).</p></td>
</tr>
<tr class="even">
<td><p><strong>Адунсигнедсмаллинт</strong></p></td>
<td><p>0,18</p></td>
<td><p>Указывает на 2-байтовое целое число без знака (DBTYPE_UI2).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адунсигнедтининт</strong></p></td>
<td><p>17</p></td>
<td><p>Указывает Однобайтовое целое число без знака (DBTYPE_UI1).</p></td>
</tr>
<tr class="even">
<td><p><strong>Адусердефинед</strong></p></td>
<td><p>132</p></td>
<td><p>Указывает пользовательскую переменную (ДБТИПЕ_УДТ).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адварбинари</strong></p></td>
<td><p>204</p></td>
<td><p>Указывает двоичное значение (только для объекта<strong>Parameter</strong> ).</p></td>
</tr>
<tr class="even">
<td><p><strong>Адварчар</strong></p></td>
<td><p>200</p></td>
<td><p>Указывает строковое значение.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адвариант</strong></p></td>
<td><p>12</p></td>
<td><p>Указывает <strong>вариант</strong> автоматизации (дбтипе_вариант).</p><p><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO. Использование может привести к непредсказуемым результатам.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адварнумерик</strong></p></td>
<td><p>139</p></td>
<td><p>Указывает числовое значение (только для объекта<strong>Parameter</strong> ).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адварвчар</strong></p></td>
<td><p>202</p></td>
<td><p>Указывает строку символов Юникода, заканчивающуюся нулем.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адвчар</strong></p></td>
<td><p>130</p></td>
<td><p>Указывает строку символов Юникода, заканчивающуюся нулем (ДБТИПЕ_ВСТР).</p></td>
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


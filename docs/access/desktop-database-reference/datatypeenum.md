---
title: DataTypeEnum (Справочник по для настольных баз данных Access)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: f5c192589f2c90b2ce7b6c7b376b80c92b341e2d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860660"
---
# <a name="datatypeenum"></a>DataTypeEnum

**Применимо к**: Access 2013 | Office 2013

Указывает тип данных [параметра](parameter-object-ado.md), [поля](field-object-ado.md)или [Свойства](property-object-ado.md). В скобки в столбце Описание в следующей таблице показан соответствующий индикатор типа OLE DB. Дополнительные сведения о типах данных OLE DB видеть главе 13 и приложение A *Справочник программиста OLE DB*.

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
<td><p><strong>AdArray<br />
</strong>(Не применяется к ADOX.)</p></td>
<td><p>0x2000</p></td>
<td><p>Значение флага, всегда вместе с другой тип данных константа, которая указывает массив, другой тип данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adBigInt</strong></p></td>
<td><p>20</p></td>
<td><p>Указывает целое число 8 байт со знаком (DBTYPE_I8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adBinary</strong></p></td>
<td><p>128</p></td>
<td><p>Указывает двоичное значение (DBTYPE_BYTES).</p></td>
</tr>
<tr class="even">
<td><p><strong>adBoolean</strong></p></td>
<td><p>11</p></td>
<td><p>Указывает логическое значение (DBTYPE_BOOL).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adBSTR</strong></p></td>
<td><p>8</p></td>
<td><p>Указывает строку символом null знаков (Юникод) (DBTYPE_BSTR).</p></td>
</tr>
<tr class="even">
<td><p><strong>adChapter</strong></p></td>
<td><p>136</p></td>
<td><p>Указывает, Глава 4 байтовое значение, указывающее строки в дочерних строк (DBTYPE_HCHAPTER).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adChar</strong></p></td>
<td><p>129</p></td>
<td><p>Указывает значение string (DBTYPE_STR).</p></td>
</tr>
<tr class="even">
<td><p><strong>adCurrency</strong></p></td>
<td><p>6</p></td>
<td><p>Указывает значение валюты (DBTYPE_CY). Валюта является фиксированной числа с четырех цифр справа от десятичной запятой. Он хранится в 8 байтовое целое число со знаком, масштабируемые с 10 000.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adDate</strong></p></td>
<td><p>7</p></td>
<td><p>Указывает значение даты (DBTYPE_DATE). Дата сохраняется как значение типа double, всей часть из которых — число дней, прошедших с 30 декабря 1899, а дробная часть из которых — долю дня.</p></td>
</tr>
<tr class="even">
<td><p><strong>adDBDate</strong></p></td>
<td><p>133</p></td>
<td><p>Указывает значение даты (ГГГГММДД) (DBTYPE_DBDATE).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adDBTime</strong></p></td>
<td><p>134</p></td>
<td><p>Указывает значение времени (ЧЧММСС) (DBTYPE_DBTIME).</p></td>
</tr>
<tr class="even">
<td><p><strong>adDBTimeStamp</strong></p></td>
<td><p>135</p></td>
<td><p>Указывает метку даты/времени (ггггммддччммсс плюс дроби в billionths) (DBTYPE_DBTIMESTAMP).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adDecimal</strong></p></td>
<td><p>14</p></td>
<td><p>Указывает точное числовое значение с фиксированной точности и масштаба (DBTYPE_DECIMAL).</p></td>
</tr>
<tr class="even">
<td><p><strong>adDouble</strong></p></td>
<td><p>5</p></td>
<td><p>Указывает значение с плавающей запятой двойной точности (DBTYPE_R8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adEmpty</strong></p></td>
<td><p>0</p></td>
<td><p>Не заданы значения (DBTYPE_EMPTY).</p></td>
</tr>
<tr class="even">
<td><p><strong>adError</strong></p></td>
<td><p>10</p></td>
<td><p>Указывает код ошибки 32-разрядная версия (DBTYPE_ERROR).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFileTime</strong></p></td>
<td><p>64</p></td>
<td><p>Указывает значение 64-разрядная версия, представляющее количество 100 наносекунд интервалов с 1 января 1601 г. (DBTYPE_FILETIME).</p></td>
</tr>
<tr class="even">
<td><p><strong>adGUID</strong></p></td>
<td><p>72</p></td>
<td><p>Указывает глобальный уникальный идентификатор (GUID) (DBTYPE_GUID).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIDispatch</strong></p></td>
<td><p>9</p></td>
<td><p>Обозначает указатель на интерфейс <strong>IDispatch</strong> на COM-объект (DBTYPE_IDISPATCH).</p><p><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO. Применение может привести к непредсказуемым последствиям.</p>
</td>
</tr>
<tr class="even">
<td><p><strong>adInteger</strong></p></td>
<td><p>3</p></td>
<td><p>Указывает 4 байта целого числа со знаком (DBTYPE_I4).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIUnknown</strong></p></td>
<td><p>13</p></td>
<td><p>Указывает указатель на интерфейс <strong>IUnknown</strong> COM-объект (DBTYPE_IUNKNOWN).</p><p><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO. Применение может привести к непредсказуемым последствиям.
</p></td>
</tr>
<tr class="even">
<td><p><strong>adLongVarBinary</strong></p></td>
<td><p>205</p></td>
<td><p>Указывает Длинное двоичное значение.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adLongVarChar</strong></p></td>
<td><p>201</p></td>
<td><p>Указывает значение длинной строкой.</p></td>
</tr>
<tr class="even">
<td><p><strong>adLongVarWChar</strong></p></td>
<td><p>203</p></td>
<td><p>Указывает значение строки Юникод долго символом null.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adNumeric</strong></p></td>
<td><p>131</p></td>
<td><p>Указывает точное числовое значение с фиксированной точности и масштаба (DBTYPE_NUMERIC).</p></td>
</tr>
<tr class="even">
<td><p><strong>adPropVariant</strong></p></td>
<td><p>138</p></td>
<td><p>Указывает автоматизация PROPVARIANT (DBTYPE_PROP_VARIANT).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSingle</strong></p></td>
<td><p>4</p></td>
<td><p>Указывает значение с плавающей запятой одиночной точности (DBTYPE_R4).</p></td>
</tr>
<tr class="even">
<td><p><strong>adSmallInt</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает двухбайтовые целого числа со знаком (DBTYPE_I2).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adTinyInt</strong></p></td>
<td><p>16</p></td>
<td><p>Указывает один байт целого числа со знаком (DBTYPE_I1).</p></td>
</tr>
<tr class="even">
<td><p><strong>adUnsignedBigInt</strong></p></td>
<td><p>21</p></td>
<td><p>Указывает, 8 байтовое целое (DBTYPE_UI8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUnsignedInt</strong></p></td>
<td><p>19</p></td>
<td><p>Указывает, 4 байтовое целое число без знака (DBTYPE_UI4).</p></td>
</tr>
<tr class="even">
<td><p><strong>adUnsignedSmallInt</strong></p></td>
<td><p>18</p></td>
<td><p>Указывает, 2 байтовое целое число без знака (DBTYPE_UI2).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUnsignedTinyInt</strong></p></td>
<td><p>17</p></td>
<td><p>Указывает один байтовое целое число без знака (DBTYPE_UI1).</p></td>
</tr>
<tr class="even">
<td><p><strong>adUserDefined</strong></p></td>
<td><p>132</p></td>
<td><p>Указывает, определенные пользователем переменные (DBTYPE_UDT).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adVarBinary</strong></p></td>
<td><p>204</p></td>
<td><p>Указывает двоичное значение (только для<strong>параметра</strong> объект).</p></td>
</tr>
<tr class="even">
<td><p><strong>adVarChar</strong></p></td>
<td><p>200</p></td>
<td><p>Указывает значение строки.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adVariant</strong></p></td>
<td><p>12</p></td>
<td><p>Указывает, автоматизации <strong>Variant</strong> (DBTYPE_VARIANT).</p><p><strong>Примечание</strong>: этот тип данных в настоящее время не поддерживается ADO. Применение может привести к непредсказуемым последствиям.</p></td>
</tr>
<tr class="even">
<td><p><strong>adVarNumeric</strong></p></td>
<td><p>139</p></td>
<td><p>Указывает числовое значение (только для<strong>параметра</strong> объект).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adVarWChar</strong></p></td>
<td><p>202</p></td>
<td><p>Указывает строку знаков Юникод символом null.</p></td>
</tr>
<tr class="even">
<td><p><strong>adWChar</strong></p></td>
<td><p>130</p></td>
<td><p>Указывает строку знаков Юникод (DBTYPE_WSTR) символом null.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.DataType.ARRAY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.BIGINT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.BINARY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.BOOLEAN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.BSTR</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.CHAPTER</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.CHAR</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.CURRENCY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.DATE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.DBDATE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.DBTIME</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.DBTIMESTAMP</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.DECIMAL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.DOUBLE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.EMPTY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.ERROR</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.FILETIME</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.GUID</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.IDISPATCH</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.INTEGER</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.IUNKNOWN</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.LONGVARBINARY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.LONGVARCHAR</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.LONGVARWCHAR</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.NUMERIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.PROPVARIANT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.SINGLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.SMALLINT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.TINYINT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.UNSIGNEDBIGINT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.UNSIGNEDINT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.UNSIGNEDSMALLINT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.UNSIGNEDTINYINT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.USERDEFINED</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.VARBINARY</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.VARCHAR</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.VARIANT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.VARNUMERIC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.DataType.VARWCHAR</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.DataType.WCHAR</p></td>
</tr>
</tbody>
</table>


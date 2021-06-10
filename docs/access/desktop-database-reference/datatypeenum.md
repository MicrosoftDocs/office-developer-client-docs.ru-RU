---
title: DataTypeEnum (Ссылка на настольные базы данных)
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

Указывает тип данных [поля,](field-object-ado.md) [параметра](parameter-object-ado.md)или [свойства.](property-object-ado.md) Соответствующий индикатор типа OLE DB показан в скобки в столбце описания следующей таблицы. Дополнительные сведения о типах данных OLE DB см. в главе 13 и приложении A справочника программиста *OLE DB.*

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
<td><p>Значение флага, всегда в сочетании с константой другого типа данных, указывает массив этого другого типа данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>adBigInt</strong></p></td>
<td><p>20</p></td>
<td><p>Указывает на подписанный в восемь byte integer (DBTYPE_I8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adBinary</strong></p></td>
<td><p>128</p></td>
<td><p>Указывает двоичное значение (DBTYPE_BYTES).</p></td>
</tr>
<tr class="even">
<td><p><strong>adBoolean</strong></p></td>
<td><p>11</p></td>
<td><p>Указывает значение boolean (DBTYPE_BOOL).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adBSTR</strong></p></td>
<td><p>8 </p></td>
<td><p>Указывает null-terminated character string (Unicode) (DBTYPE_BSTR).</p></td>
</tr>
<tr class="even">
<td><p><strong>adChapter</strong></p></td>
<td><p>136</p></td>
<td><p>Указывает значение главы с четырьмя byte, которое определяет строки в детском наборе строк (DBTYPE_HCHAPTER).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adChar</strong></p></td>
<td><p>129</p></td>
<td><p>Указывает значение строки (DBTYPE_STR).</p></td>
</tr>
<tr class="even">
<td><p><strong>adCurrency</strong></p></td>
<td><p>6 </p></td>
<td><p>Указывает значение валюты (DBTYPE_CY). Валюта — это номер фиксированной точки с четырьмя цифрами справа от десятичной точки. Он хранится в подписанном на восемь byte integer масштабе 10 000.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adDate</strong></p></td>
<td><p>7 </p></td>
<td><p>Указывает значение даты (DBTYPE_DATE). Дата хранится как двойная, вся часть которой — это количество дней с 30 декабря 1899 г., а фракционной частью которой является доля дня.</p></td>
</tr>
<tr class="even">
<td><p><strong>adDBDate</strong></p></td>
<td><p>133</p></td>
<td><p>Указывает значение даты (yyyyymmdd) (DBTYPE_DBDATE).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adDBTime</strong></p></td>
<td><p>134</p></td>
<td><p>Указывает значение времени (hhmmss) (DBTYPE_DBTIME).</p></td>
</tr>
<tr class="even">
<td><p><strong>adDBTimeStamp</strong></p></td>
<td><p>135</p></td>
<td><p>Указывает штамп даты и времени (yyyymmddhhmmss плюс доля в миллиардных долях) (DBTYPE_DBTIMESTAMP).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adDecimal</strong></p></td>
<td><p>14 </p></td>
<td><p>Указывает точное численное значение с фиксированной точностью и масштабом (DBTYPE_DECIMAL).</p></td>
</tr>
<tr class="even">
<td><p><strong>adDouble</strong></p></td>
<td><p>5 </p></td>
<td><p>Указывает значение плавающей точки с двойной точностью (DBTYPE_R8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adEmpty</strong></p></td>
<td><p>0</p></td>
<td><p>Не указывает значения (DBTYPE_EMPTY).</p></td>
</tr>
<tr class="even">
<td><p><strong>adError</strong></p></td>
<td><p>10 </p></td>
<td><p>Указывает 32-битный код ошибки (DBTYPE_ERROR).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFileTime</strong></p></td>
<td><p>64</p></td>
<td><p>Указывает 64-битное значение, представляющее число 100-наносекундных интервалов с 1 января 1601 г. (DBTYPE_FILETIME).</p></td>
</tr>
<tr class="even">
<td><p><strong>adGUID</strong></p></td>
<td><p>72</p></td>
<td><p>Указывает глобальный уникальный идентификатор (GUID) (DBTYPE_GUID).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIDispatch</strong></p></td>
<td><p>9 </p></td>
<td><p>Указывает указатель на интерфейс <strong>IDispatch</strong> на объекте COM (DBTYPE_IDISPATCH).</p><p><strong>ПРИМЕЧАНИЕ.</strong>Этот тип данных в настоящее время не поддерживается ADO. Использование может привести к непредсказуемым результатам.</p>
</td>
</tr>
<tr class="even">
<td><p><strong>adInteger</strong></p></td>
<td><p>3</p></td>
<td><p>Указывает на подписанный в четырех byte ряд (DBTYPE_I4).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIUnknown</strong></p></td>
<td><p>13</p></td>
<td><p>Указывает указатель на <strong>интерфейс IUnknown</strong> на объекте COM (DBTYPE_IUNKNOWN).</p><p><strong>ПРИМЕЧАНИЕ.</strong>Этот тип данных в настоящее время не поддерживается ADO. Использование может привести к непредсказуемым результатам.
</p></td>
</tr>
<tr class="even">
<td><p><strong>adLongVarBinary</strong></p></td>
<td><p>205</p></td>
<td><p>Указывает длинное двоичное значение.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adLongVarChar</strong></p></td>
<td><p>201</p></td>
<td><p>Указывает значение длинной строки.</p></td>
</tr>
<tr class="even">
<td><p><strong>adLongVarWChar</strong></p></td>
<td><p>203</p></td>
<td><p>Указывает значение строки Юникод с длинным null-terminated.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adNumeric</strong></p></td>
<td><p>131</p></td>
<td><p>Указывает точное численное значение с фиксированной точностью и масштабом (DBTYPE_NUMERIC).</p></td>
</tr>
<tr class="even">
<td><p><strong>adPropVariant</strong></p></td>
<td><p>138</p></td>
<td><p>Указывает средства автоматизации PROPVARIANT (DBTYPE_PROP_VARIANT).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSingle</strong></p></td>
<td><p>4 </p></td>
<td><p>Указывает одноточное значение плавающей точки (DBTYPE_R4).</p></td>
</tr>
<tr class="even">
<td><p><strong>adSmallInt</strong></p></td>
<td><p>2</p></td>
<td><p>Указывает на двухбетный подписанный ряд (DBTYPE_I2).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adTinyInt</strong></p></td>
<td><p>16 </p></td>
<td><p>Указывает на одноайтовую подпись (DBTYPE_I1).</p></td>
</tr>
<tr class="even">
<td><p><strong>adUnsignedBigInt</strong></p></td>
<td><p>21</p></td>
<td><p>Указывает неподписаный неподписаный 8-кет (DBTYPE_UI8).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUnsignedInt</strong></p></td>
<td><p>19</p></td>
<td><p>Указывает неподписаный четверной ряд (DBTYPE_UI4).</p></td>
</tr>
<tr class="even">
<td><p><strong>adUnsignedSmallInt</strong></p></td>
<td><p>18 </p></td>
<td><p>Указывает на неподписавую неподписаемую DBTYPE_UI2.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUnsignedTinyInt</strong></p></td>
<td><p>17 </p></td>
<td><p>Указывает на неподписавую неподписаемую неподписаемую DBTYPE_UI1.</p></td>
</tr>
<tr class="even">
<td><p><strong>adUserDefined</strong></p></td>
<td><p>132</p></td>
<td><p>Указывает переменную, определяемую пользователем (DBTYPE_UDT).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adVarBinary</strong></p></td>
<td><p>204</p></td>
<td><p>Указывает двоичное значение<strong>(только объект Параметр).</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adVarChar</strong></p></td>
<td><p>200</p></td>
<td><p>Указывает строковую величину.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adVariant</strong></p></td>
<td><p>12 </p></td>
<td><p>Указывает вариант <strong>автоматизации</strong> (DBTYPE_VARIANT).</p><p><strong>ПРИМЕЧАНИЕ.</strong>Этот тип данных в настоящее время не поддерживается ADO. Использование может привести к непредсказуемым результатам.</p></td>
</tr>
<tr class="even">
<td><p><strong>adVarNumeric</strong></p></td>
<td><p>139</p></td>
<td><p>Указывает численное значение<strong>(только объект Параметр).</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adVarWChar</strong></p></td>
<td><p>202</p></td>
<td><p>Указывает строку символов Юникод с null-terminated.</p></td>
</tr>
<tr class="even">
<td><p><strong>adWChar</strong></p></td>
<td><p>130</p></td>
<td><p>Указывает строку символов Юникод с null-terminated (DBTYPE_WSTR).</p></td>
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
<th><p>Константа</p></th>
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


---
title: Метод CreateRecordset (RDS)
TOCTitle: CreateRecordset method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3dda0840617c32e9dceea3bd1baa362c5652a373
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295340"
---
# <a name="createrecordset-method-rds"></a>Метод CreateRecordset (RDS)

**Область применения**: Access 2013, Office 2013

Создает пустой, отключенный [набор записей.](recordset-object-ado.md)

## <a name="syntax"></a>Синтаксис

*объект*. CreateRecordset *(ColumnInfos)*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Object* |Переменная объекта, представляюая [RDSServer.DataFactory](datafactory-object-rdsserver.md) или [RDS. Объект DataControl.](datacontrol-object-rds.md)|
|*ColumnsInfos* |Набор **атрибутов Variant,** определяя каждый столбец **созданного Набор записей.** Каждое определение столбца содержит массив из четырех необходимых атрибутов и одного необязательного атрибута. Затем набор массивов столбцов сгруппироваться в массив, который определяет **Набор записей.** Список атрибутов см. в следующей таблице.|

### <a name="variant-array-attributes"></a>Атрибуты массива variant

|Атрибут|Описание|
|:--------|:----------|
|Имя |Имя загона столбца.|
|Тип |Integer типа данных.|
|Size |Набор ширины символов независимо от типа данных.|
|Недействительность |Значение Boolean.|
|Масштаб (необязательный) |Этот необязательный атрибут определяет масштаб для числовых полей. Если это значение не указано, численные значения будут усечены до трех. Точность не влияет, но число цифр, следующих за десятичной точкой, будет усечено до трех.|

## <a name="remarks"></a>Примечания

Бизнес-объект на стороне сервера может  заполнять полученный набор записей данными от поставщика данных, не относящегося к OLE DB, например файла операционной системы, содержащего котировки акций.

В следующей таблице перечислены значения [DataTypeEnum,](datatypeenum.md) поддерживаемые **методом CreateRecordset.** Указанный номер — это справочный номер, используемый для определения полей.

Каждый из типов данных имеет фиксированную длину или переменную длину. Типы фиксированной длины должны быть определены с размером -1, так как размер заранее определен и определение размера по-прежнему требуется. Типы данных переменной длины позволяют размер от 1 до 32767.

Для некоторых типов переменных данных тип может быть принужден к типу, отмеченным в столбце Подмена. Замены будут созданы и заполнены только после создания и заполнения **Recordset.** Затем вы можете проверить фактический тип данных, если это необходимо.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Длина</p></th>
<th><p>Константа</p></th>
<th><p>Номер</p></th>
<th><p>Замена</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adTinyInt</strong></p></td>
<td><p>16 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adSmallInt</strong></p></td>
<td><p>2</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adInteger</strong></p></td>
<td><p>3</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adBigInt</strong></p></td>
<td><p>20</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adUnsignedTinyInt</strong></p></td>
<td><p>17 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adUnsignedSmallInt</strong></p></td>
<td><p>18 </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adUnsignedInt</strong></p></td>
<td><p>19</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adUnsignedBigInt</strong></p></td>
<td><p>21</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adSingle</strong></p></td>
<td><p>4 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adDouble</strong></p></td>
<td><p>5 </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adCurrency</strong></p></td>
<td><p>6 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adDecimal</strong></p></td>
<td><p>14 </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adNumeric</strong></p></td>
<td><p>131</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adBoolean</strong></p></td>
<td><p>11</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adError</strong></p></td>
<td><p>10 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adGuid</strong></p></td>
<td><p>72</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adDate</strong></p></td>
<td><p>7 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adDBDate</strong></p></td>
<td><p>133</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adDBTime</strong></p></td>
<td><p>134</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>adDBTimestamp</strong></p></td>
<td><p>135</p></td>
<td><p>7 </p></td>
</tr>
<tr class="odd">
<td><p>Переменная</p></td>
<td><p><strong>adBSTR</strong></p></td>
<td><p>8 </p></td>
<td><p>130</p></td>
</tr>
<tr class="even">
<td><p>Переменная</p></td>
<td><p><strong>adChar</strong></p></td>
<td><p>129</p></td>
<td><p>200</p></td>
</tr>
<tr class="odd">
<td><p>Переменная</p></td>
<td><p><strong>adVarChar</strong></p></td>
<td><p>200</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Переменная</p></td>
<td><p><strong>adLongVarChar</strong></p></td>
<td><p>201</p></td>
<td><p>200</p></td>
</tr>
<tr class="odd">
<td><p>Переменная</p></td>
<td><p><strong>adWChar</strong></p></td>
<td><p>130</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Переменная</p></td>
<td><p><strong>adVarWChar</strong></p></td>
<td><p>202</p></td>
<td><p>130</p></td>
</tr>
<tr class="odd">
<td><p>Переменная</p></td>
<td><p><strong>adLongVarWChar</strong></p></td>
<td><p>203</p></td>
<td><p>130</p></td>
</tr>
<tr class="even">
<td><p>Переменная</p></td>
<td><p><strong>adBinary</strong></p></td>
<td><p>128</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Переменная</p></td>
<td><p><strong>adVarBinary</strong></p></td>
<td><p>204</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Переменная</p></td>
<td><p><strong>adLongVarBinary</strong></p></td>
<td><p>205</p></td>
<td><p>204</p></td>
</tr>
</tbody>
</table>


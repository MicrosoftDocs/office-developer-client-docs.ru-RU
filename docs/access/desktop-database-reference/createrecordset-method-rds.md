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

Создает пустой отключенный [набор записей](recordset-object-ado.md).

## <a name="syntax"></a>Синтаксис

*объект*. CreateRecordset (*колумнинфос*)

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*Object* |Объектная переменная, представляющая объект [рдссервер.](datafactory-object-rdsserver.md) DataObject или [RDS. Объект управления](datacontrol-object-rds.md) DataObject.|
|*колумнсинфос* |Массив **Variant** атрибутов, который определяет каждый столбец в созданном **наборе записей** . Каждое определение столбца содержит массив из четырех обязательных атрибутов и один необязательный атрибут. После этого набор массивов столбцов будет сгруппирован в массив, который определяет **набор записей**. Список атрибутов представлен в следующей таблице.|

### <a name="variant-array-attributes"></a>Атрибуты массива Variant

|Атрибут|Описание|
|:--------|:----------|
|Имя |Имя заголовка столбца.|
|Тип |Целое число типа данных.|
|Размер |Целое значение ширины в символах, независимо от типа данных.|
|Возможность принимать значения NULL |Логическое значение.|
|Scale (необязательно) |Этот необязательный атрибут определяет масштаб для числовых полей. Если это значение не указано, числовые значения будут сокращены до шкалы 3. На точность не влияет, но количество цифр после десятичной точки будет укорочено до 3.|

## <a name="remarks"></a>Примечания

Серверный бизнес-объект может заполнить полученный **набор записей** данными из поставщика данных, отличного от OLE DB, например из файла операционной системы, содержащего котировки акций.

В следующей таблице приведены значения [DataTypeEnum](datatypeenum.md) , поддерживаемые методом **CreateRecordset** . В списке указан номер ссылки, используемый для определения полей.

Каждый тип данных имеет фиксированную или переменную длину. Типы фиксированной длины должны определяться размером – 1, так как размер предварительно определен, а определение размера по-прежнему требуется. Типы данных переменной длины допускают размер от 1 до 32767.

Для некоторых типов данных переменных тип может быть приведен к типу, указанному в столбце подстановки. Подстановки не отображаются до тех пор, пока не будет создан и заполнен **набор записей** . При необходимости вы можете проверить фактический тип данных.

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
<th><p>Подстановки</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>адтининт</strong></p></td>
<td><p>16 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>адсмаллинт</strong></p></td>
<td><p>2</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>адинтежер</strong></p></td>
<td><p>4</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>адбигинт</strong></p></td>
<td><p>двадцать</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>адунсигнедтининт</strong></p></td>
<td><p>17 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>адунсигнедсмаллинт</strong></p></td>
<td><p>18 </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>адунсигнединт</strong></p></td>
<td><p>19</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>адунсигнедбигинт</strong></p></td>
<td><p>21</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>адсингле</strong></p></td>
<td><p>4 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>аддаубле</strong></p></td>
<td><p>5 </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>адкурренци</strong></p></td>
<td><p>6 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>аддеЦимал</strong></p></td>
<td><p>14 </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>аднумерик</strong></p></td>
<td><p>131</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>адбулеан</strong></p></td>
<td><p>11 </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>адеррор</strong></p></td>
<td><p>10 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>адгуид</strong></p></td>
<td><p>72</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>аддате</strong></p></td>
<td><p>7 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>аддбдате</strong></p></td>
<td><p>133</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>аддбтиме</strong></p></td>
<td><p>134</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ИСПРАВЛЕНО</p></td>
<td><p><strong>аддбтиместамп</strong></p></td>
<td><p>135</p></td>
<td><p>7 </p></td>
</tr>
<tr class="odd">
<td><p>Переменная</p></td>
<td><p><strong>адбстр</strong></p></td>
<td><p>8 </p></td>
<td><p>130</p></td>
</tr>
<tr class="even">
<td><p>Переменная</p></td>
<td><p><strong>адчар</strong></p></td>
<td><p>129</p></td>
<td><p>200</p></td>
</tr>
<tr class="odd">
<td><p>Переменная</p></td>
<td><p><strong>адварчар</strong></p></td>
<td><p>200</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Переменная</p></td>
<td><p><strong>адлонгварчар</strong></p></td>
<td><p>201</p></td>
<td><p>200</p></td>
</tr>
<tr class="odd">
<td><p>Переменная</p></td>
<td><p><strong>адвчар</strong></p></td>
<td><p>130</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Переменная</p></td>
<td><p><strong>адварвчар</strong></p></td>
<td><p>202</p></td>
<td><p>130</p></td>
</tr>
<tr class="odd">
<td><p>Переменная</p></td>
<td><p><strong>адлонгварвчар</strong></p></td>
<td><p>203</p></td>
<td><p>130</p></td>
</tr>
<tr class="even">
<td><p>Переменная</p></td>
<td><p><strong>адбинари</strong></p></td>
<td><p>128</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Переменная</p></td>
<td><p><strong>адварбинари</strong></p></td>
<td><p>204</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Переменная</p></td>
<td><p><strong>адлонгварбинари</strong></p></td>
<td><p>205</p></td>
<td><p>204</p></td>
</tr>
</tbody>
</table>


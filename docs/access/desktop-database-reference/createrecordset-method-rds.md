---
title: Метод CreateRecordset (RDS)
TOCTitle: CreateRecordset Method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d975faf45cf6a16bdae9f800084ebbbbaec3127d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868534"
---
# <a name="createrecordset-method-rds"></a>Метод CreateRecordset (RDS)


**Применимо к**: Access 2013, Office 2013


Создает пустой, отключенные [набора записей](recordset-object-ado.md).

## <a name="syntax"></a>Синтаксис

*объект*. CreateRecordset (*ColumnInfos*)

## <a name="parameters"></a>Параметры

  - *Объект*

  - Объектную переменную, которая представляет [RDSServer.DataFactory](datafactory-object-rdsserver.md) или [RDS. DataControl](datacontrol-object-rds.md) объекта.

  - *ColumnsInfos*

  - Создать **Variant** массив атрибутов, определяющий столбцы в **набора записей** . Определение каждого столбца содержит массив четыре обязательные атрибуты и один необязательный атрибут. Набор столбцов массивов нажмите сгруппированы в массив, который определяет **набор записей**.
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Атрибут</p></th>
    <th><p>Описание</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Имя</p></td>
    <td><p>Имя заголовка столбца.</p></td>
    </tr>
    <tr class="even">
    <td><p>Тип</p></td>
    <td><p>Целое число типа данных.</p></td>
    </tr>
    <tr class="odd">
    <td><p>Size</p></td>
    <td><p>Целое число от ширины знаков, независимо от типа данных.</p></td>
    </tr>
    <tr class="even">
    <td><p>Возможность принимать значение NULL</p></td>
    <td><p>Логическое значение.</p></td>
    </tr>
    <tr class="odd">
    <td><p>Масштаб<br />
(Необязательно)</p></td>
    <td><p>Этот дополнительный атрибут задает масштаб для числовых полей. Если это значение не указано, с горизонтальным трех усекаются числовых значений. Количество разрядов после запятой будет усечено до трех, но не повлияет точности.</p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a>Замечания

На сервере бизнес-объекта можно заполнить результирующего **набора записей** с данными из не - поставщиков данных OLE DB, такие как файл операционной системы, содержащий акций.

В следующей таблице перечислены значения [DataTypeEnum](datatypeenum.md) , поддерживаемый метод **CreateRecordset** . Номер, указанный является номер ссылки, используемые для определения полей.

Каждый из типов данных является фиксированной длины или переменной длины. Типы фиксированной длины должны быть определены с размером – 1, так как предварительно определенный размер и определение размера по-прежнему требуется. Типы данных переменной длины разрешить размер от 1 до 32767.

Для некоторых типов данных переменной тип может привести к типу, указаны в столбце подстановки. Вы не увидите замены до того времени, после создания и заполнения **набора записей** . Затем следует проверить, тип фактических данных, если это необходимо.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Length</p></th>
<th><p>Constant</p></th>
<th><p>Number</p></th>
<th><p>Замена </p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Фиксация</p></td>
<td><p><strong>adTinyInt</strong></p></td>
<td><p>16</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Фиксация</p></td>
<td><p><strong>adSmallInt</strong></p></td>
<td><p>2</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Фиксация</p></td>
<td><p><strong>adInteger</strong></p></td>
<td><p>3</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Фиксация</p></td>
<td><p><strong>adBigInt</strong></p></td>
<td><p>20</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Фиксация</p></td>
<td><p><strong>adUnsignedTinyInt</strong></p></td>
<td><p>17</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Фиксация</p></td>
<td><p><strong>adUnsignedSmallInt</strong></p></td>
<td><p>18</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Фиксация</p></td>
<td><p><strong>adUnsignedInt</strong></p></td>
<td><p>19</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Фиксация</p></td>
<td><p><strong>adUnsignedBigInt</strong></p></td>
<td><p>21</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Фиксация</p></td>
<td><p><strong>adSingle</strong></p></td>
<td><p>4</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Фиксация</p></td>
<td><p><strong>adDouble</strong></p></td>
<td><p>5</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Фиксация</p></td>
<td><p><strong>adCurrency</strong></p></td>
<td><p>6</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Фиксация</p></td>
<td><p><strong>adDecimal</strong></p></td>
<td><p>14</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Фиксация</p></td>
<td><p><strong>adNumeric</strong></p></td>
<td><p>131</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Фиксация</p></td>
<td><p><strong>adBoolean</strong></p></td>
<td><p>11</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Фиксация</p></td>
<td><p><strong>adError</strong></p></td>
<td><p>10</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Фиксация</p></td>
<td><p><strong>adGuid</strong></p></td>
<td><p>72</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Фиксация</p></td>
<td><p><strong>adDate</strong></p></td>
<td><p>7</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Фиксация</p></td>
<td><p><strong>adDBDate</strong></p></td>
<td><p>133</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Фиксация</p></td>
<td><p><strong>adDBTime</strong></p></td>
<td><p>134</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Фиксация</p></td>
<td><p><strong>adDBTimestamp</strong></p></td>
<td><p>135</p></td>
<td><p>7</p></td>
</tr>
<tr class="odd">
<td><p>Переменная</p></td>
<td><p><strong>adBSTR</strong></p></td>
<td><p>8</p></td>
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


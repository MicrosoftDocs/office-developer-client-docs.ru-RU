---
title: Свойство ExecuteOptions (RDS)
TOCTitle: ExecuteOptions property (RDS)
ms:assetid: fb244cbd-9a03-9128-1373-694c9061c9da
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250285(v=office.15)
ms:contentKeyID: 48548864
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9cf773090ccb37bf4cad4aff41499ad01f966479
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293254"
---
# <a name="executeoptions-property-rds"></a>Свойство ExecuteOptions (RDS)


**Область применения**: Access 2013, Office 2013

Указывает, включено ли асинхронное выполнение.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает одно из следующих значений.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Адцексексинк</strong></p></td>
<td><p>Выполняет следующее обновление <a href="recordset-object-ado.md">набора записей</a> в синхронном режиме.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адцексекасинк</strong></p></td>
<td><p>Значение, используемое по умолчанию. Асинхронно выполняет следующее обновление объекта <strong>Recordset</strong> .</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Каждый исполняемый файл на стороне клиента, использующий эти константы, должен предоставлять объявления для них. Вы можете вырезать и вставить объявления констант из файла Адквбс. Inc, расположенного в папке C:\Program Files\Common Филес\систем\мсадк.

## <a name="remarks"></a>Замечания

Если для **ExecuteOptions** задано значение **адцексекасинк**, асинхронно выполняется следующий вызов **обновления** в [RDS. ](datacontrol-object-rds.md) **Набор записей**объекта DataObject.

Если вы попытаетесь вызвать [Reset](reset-method-rds.md), [Refresh](refresh-method-rds.md), [SubmitChanges](submitchanges-method-rds.md), [CancelUpdate](cancelupdate-method-ado.md)или [Recordset](recordset-sourcerecordset-properties-rds.md) , в то время как другая асинхронная операция, которая может изменить [RDS. ](datacontrol-object-rds.md)Выполняется **набор записей** объекта DataObject, возникает ошибка.

Если во время асинхронной операции возникает ошибка, то **RDS. **Изменение значения свойства [ReadyState](readystate-property-rds.md) объекта **адкреадистателоадед** на **Адкреадистатекомплете**, а значение свойства **Recordset** *не*остается.


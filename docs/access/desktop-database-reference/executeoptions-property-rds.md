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

## <a name="settings-and-return-values"></a>Параметры и значения возврата

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
<td><p><strong>adcExecSync</strong></p></td>
<td><p>Выполняет следующее синхронное обновление <a href="recordset-object-ado.md">Recordset.</a></p></td>
</tr>
<tr class="even">
<td><p><strong>adcExecAsync</strong></p></td>
<td><p>Значение, используемое по умолчанию. Выполняет следующее обновление асинхронно <strong>recordset.</strong></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Каждый исполняемый клиентский файл, использующий эти константы, должен предоставлять для них объявления. Вы можете вырезать и ввести постоянные объявления, которые нужны из файла Adcvbs.inc, расположенного в папке C:\Program Files\Common Files\System\MSADC.

## <a name="remarks"></a>Примечания

Если **в executeOptions** задан **adcExecAsync,** то это асинхронно выполняет следующий вызов **обновления** в [RDS. Набор](datacontrol-object-rds.md) записей объекта DataControl.

Если вы попробуете вызвать [сброс,](reset-method-rds.md) [обновить,](refresh-method-rds.md) [отправитьChanges,](submitchanges-method-rds.md) [CancelUpdate](cancelupdate-method-ado.md)или [Recordset,](recordset-sourcerecordset-properties-rds.md) а также другую асинхронную операцию, которая может изменить [RDS. Выполняется набор](datacontrol-object-rds.md) записей объекта DataControl, возникает ошибка. 

Если ошибка возникает во время асинхронной операции, **RDS. Значение ReadyState объекта DataControl** изменяется с **adcReadyStateLoaded** на **adcReadyStateComplete,** а значение свойства **Recordset** остается *Ничто*. [](readystate-property-rds.md)


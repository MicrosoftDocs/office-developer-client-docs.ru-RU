---
title: Свойство ReadyState (RDS)
TOCTitle: ReadyState property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 71dd674e90e2438c616f0973c4f9948f1b20b1f1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714782"
---
# <a name="readystate-property-rds"></a>Свойство ReadyState (RDS)

**Применимо к**: Access 2013, Office 2013

Индикатор выполнения объекта [DataControl](datacontrol-object-rds.md) при извлечении данных в его объекта [набора записей](recordset-object-ado.md) .

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает одно из следующих значений.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adcReadyStateLoaded</strong></p></td>
<td><p>Текущий запрос по-прежнему выполняется и строки не выбраны. Объект <strong>DataControl</strong> <strong>записей</strong> недоступен для использования.</p></td>
</tr>
<tr class="even">
<td><p><strong>adcReadyStateInteractive</strong></p></td>
<td><p>Начальный набор строк, которые извлекаются с текущего запроса был сохранен в объекте <strong>DataControl</strong> <strong>записей</strong> и доступны для использования. Оставшиеся строки по-прежнему извлечении.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adcReadyStateComplete</strong></p></td>
<td><p>Все полученные текущего запроса строки хранятся в объекте <strong>DataControl</strong> <strong>записей</strong> и доступны для использования. Это состояние также будет существовать, если операция прервана из-за ошибки или объекта <strong>набора записей</strong> не инициализирован.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Каждый исполняемый файл со стороны клиента, который использует эти константы необходимо предоставить объявления для них. Можно вырежьте и вставьте объявлений констант из файла Adcvbs.inc, находящийся в папке C:\Program Files\Common Files\System\MSADC.

## <a name="remarks"></a>Замечания

Событие [onReadyStateChange](onreadystatechange-event-rds.md) используется для отслеживания изменений в свойстве **ReadyState** во время операции асинхронного запроса. Это эффективнее, чем периодически проверки значения свойства.

При возникновении ошибки во время асинхронной операции, изменения свойств **ReadyState** **adcReadyStateComplete**свойство [State](state-property-ado.md) изменяется с **adStateExecuting** **adStateClosed**и **записей** Свойство [Value](value-property-ado.md) объекта остается *значение Nothing*.


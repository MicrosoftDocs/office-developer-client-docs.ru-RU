---
title: Свойство ReadyState (RDS)
TOCTitle: ReadyState Property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be07b0ffb983889aa7002406da9c40e13522c5c0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880120"
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
> <P>Каждый исполняемый файл со стороны клиента, который использует эти константы необходимо предоставить объявления для них. Можно вырежьте и вставьте объявлений констант из файла Adcvbs.inc, находящийся в папке C:\Program Files\Common Files\System\MSADC.</P>



## <a name="remarks"></a>Замечания

Событие [onReadyStateChange](onreadystatechange-event-rds.md) используется для отслеживания изменений в свойстве **ReadyState** во время операции асинхронного запроса. Это эффективнее, чем периодически проверки значения свойства.

При возникновении ошибки во время асинхронной операции, изменения свойств **ReadyState** **adcReadyStateComplete**свойство [State](state-property-ado.md) изменяется с **adStateExecuting** **adStateClosed**и **записей** Свойство [Value](value-property-ado.md) объекта остается *значение Nothing*.


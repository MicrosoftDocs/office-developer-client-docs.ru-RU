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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300821"
---
# <a name="readystate-property-rds"></a>Свойство ReadyState (RDS)

**Область применения**: Access 2013, Office 2013

Указывает ход выполнения объекта [DataControl](datacontrol-object-rds.md) при извлечении данных в объект [Recordset.](recordset-object-ado.md)

## <a name="settings-and-return-values"></a>Параметры и значения возврата

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
<td><p>Текущий запрос по-прежнему выполняется, и строки не были извлечены. Набор записей объекта <strong>DataControl</strong> не доступен для использования. <strong></strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adcReadyStateInteractive</strong></p></td>
<td><p>Начальный набор строк, полученных текущим запросом, хранится в наборе <strong></strong> записей объекта <strong>DataControl</strong> и доступен для использования. Остальные строки по-прежнему извлекаются.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adcReadyStateComplete</strong></p></td>
<td><p>Все строки, извлеченные текущим запросом, хранятся в наборе записей объекта <strong>DataControl</strong> и доступны для использования. <strong></strong> Это состояние также будет существовать, если операция прерывается из-за ошибки или если объект <strong>Recordset</strong> не инициализирован.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Каждый исполняемый клиентский файл, использующий эти константы, должен предоставлять для них объявления. Вы можете вырезать и ввести нужные постоянные объявления из файла Adcvbs.inc, расположенного в папке C:\Program Files\Common Files\System\MSADC.

## <a name="remarks"></a>Примечания

Используйте [событие onReadyStateChange](onreadystatechange-event-rds.md) для мониторинга изменений свойства **ReadyState** во время асинхронной операции запроса. Это эффективнее, чем периодические проверки значения свойства.

Если ошибка возникает во время асинхронной операции, свойство **ReadyState** изменяется на [](value-property-ado.md) **adcReadyStateComplete,** свойство состояния меняется от **adStateExecuting до adStateClosed,** а свойство Значение объекта **Recordset** остается nothing *.* [](state-property-ado.md) 


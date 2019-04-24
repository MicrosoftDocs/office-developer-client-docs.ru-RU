---
title: Сводка по объектной модели RDS
TOCTitle: RDS object model summary
ms:assetid: 0355d62a-dabb-8643-5c43-1e98ccf7f3b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248800(v=office.15)
ms:contentKeyID: 48542981
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 33cbdc6de644592d87b7d49e65a5c5674ad94d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300877"
---
# <a name="rds-object-model-summary"></a>Сводка по объектной модели RDS


**Область применения**: Access 2013, Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Object</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="dataspace-object-rds.md">Рабочих. DataSpace</a></p></td>
<td><p>Этот объект содержит метод получения прокси-сервера. Прокси-сервер может быть установлен по умолчанию или настраиваемой серверной программой (бизнес-объектом). Серверная программа может быть вызвана в Интернете, интрасети, локальной сети или локальной библиотеке динамической компоновки.</p></td>
</tr>
<tr class="even">
<td><p><a href="datafactory-object-rdsserver.md">Рдссервер. факт.</a></p></td>
<td><p>Этот объект представляет программу сервера по умолчанию. Он выполняет процесс получения и обновления данных RDS, используемый по умолчанию.</p></td>
</tr>
<tr class="odd">
<td><p><a href="datacontrol-object-rds.md">Рабочих. DataControl</a></p></td>
<td><p>Этот объект может автоматически вызывать <strong>RDS. Объект Space</strong> и <strong>рдссервер.</strong> объект фактов. Используйте этот объект, чтобы вызвать процесс получения или обновления данных RDS, используемый по умолчанию. Этот объект также предоставляет средства для визуальных элементов управления для доступа к возвращенному объекту <strong>Recordset</strong> .</p></td>
</tr>
</tbody>
</table>


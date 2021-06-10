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
<th><p>Объект</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="dataspace-object-rds.md">RDS. DataSpace</a></p></td>
<td><p>Этот объект содержит метод получения прокси-сервера. Прокси-сервер может быть по умолчанию или настраиваемой серверной программой (бизнес-объектом). Серверная программа может вызываться в Интернете, интрасети, локальной сети или локальной библиотеке динамических ссылок.</p></td>
</tr>
<tr class="even">
<td><p><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></p></td>
<td><p>Этот объект представляет серверную программу по умолчанию. Он выполняет ирисовку данных RDS по умолчанию и поведение обновления.</p></td>
</tr>
<tr class="odd">
<td><p><a href="datacontrol-object-rds.md">RDS. DataControl</a></p></td>
<td><p>Этот объект может автоматически вызывать <strong>RDS. Объекты DataSpace</strong> и <strong>RDSServer.DataFactory.</strong> Используйте этот объект, чтобы вызвать по умолчанию сбор данных RDS или обновление поведения. Этот объект также предоставляет средства визуального управления для доступа к возвращенным <strong>объекту Recordset.</strong></p></td>
</tr>
</tbody>
</table>


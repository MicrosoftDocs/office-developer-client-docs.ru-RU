---
title: Метод Cancel (ADO)
TOCTitle: Cancel method (ADO)
ms:assetid: 747edc04-a5cc-3631-2d0b-82e7e41a76b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249476(v=office.15)
ms:contentKeyID: 48545662
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231032
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 791803bb8935ffab24e5aed7e4e6a77360e82b65
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713235"
---
# <a name="cancel-method-ado"></a>Метод Cancel (ADO)

**Применимо к**: Access 2013, Office 2013

Отменяет выполнение ожидающих асинхронного вызова метода.

## <a name="syntax"></a>Синтаксис

*объект*. Отмена

## <a name="remarks"></a>Замечания

Используйте метод **Cancel** для завершения выполнения асинхронного вызова метода (то есть, метод, вызываемый с параметром **adAsyncConnect**, **adAsyncExecute**или **adAsyncFetch** ).

В следующей таблице показаны какие задачи останавливается при использовании метода **Cancel** на определенный тип объекта.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
Если <em>объект</em> является</p></th>
<th><p>Последний асинхронного вызова этого метода будет завершен</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="command-object-ado.md">Command</a></p></td>
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute</a></p></td>
</tr>
<tr class="even">
<td><p><a href="connection-object-ado.md">Connection</a></p></td>
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Выполнение</a> или <a href="open-method-ado-connection.md">Open</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="record-object-ado.md">Record</a></p></td>
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a>, <a href="deleterecord-method-ado.md">макрокоманду УдалитьЗапись</a>, <a href="moverecord-method-ado.md">MoveRecord</a>или <a href="open-method-ado-record.md">Открыть</a></p></td>
</tr>
<tr class="even">
<td><p><a href="recordset-object-ado.md">Recordset</a></p></td>
<td><p><a href="open-method-ado-recordset.md">Open</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="stream-object-ado.md">Stream</a></p></td>
<td><p><a href="open-method-ado-stream.md">Open</a></p></td>
</tr>
</tbody>
</table>


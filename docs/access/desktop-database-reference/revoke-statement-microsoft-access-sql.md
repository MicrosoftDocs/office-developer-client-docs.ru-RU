---
title: ОТМЕНИТЬ оператора (Microsoft Access SQL)
TOCTitle: REVOKE statement (Microsoft Access SQL)
ms:assetid: 69399fd6-c4e8-f2e2-e5f4-48ae779323f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195272(v=office.15)
ms:contentKeyID: 48545409
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277479
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 20122fee617597987940766a076d5f968a87c2d2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698452"
---
# <a name="revoke-statement-microsoft-access-sql"></a>ОТМЕНИТЬ оператора (Microsoft Access SQL)

**Применимо к**: Access 2013, Office 2013

Запрещение определенных привилегий существующему пользователю или группе.

## <a name="syntax"></a>Синтаксис

ОТМЕНИТЬ {*принципу предоставления минимальных прав*\[, *принципу предоставления минимальных прав*,... \]} Д {таблицы в *таблице* | Объект *object*|

CONTAINTER *container*} из {*имя_обладателя_прав*\[, *имя_обладателя_прав*,... \]}

Инструкция REVOKE состоит из следующих частей:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Часть</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>принципу предоставления минимальных прав</em></p></td>
<td><p>Привилегии или права, которое требуется отозвать. Привилегии задаются с помощью следующих ключевых слов: выбор, DELETE, INSERT, UPDATE, размещения сообщений, SELECTSECURITY, UPDATESECURITY, DBPASSWORD, UPDATEIDENTITY, создать, SELECTSCHEMA, СХЕМЫ и UPDATEOWNER.</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
<td><p>Любое допустимое имя таблицы.</p></td>
</tr>
<tr class="odd">
<td><p><em>object</em></p></td>
<td><p>Это могут использовать любой объект не таблицы. Сохраненные запрос (представления или процедуры) — один пример.</p></td>
</tr>
<tr class="even">
<td><p><em>контейнер</em></p></td>
<td><p>Имя допустимого хранилища.</p></td>
</tr>
<tr class="odd">
<td><p><em>имя_обладателя_прав</em></p></td>
<td><p>Имя пользователя или группы.</p></td>
</tr>
</tbody>
</table>


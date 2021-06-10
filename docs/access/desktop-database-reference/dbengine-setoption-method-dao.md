---
title: Метод DBEngine.SetOption (DAO)
TOCTitle: SetOption Method
ms:assetid: ea55c10c-2385-1b7e-0cba-32982c9b6643
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836236(v=office.15)
ms:contentKeyID: 48548461
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1088781
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5875a8935b1b44c3c36b29344af32df552f6e01c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294199"
---
# <a name="dbenginesetoption-method-dao"></a>Метод DBEngine.SetOption (DAO)

**Область применения**: Access 2013, Office 2013

Временно переопределяет значения для ключей двигателя базы данных Microsoft Access в реестре Windows (только в рабочей области Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражения* . SetOption ***(Параметр***, ***Значение***)

*выражение*: выражение, возвращающее объект **DBEngine**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Option</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Константа, как описано в Примечание.</p></td>
</tr>
<tr class="even">
<td><p><em>Value</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Значение, которое необходимо установить.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Каждая константа ссылается на соответствующий ключ реестра в пути HKEY LOCAL MACHINE \_ \_ SOFTWARE Microsoft Office \\ \\ \\ \\ 12.0 \\ Access Connectivity Engine \\ Engines \\ ACE (то есть **dbSharedAsyncDelay** соответствует ключевому программному обеспечению локальной машины HKEY Microsoft Office 12.0 Двигатели подключения доступа \_ \_ \\ \\ \\ \\ \\ \\ \\ ACE \\ SharedAsyncDelay и т. д.).

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
<td><p><strong>dbPageTimeout</strong></p></td>
<td><p>Клавиша PageTimeout</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSharedAsyncDelay</strong></p></td>
<td><p>Ключ SharedAsyncDelay</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbExclusiveAsyncDelay</strong></p></td>
<td><p>Ключ ExclusiveAsyncDelay</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLockRetry</strong></p></td>
<td><p>Ключ LockRetry</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbUserCommitSync</strong></p></td>
<td><p>Ключ UserCommitSync</p></td>
</tr>
<tr class="even">
<td><p><strong>dbImplicitCommitSync</strong></p></td>
<td><p>Клавиша ImplicitCommitSync</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbMaxBufferSize</strong></p></td>
<td><p>Ключ MaxBufferSize</p></td>
</tr>
<tr class="even">
<td><p><strong>dbMaxLocksPerFile</strong></p></td>
<td><p>Ключ MaxLocksPerFile</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLockDelay</strong></p></td>
<td><p>Ключ LockDelay</p></td>
</tr>
<tr class="even">
<td><p><strong>dbRecycleLVs</strong></p></td>
<td><p>Ключ RecycleLVs</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFlushTransactionTimeout</strong></p></td>
<td><p>Клавиша FlushTransactionTimeout</p></td>
</tr>
</tbody>
</table>


Используйте метод **SetOption** для переопределения значений реестра во время работы. Новые значения, установленные с помощью метода **SetOption,** остаются в силе до тех пор, пока не будут изменены другим вызовом **SetOption** или до закрытия объекта **DBEngine.**


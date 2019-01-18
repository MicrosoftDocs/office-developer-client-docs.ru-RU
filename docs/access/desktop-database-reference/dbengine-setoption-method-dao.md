---
title: 'Метод: DBEngine.SetOption (DAO)'
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699893"
---
# <a name="dbenginesetoption-method-dao"></a>Метод: DBEngine.SetOption (DAO)

**Применимо к**: Access 2013, Office 2013

Временно переопределяет значения для клавиш ядра базы данных Microsoft Access в реестре Windows (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . SetOption (***вариант***, ***значение***)

*выражение* Выражение, возвращающее объект **DBEngine** .

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Option</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>Константа, как описано в разделе Примечания.</p></td>
</tr>
<tr class="even">
<td><p><em>Value</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Значение, которое требуется для параметра.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Каждая константа ссылается на соответствующий раздел реестра в поле путь HKEY\_ЛОКАЛЬНОГО\_МАШИНЫ\\программного обеспечения\\Microsoft\\Office\\12.0\\ядро доступа подключения к\\обработчики\\ACE (то есть, **dbSharedAsyncDelay** соответствующий ключ HKEY\_ЛОКАЛЬНОГО\_МАШИНЫ\\программного обеспечения\\Microsoft\\Office\\12.0\\модуль подключения к Access\\обработчики\\элемент управления ДОСТУПОМ \\SharedAsyncDelay, и так далее).

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
<td><p>Клавиша SharedAsyncDelay</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbExclusiveAsyncDelay</strong></p></td>
<td><p>Клавиша ExclusiveAsyncDelay</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLockRetry</strong></p></td>
<td><p>Клавиша LockRetry</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbUserCommitSync</strong></p></td>
<td><p>Клавиша UserCommitSync</p></td>
</tr>
<tr class="even">
<td><p><strong>dbImplicitCommitSync</strong></p></td>
<td><p>Клавиша ImplicitCommitSync</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbMaxBufferSize</strong></p></td>
<td><p>Клавиша MaxBufferSize</p></td>
</tr>
<tr class="even">
<td><p><strong>dbMaxLocksPerFile</strong></p></td>
<td><p>Клавиша MaxLocksPerFile</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLockDelay</strong></p></td>
<td><p>Клавиша LockDelay</p></td>
</tr>
<tr class="even">
<td><p><strong>dbRecycleLVs</strong></p></td>
<td><p>Клавиша RecycleLVs</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbFlushTransactionTimeout</strong></p></td>
<td><p>Клавиша FlushTransactionTimeout</p></td>
</tr>
</tbody>
</table>


Используйте метод **SetOption** переопределение значения реестра во время выполнения. Новые значения, установленных с помощью метода **SetOption** остаются в силе до еще раз изменена другой вызов **SetOption** или закрытии объекта **DBEngine** .


---
title: Метод TableDefs.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 63f543fd86e309372e0432c3e45513cd9d3942ab
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709322"
---
# <a name="tabledefsdelete-method-dao"></a>Метод TableDefs.Delete (DAO)

**Применимо к**: Access 2013, Office 2013

Удаляет указанный объект **TableDef** из коллекции **TableDefs** .

## <a name="syntax"></a>Синтаксис

*выражение* . Удаление (***имя***)

*выражение* Переменная, которая представляет собой объект- **TableDefs** .

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
<td><p><em>Name</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Имя TableDef для удаления.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Метод Delete поддерживается только в том случае, когда объект **TableDef** новые и еще не был добавлен к базе данных или свойство **с возможностью записи** **TableDef** имеет значение **True**.


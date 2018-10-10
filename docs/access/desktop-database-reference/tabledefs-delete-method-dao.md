---
title: TableDefs.Delete Method (DAO)
TOCTitle: Delete Method
ms:assetid: 130bb50d-17c3-b2ab-9360-0d91d0cee131
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845419(v=office.15)
ms:contentKeyID: 48543358
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e39a1390c9ea26baa83d8203967d603237a3ab1c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481465"
---
# <a name="tabledefsdelete-method-dao"></a>TableDefs.Delete Method (DAO)


**Применимо к**: Access 2013 | Office 2013

Удаляет указанный объект **TableDef** из коллекции **TableDefs** .

## <a name="syntax"></a>Синтаксис

*выражение* . Удаление (***имя***)

*выражение* Переменная, которая представляет собой объект- **TableDefs** .

### <a name="parameters"></a>Параметры

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
<td><p>Имя</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Имя TableDef для удаления.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Метод Delete поддерживается только в том случае, когда объект **TableDef** новые и еще не был добавлен к базе данных или свойство **с возможностью записи** **TableDef** имеет значение **True**.


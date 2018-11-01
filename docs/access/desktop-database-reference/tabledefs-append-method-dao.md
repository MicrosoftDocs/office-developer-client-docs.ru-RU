---
title: TableDefs.Append Method (DAO)
TOCTitle: Append Method
ms:assetid: f951a3c4-dade-c1ef-3bfc-6b2a60e12adc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837001(v=office.15)
ms:contentKeyID: 48548811
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 016b31f4c6c6648cfa853e3f5087451485c7d65f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884459"
---
# <a name="tabledefsappend-method-dao"></a>TableDefs.Append Method (DAO)


**Применимо к**: Access 2013, Office 2013

Добавляет новый **TableDef** в коллекцию **TableDefs** .

## <a name="syntax"></a>Синтаксис

*выражение* . Добавление (***объект***)

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
<td><p>Объект</p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Объект</strong></p></td>
<td><p>Объектная переменная, представляющий поле, добавленный в коллекцию.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Добавленный объект становится сохраняемого объекта, хранящиеся на диске, пока не будет удалена с помощью метода **Delete** .

Добавление нового объекта выполняется немедленно, но следует использовать метод **Refresh** в семействах сайтов, которые может затронуть изменения структуры базы данных.

Если объект, в которую добавляются не завершена (например, при любые объекты **поля** еще не добавлены в коллекцию **полей** **индекс** объекта до добавляется к коллекции **индексов** ) или задать свойства в одном или нескольких неправильные подчиненных объектов, с помощью метода **Append** приводит к ошибке. Например если вы еще не указан тип поля и попытайтесь добавьте объект **поля** в коллекцию **полей** в объекте **TableDef** , с помощью метода **Append** запускает ошибку времени выполнения.


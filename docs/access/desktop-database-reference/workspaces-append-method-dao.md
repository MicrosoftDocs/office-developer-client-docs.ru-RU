---
title: Workspaces.Append Method (DAO)
TOCTitle: Append Method
ms:assetid: 195c26a6-a1d1-40a8-7e7e-13cd632008b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845644(v=office.15)
ms:contentKeyID: 48543498
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d880f681f560a3ae10ddfa41a2fc824d62a46ae8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883437"
---
# <a name="workspacesappend-method-dao"></a>Workspaces.Append Method (DAO)


**Применимо к**: Access 2013, Office 2013

Добавление новой **рабочей области для** семейства сайтов **рабочих областей** .

## <a name="syntax"></a>Синтаксис

*выражение* . Добавление (***объект***)

*выражение* Переменная, которая представляет собой объект- **рабочие области** .

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


---
title: Properties.Append Method (DAO)
TOCTitle: Append Method
ms:assetid: 47f1e24f-975c-3fdc-5c3c-8c91f2920c81
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193232(v=office.15)
ms:contentKeyID: 48544609
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e85ab0bb12f9016f103187aa4c16fd7bf0d2dcba
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883227"
---
# <a name="propertiesappend-method-dao"></a>Properties.Append Method (DAO)


**Применимо к**: Access 2013, Office 2013

Добавляет новое **свойство** в коллекцию **свойств** .

## <a name="syntax"></a>Синтаксис

*выражение* . Добавление (***объект***)

*выражение* Переменная, которая представляет собой объект- **Свойства** .

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


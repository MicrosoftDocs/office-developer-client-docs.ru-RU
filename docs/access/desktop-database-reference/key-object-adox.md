---
title: Объект ключа (ADOX - ссылки для настольных баз данных Access)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f56a90b7accd1b64c9a52e0a7cf5385f83fd10d5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717141"
---
# <a name="key-object-adox"></a>Объект Key (ADOX)


**Применимо к**: Access 2013, Office 2013

Представляет основной, внешний или уникальное ключевое поле из таблицы базы данных.

## <a name="remarks"></a>Замечания

Следующий код создает новый **ключ**.

`Dim obj As New Key`

С помощью свойств и коллекций объекта **ключа** можно выполнить следующие действия.

- Определите ключ с помощью свойства [Name](name-property-adox.md) .

- Определите, является ли ключ основной, внешний или уникальные со свойством [типа](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) .

- Доступ к столбцам базы данных ключа в коллекции [столбцов](columns-collection-adox.md) .

- Укажите имя связанной таблицы с помощью свойства [RelatedTable](relatedtable-property-adox.md) .

- Определите действие, выполняемое на удаление или обновление основного ключа с помощью свойства [DeleteRule](deleterule-property-adox.md) и [UpdateRule](updaterule-property-adox.md) .


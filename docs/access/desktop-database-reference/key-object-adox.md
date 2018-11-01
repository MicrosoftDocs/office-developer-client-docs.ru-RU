---
title: Объект ключа (ADOX - ссылки для настольных баз данных Access)
TOCTitle: Key Object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2edda6dfe7dd9ec28f3eb4cb11714d59806c80e0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871362"
---
# <a name="key-object-adox"></a>Объект ключа (ADOX)


**Применимо к**: Access 2013, Office 2013

Представляет основной, внешний или уникальное ключевое поле из таблицы базы данных.

## <a name="remarks"></a>Замечания

Следующий код создает новый **ключ**.

`Dim obj As New Key`

С помощью свойств и коллекций объекта **ключа** можно выполнить следующие действия.

- Определите ключ с помощью свойства [Name](name-property-adox.md) .

- Определите, является ли ключ основной, внешний или уникальные со свойством [типа](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) .

- Доступ к столбцам базы данных ключа в коллекции [столбцов](columns-collection-adox.md) .

- Укажите имя связанной таблицы с помощью свойства [RelatedTable](relatedtable-property-adox.md) .

- Определите действие, выполняемое на удаление или обновление основного ключа с помощью свойства [DeleteRule](deleterule-property-adox.md) и [UpdateRule](updaterule-property-adox.md) .


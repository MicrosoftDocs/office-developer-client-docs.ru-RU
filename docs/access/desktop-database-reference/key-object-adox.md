---
title: Объект ключа (ADOX - ссылки для настольных баз данных Access)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7722130c76516eaa7dcaf0598a5e1c040e21ba25
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025947"
---
# <a name="key-object-adox"></a>Объект Key (ADOX)


**Применимо к**: Access 2013, Office 2013

Представляет основной, внешний или уникальное ключевое поле из таблицы базы данных.

## <a name="remarks"></a>Примечания

Следующий код создает новый **ключ**.

`Dim obj As New Key`

С помощью свойств и коллекций объекта **ключа** можно выполнить следующие действия.

- Определите ключ с помощью свойства [Name](name-property-adox.md) .

- Определите, является ли ключ основной, внешний или уникальные со свойством [типа](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) .

- Доступ к столбцам базы данных ключа в коллекции [столбцов](columns-collection-adox.md) .

- Укажите имя связанной таблицы с помощью свойства [RelatedTable](relatedtable-property-adox.md) .

- Определите действие, выполняемое на удаление или обновление основного ключа с помощью свойства [DeleteRule](deleterule-property-adox.md) и [UpdateRule](updaterule-property-adox.md) .


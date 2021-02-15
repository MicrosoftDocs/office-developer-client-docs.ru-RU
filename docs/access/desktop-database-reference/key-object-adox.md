---
title: Key Object (ADOX - Access desktop database reference)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f56a90b7accd1b64c9a52e0a7cf5385f83fd10d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290754"
---
# <a name="key-object-adox"></a>Key object (ADOX)


**Область применения**: Access 2013, Office 2013

Представляет поле первичного, внешнего или уникального ключа из таблицы базы данных.

## <a name="remarks"></a>Заметки

Следующий код создает новый **ключ:**

`Dim obj As New Key`

С помощью свойств и коллекций объекта **Key** можно:

- Определите ключ с помощью [свойства Name.](name-property-adox.md)

- Определите, является ли ключ первичным, внешним или уникальным с помощью [свойства Type.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox)

- Доступ к столбцам базы данных ключа с помощью коллекции [Columns.](columns-collection-adox.md)

- Укажите имя связанной таблицы со [свойством RelatedTable.](relatedtable-property-adox.md)

- Определите действие, выполненное при удалении или обновлении первичного ключа, с помощью свойств [DeleteRule](deleterule-property-adox.md) и [UpdateRule.](updaterule-property-adox.md)


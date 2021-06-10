---
title: Объект Index (ADOX)
TOCTitle: Index object (ADOX)
ms:assetid: fe368ab1-e396-4684-d930-18b0ba58a925
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250304(v=office.15)
ms:contentKeyID: 48548929
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 02d12fffa2c766425054e344e9f7d9d7a22cb517
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291777"
---
# <a name="index-object-adox"></a>Объект Index (ADOX)

**Область применения**: Access 2013, Office 2013

Представляет индекс из таблицы баз данных.

## <a name="remarks"></a>Примечания

Следующий код создает новый **индекс:**

`Dim obj As New Index`

С свойствами и коллекциями объекта **Index** можно:

- Определите индекс с [свойством Name.](name-property-adox.md)

- Доступ к столбцам базы данных индекса с помощью коллекции [Столбцы.](columns-collection-adox.md)

- Укажите, должны ли клавиши индекса быть уникальными с [свойством Unique.](unique-property-adox.md)

- Укажите, является ли индекс основным ключом для таблицы с [свойством PrimaryKey.](primarykey-property-adox.md)

- Укажите, имеют ли записи с значениями null в своих полях индекса записи с [свойством IndexNulls.](indexnulls-property-adox.md)

- Укажите, кластерит ли индекс с [свойством Clustered.](clustered-property-adox.md)

- Доступ к свойствам индекса для конкретного поставщика с [коллекцией свойств.](properties-collection-ado.md)


> [!NOTE]
> Ошибка возникает при приложении [](column-object-adox.md) столбца к коллекции **Столбцов**  индекса, если столбец не существует в объекте [Table,](table-object-adox.md) который уже придан в коллекцию [Таблицы.](tables-collection-adox.md) 

Поставщик данных может не поддерживать все свойства объектов **Index.** Ошибка будет возникать, если вы установили значение для свойства, которое не поддерживается поставщиком. Для новых **объектов Index** ошибка возникает при приложении объекта к коллекции. Для существующих объектов ошибка возникает при настройке свойства.

При создании **объектов Index** наличие соответствующего значения по умолчанию для необязательных свойств не гарантирует, что поставщик поддерживает свойство. Дополнительные сведения о свойствах, поддерживаемых поставщиком, см. в документации поставщика.


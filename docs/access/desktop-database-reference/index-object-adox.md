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

Представляет индекс из таблицы базы данных.

## <a name="remarks"></a>Заметки

Следующий код создает новый **индекс:**

`Dim obj As New Index`

С помощью свойств и коллекций объекта **Index** можно:

- Определите индекс с помощью [свойства Name.](name-property-adox.md)

- Доступ к столбцам базы данных индекса с помощью коллекции [Columns.](columns-collection-adox.md)

- Укажите, должны ли ключи индекса быть уникальными с помощью [свойства Unique.](unique-property-adox.md)

- Укажите, является ли индекс первичным ключом для таблицы со [свойством PrimaryKey.](primarykey-property-adox.md)

- Укажите, имеют ли записи со значениями NULL в своих полях индекса записи индекса со свойством [IndexNulls.](indexnulls-property-adox.md)

- Укажите, кластеризация ли индекса с помощью [кластерного](clustered-property-adox.md) свойства.

- Доступ к свойствам индекса для определенного поставщика с помощью коллекции [Properties.](properties-collection-ado.md)


> [!NOTE]
> Ошибка будет возникать при [](column-object-adox.md) приложении столбца к  коллекции **Columns** индекса, если столбец не существует в [объекте Table,](table-object-adox.md) который уже был придан коллекции [Tables.](tables-collection-adox.md) 

Поставщик данных может поддерживать не все свойства объектов **Index.** Ошибка возникает, если вы установили значение для свойства, которое не поддерживается поставщиком. Для новых **объектов Index** ошибка возникает, когда объект будет appended к коллекции. Для существующих объектов ошибка возникает при установке свойства.

При создании **объектов Index** наличие соответствующего значения по умолчанию для необязательного свойства не гарантирует, что ваш поставщик поддерживает это свойство. Дополнительные сведения о свойствах, поддерживаемые поставщиком, см. в документации поставщика.


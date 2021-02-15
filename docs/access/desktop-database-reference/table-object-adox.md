---
title: Объект Table (ADOX)
TOCTitle: Table object (ADOX)
ms:assetid: 53a3e2f9-4ec0-8fed-d482-4f995921587b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249273(v=office.15)
ms:contentKeyID: 48544874
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6475621d711881b0187031aa037c8284e155546d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314408"
---
# <a name="table-object-adox"></a>Объект Table (ADOX)

**Область применения**: Access 2013, Office 2013

Представляет таблицу базы данных, включаемую столбцы, индексы и ключи.

## <a name="remarks"></a>Заметки

Следующий код создает новую **таблицу:**

`Dim obj As New Table`

С помощью свойств и коллекций объекта **Table** можно:

- Определите таблицу с помощью [свойства Name.](name-property-adox.md)

- Определите тип таблицы со [свойством Type.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox)

- Доступ к столбцам базы данных таблицы с помощью коллекции [Columns.](columns-collection-adox.md)

- Доступ к индексам таблицы с помощью коллекции [Indexes.](indexes-collection-adox.md)

- Доступ к ключам таблицы с помощью коллекции [Keys.](keys-collection-adox.md)

- Укажите [каталог,](catalog-object-adox.md) который является владельцем таблицы, со [свойством ParentCatalog.](parentcatalog-property-adox.md)

- Сведения о дате возврата [со свойствами DateCreated](datecreated-property-adox.md) и [DateModified.](datemodified-property-adox.md)

- Доступ к свойствам таблицы для определенного поставщика с помощью коллекции [Properties.](properties-collection-ado.md)


> [!NOTE]
> Поставщик данных может поддерживать не все свойства объектов **Table.** Ошибка возникает, если вы установили значение для свойства, которое поставщик не поддерживает. Для новых **объектов Table** ошибка возникает, когда объект будет appended к коллекции. Для существующих объектов ошибка возникает при установке свойства.

При создании **объектов Table** наличие соответствующего значения по умолчанию для необязательного свойства не гарантирует, что ваш поставщик поддерживает это свойство. Дополнительные сведения о свойствах, поддерживаемые поставщиком, см. в документации поставщика.


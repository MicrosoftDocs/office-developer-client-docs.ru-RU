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

Представляет таблицу баз данных, включаемую столбцы, индексы и клавиши.

## <a name="remarks"></a>Примечания

Следующий код создает новую **таблицу:**

`Dim obj As New Table`

С свойствами и коллекциями объекта **Table** можно:

- Определите таблицу с [свойством Name.](name-property-adox.md)

- Определите тип таблицы с [свойством Type.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox)

- Доступ к столбцам базы данных таблицы с помощью коллекции [Столбцы.](columns-collection-adox.md)

- Доступ к индексам таблицы с помощью коллекции [Indexes.](indexes-collection-adox.md)

- Доступ к клавишам таблицы с помощью коллекции [Ключей.](keys-collection-adox.md)

- Укажите [каталог,](catalog-object-adox.md) который владеет таблицей с [свойством ParentCatalog.](parentcatalog-property-adox.md)

- Сведения о дате возврата со свойствами [DateCreated](datecreated-property-adox.md) и [DateModified.](datemodified-property-adox.md)

- Доступ к свойствам таблицы, определенной для поставщика, с [коллекцией свойств.](properties-collection-ado.md)


> [!NOTE]
> Поставщик данных может не поддерживать все свойства объектов **Table.** Ошибка возникает, если установлено значение для свойства, которое поставщик не поддерживает. Для новых **объектов Таблицы** ошибка возникает при приложении объекта к коллекции. Для существующих объектов ошибка возникает при настройке свойства.

При создании **объектов Table** наличие соответствующего значения по умолчанию для необязательных свойств не гарантирует, что поставщик поддерживает свойство. Дополнительные сведения о свойствах, поддерживаемых поставщиком, см. в документации поставщика.


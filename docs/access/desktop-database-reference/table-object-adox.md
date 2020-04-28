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

Представляет таблицу базы данных, в том числе столбцы, индексы и ключи.

## <a name="remarks"></a>Примечания

В приведенном ниже коде создается новая **Таблица**:

`Dim obj As New Table`

С помощью свойств и коллекций объекта **Table** можно выполнять следующие действия:

- Определите таблицу со свойством [Name](name-property-adox.md) .

- Определите тип таблицы со свойством [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox) .

- Доступ к столбцам базы данных таблицы с помощью коллекции [Columns](columns-collection-adox.md) .

- Доступ к индексам таблицы с помощью коллекции [indexes](indexes-collection-adox.md) .

- Доступ к ключам таблицы с помощью коллекции [Keys](keys-collection-adox.md) .

- Укажите [Каталог](catalog-object-adox.md) , который владеет таблицей, с помощью свойства [ParentCatalog](parentcatalog-property-adox.md) .

- Сведения о дате возврата с помощью свойств [DateCreated](datecreated-property-adox.md) и [DateModified](datemodified-property-adox.md) .

- Доступ к свойствам таблицы, зависящей от поставщика, с коллекцией [свойств](properties-collection-ado.md) .


> [!NOTE]
> Поставщик данных может не поддерживать все свойства объектов **Table** . Если для свойства задано значение, которое не поддерживается поставщиком, произойдет ошибка. Для новых объектов **Table** ошибка будет возникать при добавлении объекта в коллекцию. Для существующих объектов ошибка будет возникать при задании свойства.

При создании объектов **Table** наличие соответствующего значения по умолчанию для дополнительного свойства не гарантирует, что поставщик не поддерживает это свойство. Для получения дополнительных сведений о свойствах, поддерживаемых поставщиком, обратитесь к документации поставщика.


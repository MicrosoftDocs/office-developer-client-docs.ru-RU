---
title: Объект Column (ADOX)
TOCTitle: Column object (ADOX)
ms:assetid: ad38c2df-f704-0599-4b7a-8556e430ba46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249811(v=office.15)
ms:contentKeyID: 48547034
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 188f70d32237385cd82979589aecb989f18748b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296250"
---
# <a name="column-object-adox"></a>Объект Column (ADOX)


**Область применения**: Access 2013, Office 2013

Представляет столбец из таблицы, индекса или ключа.

## <a name="remarks"></a>Замечания

Следующий код создает новый **столбец**:

`Dim obj As New Column`

С помощью свойств и коллекций объекта **Column** можно выполнять следующие действия:

  - Определите столбец со свойством [Name](name-property-adox.md) .

  - Укажите тип данных столбца с помощью свойства [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) .

  - Определите, является ли столбец фиксированной длиной, или может ли он содержать значения NULL с помощью [](attributes-property-adox.md) свойства Attributes.

  - Указание максимального размера столбца с помощью свойства [DefinedSize](definedsize-property-adox.md) .

  - Для числовых значений данных укажите масштаб с помощью свойства [NumericScale](numericscale-property-adox.md) .

  - Для числового значения данных укажите максимальную точность со свойством [Precision](precision-property-adox.md) .

  - Укажите [Каталог](catalog-object-adox.md) , который владеет столбцом, с помощью свойства [ParentCatalog](parentcatalog-property-adox.md) .

  - Для ключевых столбцов укажите имя связанного столбца в связанной таблице с помощью свойства [RelatedColumn](relatedcolumn-property-adox.md) .

  - Для столбцов индекса укажите, используется ли порядок сортировки по возрастанию или убыванию с помощью свойства [SortOrder](sortorder-property-adox.md) .

  - Доступ к свойствам, зависящим от поставщика, с коллекцией [свойств](properties-collection-ado.md) .


> [!NOTE]
> Поставщик данных может поддерживать не все свойства объектов **Column** . Если для свойства задано значение, которое не поддерживается поставщиком, произойдет ошибка. Для новых **** объектов Columns ошибка будет возникать при добавлении объекта в коллекцию. Для существующих объектов ошибка будет возникать при задании свойства.
> 
> При создании объектов **Column** наличие соответствующего значения по умолчанию для дополнительного свойства не гарантирует, что поставщик не поддерживает это свойство. Для получения дополнительных сведений о свойствах, поддерживаемых поставщиком, обратитесь к документации поставщика.


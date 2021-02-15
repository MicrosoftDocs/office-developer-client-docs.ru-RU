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

## <a name="remarks"></a>Заметки

Следующий код создает новый **столбец:**

`Dim obj As New Column`

С помощью свойств и коллекций объекта **Column** можно:

  - Определите столбец с помощью [свойства Name.](name-property-adox.md)

  - Укажите тип данных столбца со [свойством Type.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox)

  - Определите, имеет ли столбец фиксированную длину или может ли он содержать значения null со [свойством Attributes.](attributes-property-adox.md)

  - Укажите максимальный размер столбца с помощью свойства [DefinedSize.](definedsize-property-adox.md)

  - Для численных значений данных укажите масштаб с помощью свойства [NumericScale.](numericscale-property-adox.md)

  - Для числимых значений данных укажите максимальную точность с помощью [свойства Precision.](precision-property-adox.md)

  - Укажите [каталог,](catalog-object-adox.md) который является владельцем столбца, со [свойством ParentCatalog.](parentcatalog-property-adox.md)

  - Для ключевых столбцов укажите имя связанного столбца в связанной таблице со [свойством RelatedColumn.](relatedcolumn-property-adox.md)

  - Для столбцов индекса укажите, является ли порядок сортировки по возрастанию или убыванию с помощью свойства [SortOrder.](sortorder-property-adox.md)

  - Доступ к свойствам поставщика с помощью коллекции [Properties.](properties-collection-ado.md)


> [!NOTE]
> Поставщик данных может поддерживать не все свойства объектов **Column.** Ошибка возникает, если вы установили значение для свойства, которое поставщик не поддерживает. Для новых **объектов Column** ошибка возникает, когда объект будет сдан в коллекцию. Для существующих объектов ошибка возникает при установке свойства.
> 
> При создании **объектов Column** наличие соответствующего значения по умолчанию для необязательного свойства не гарантирует, что поставщик поддерживает это свойство. Дополнительные сведения о свойствах, поддерживаемые поставщиком, см. в документации поставщика.


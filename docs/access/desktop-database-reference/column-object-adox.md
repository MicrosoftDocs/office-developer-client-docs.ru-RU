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

## <a name="remarks"></a>Примечания

Следующий код создает новый **столбец:**

`Dim obj As New Column`

С свойствами и коллекциями объекта **Column** можно:

  - Определите столбец с [свойством Name.](name-property-adox.md)

  - Укажите тип данных столбца с [свойством Type.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox)

  - Определите, является ли столбец фиксированной длины или может содержать значения null с [свойством Атрибуты.](attributes-property-adox.md)

  - Укажите максимальный размер столбца с [свойством DefinedSize.](definedsize-property-adox.md)

  - Для численных значений данных укажите масштаб с [свойством NumericScale.](numericscale-property-adox.md)

  - Для численного значения данных укажите максимальную точность с [свойством Precision.](precision-property-adox.md)

  - Укажите [каталог,](catalog-object-adox.md) который владеет столбцом с [свойством ParentCatalog.](parentcatalog-property-adox.md)

  - Для ключевых столбцов укажите имя связанного столбца в связанной таблице с [свойством RelatedColumn.](relatedcolumn-property-adox.md)

  - Для столбцов индексов укажите, является ли порядок сортировки восходящим или убывательным с [свойством SortOrder.](sortorder-property-adox.md)

  - Доступ к свойствам, определенным поставщикам, с [коллекцией свойств.](properties-collection-ado.md)


> [!NOTE]
> Не все свойства объектов **Column** могут поддерживаться поставщиком данных. Ошибка возникает, если установлено значение для свойства, которое поставщик не поддерживает. Для новых **объектов Column** ошибка возникает при приложении объекта к коллекции. Для существующих объектов ошибка возникает при настройке свойства.
> 
> При создании **объектов Column** наличие соответствующего значения по умолчанию для необязательных свойств не гарантирует, что поставщик поддерживает свойство. Дополнительные сведения о свойствах, поддерживаемых поставщиком, см. в документации поставщика.


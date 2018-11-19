---
title: Объект Column (ADOX)
TOCTitle: Column object (ADOX)
ms:assetid: ad38c2df-f704-0599-4b7a-8556e430ba46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249811(v=office.15)
ms:contentKeyID: 48547034
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1b7ebd312727e1dc5071964cf1125d1c76bec4d
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026011"
---
# <a name="column-object-adox"></a>Объект Column (ADOX)


**Применимо к**: Access 2013, Office 2013

Представляет столбец из таблицы, индекса или ключа.

## <a name="remarks"></a>Примечания

В следующем коде создается новый **столбец**:

`Dim obj As New Column`

С помощью свойств и коллекций объекта **столбца** можно выполнить следующие действия.

  - Определите столбец с помощью свойства [Name](name-property-adox.md) .

  - Задать тип данных столбца с помощью [типа](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) свойства.

  - Определите, если столбец является фиксированной длины или он может содержать значение null, значения с помощью свойства [атрибуты](attributes-property-adox.md) .

  - Укажите максимальный размер столбца с помощью свойства [DefinedSize](definedsize-property-adox.md) .

  - Для значений числовые данные укажите масштаб со свойством [NumericScale](numericscale-property-adox.md) .

  - Для числового значения данных укажите максимальной точности со свойством [точности](precision-property-adox.md) .

  - Укажите [каталог](catalog-object-adox.md) , которому принадлежит столбец со свойством [ParentCatalog](parentcatalog-property-adox.md) .

  - Для ключевых столбцов укажите имя столбца, связанных с ними в связанные таблицы со свойством [RelatedColumn](relatedcolumn-property-adox.md) .

  - Для столбцов индекса укажите ли порядок сортировки по возрастанию или по убыванию со свойством [SortOrder](sortorder-property-adox.md) .

  - Доступа к свойствам конкретного поставщика с набором [свойств](properties-collection-ado.md) .


> [!NOTE]
> Не все свойства **столбца** объектов могут поддерживаться поставщика данных. Если выбрать значение для свойства, которое не поддерживает поставщик, произойдет ошибка. Для новых объектов **столбца** ошибка возникает при объект добавляется к коллекции. Для существующих объектов ошибка возникает, когда для свойства.
> 
> При создании **столбца** объектов, наличие значения по умолчанию для необязательные свойства не гарантирует, что ваш поставщик поддерживает свойство. Для получения дополнительных сведений о свойствах ваш поставщик поддерживает обратитесь к документации поставщика.


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
# <a name="column-object-adox"></a><span data-ttu-id="95e5b-102">Объект Column (ADOX)</span><span class="sxs-lookup"><span data-stu-id="95e5b-102">Column object (ADOX)</span></span>


<span data-ttu-id="95e5b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="95e5b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95e5b-104">Представляет столбец из таблицы, индекса или ключа.</span><span class="sxs-lookup"><span data-stu-id="95e5b-104">Represents a column from a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="95e5b-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="95e5b-105">Remarks</span></span>

<span data-ttu-id="95e5b-106">В следующем коде создается новый **столбец**:</span><span class="sxs-lookup"><span data-stu-id="95e5b-106">The following code creates a new **Column**:</span></span>

`Dim obj As New Column`

<span data-ttu-id="95e5b-107">С помощью свойств и коллекций объекта **столбца** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="95e5b-107">With the properties and collections of a **Column** object, you can:</span></span>

  - <span data-ttu-id="95e5b-108">Определите столбец с помощью свойства [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="95e5b-108">Identify the column with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="95e5b-109">Задать тип данных столбца с помощью [типа](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) свойства.</span><span class="sxs-lookup"><span data-stu-id="95e5b-109">Specify the data type of the column with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property.</span></span>

  - <span data-ttu-id="95e5b-110">Определите, если столбец является фиксированной длины или он может содержать значение null, значения с помощью свойства [атрибуты](attributes-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="95e5b-110">Determine if the column is fixed-length, or if it can contain null values with the [Attributes](attributes-property-adox.md) property.</span></span>

  - <span data-ttu-id="95e5b-111">Укажите максимальный размер столбца с помощью свойства [DefinedSize](definedsize-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="95e5b-111">Specify the maximum size of the column with the [DefinedSize](definedsize-property-adox.md) property.</span></span>

  - <span data-ttu-id="95e5b-112">Для значений числовые данные укажите масштаб со свойством [NumericScale](numericscale-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="95e5b-112">For numeric data values, specify the scale with the [NumericScale](numericscale-property-adox.md) property.</span></span>

  - <span data-ttu-id="95e5b-113">Для числового значения данных укажите максимальной точности со свойством [точности](precision-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="95e5b-113">For numeric data value, specify the maximum precision with the [Precision](precision-property-adox.md) property.</span></span>

  - <span data-ttu-id="95e5b-114">Укажите [каталог](catalog-object-adox.md) , которому принадлежит столбец со свойством [ParentCatalog](parentcatalog-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="95e5b-114">Specify the [Catalog](catalog-object-adox.md) that owns the column with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

  - <span data-ttu-id="95e5b-115">Для ключевых столбцов укажите имя столбца, связанных с ними в связанные таблицы со свойством [RelatedColumn](relatedcolumn-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="95e5b-115">For key columns, specify the name of the related column in the related table with the [RelatedColumn](relatedcolumn-property-adox.md) property.</span></span>

  - <span data-ttu-id="95e5b-116">Для столбцов индекса укажите ли порядок сортировки по возрастанию или по убыванию со свойством [SortOrder](sortorder-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="95e5b-116">For index columns, specify whether the sort order is ascending or descending with the [SortOrder](sortorder-property-adox.md) property.</span></span>

  - <span data-ttu-id="95e5b-117">Доступа к свойствам конкретного поставщика с набором [свойств](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="95e5b-117">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="95e5b-118">Не все свойства **столбца** объектов могут поддерживаться поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="95e5b-118">Not all properties of **Column** objects may be supported by your data provider.</span></span> <span data-ttu-id="95e5b-119">Если выбрать значение для свойства, которое не поддерживает поставщик, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="95e5b-119">An error will occur if you have set a value for a property that the provider does not support.</span></span> <span data-ttu-id="95e5b-120">Для новых объектов **столбца** ошибка возникает при объект добавляется к коллекции.</span><span class="sxs-lookup"><span data-stu-id="95e5b-120">For new **Column** objects, the error will occur when the object is appended to the collection.</span></span> <span data-ttu-id="95e5b-121">Для существующих объектов ошибка возникает, когда для свойства.</span><span class="sxs-lookup"><span data-stu-id="95e5b-121">For existing objects, the error will occur when setting the property.</span></span>
> 
> <span data-ttu-id="95e5b-122">При создании **столбца** объектов, наличие значения по умолчанию для необязательные свойства не гарантирует, что ваш поставщик поддерживает свойство.</span><span class="sxs-lookup"><span data-stu-id="95e5b-122">When creating **Column** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</span></span> <span data-ttu-id="95e5b-123">Для получения дополнительных сведений о свойствах ваш поставщик поддерживает обратитесь к документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="95e5b-123">For more information about which properties your provider supports, see your provider documentation.</span></span>


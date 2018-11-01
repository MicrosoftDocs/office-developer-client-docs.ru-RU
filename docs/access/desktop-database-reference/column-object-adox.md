---
title: Объект столбца (ADOX)
TOCTitle: Column Object (ADOX)
ms:assetid: ad38c2df-f704-0599-4b7a-8556e430ba46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249811(v=office.15)
ms:contentKeyID: 48547034
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28ae0f69303db5569b97799d8a77ca66828e2035
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879622"
---
# <a name="column-object-adox"></a><span data-ttu-id="6d01d-102">Объект столбца (ADOX)</span><span class="sxs-lookup"><span data-stu-id="6d01d-102">Column Object (ADOX)</span></span>


<span data-ttu-id="6d01d-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d01d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d01d-104">Представляет столбец из таблицы, индекса или ключа.</span><span class="sxs-lookup"><span data-stu-id="6d01d-104">Represents a column from a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d01d-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="6d01d-105">Remarks</span></span>

<span data-ttu-id="6d01d-106">В следующем коде создается новый **столбец**:</span><span class="sxs-lookup"><span data-stu-id="6d01d-106">The following code creates a new **Column**:</span></span>

`Dim obj As New Column`

<span data-ttu-id="6d01d-107">С помощью свойств и коллекций объекта **столбца** можно выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6d01d-107">With the properties and collections of a **Column** object, you can:</span></span>

  - <span data-ttu-id="6d01d-108">Определите столбец с помощью свойства [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="6d01d-108">Identify the column with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="6d01d-109">Задать тип данных столбца с помощью [типа](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) свойства.</span><span class="sxs-lookup"><span data-stu-id="6d01d-109">Specify the data type of the column with the [Type](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) property.</span></span>

  - <span data-ttu-id="6d01d-110">Определите, если столбец является фиксированной длины или он может содержать значение null, значения с помощью свойства [атрибуты](attributes-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="6d01d-110">Determine if the column is fixed-length, or if it can contain null values with the [Attributes](attributes-property-adox.md) property.</span></span>

  - <span data-ttu-id="6d01d-111">Укажите максимальный размер столбца с помощью свойства [DefinedSize](definedsize-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="6d01d-111">Specify the maximum size of the column with the [DefinedSize](definedsize-property-adox.md) property.</span></span>

  - <span data-ttu-id="6d01d-112">Для значений числовые данные укажите масштаб со свойством [NumericScale](numericscale-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="6d01d-112">For numeric data values, specify the scale with the [NumericScale](numericscale-property-adox.md) property.</span></span>

  - <span data-ttu-id="6d01d-113">Для числового значения данных укажите максимальной точности со свойством [точности](precision-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="6d01d-113">For numeric data value, specify the maximum precision with the [Precision](precision-property-adox.md) property.</span></span>

  - <span data-ttu-id="6d01d-114">Укажите [каталог](catalog-object-adox.md) , которому принадлежит столбец со свойством [ParentCatalog](parentcatalog-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="6d01d-114">Specify the [Catalog](catalog-object-adox.md) that owns the column with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

  - <span data-ttu-id="6d01d-115">Для ключевых столбцов укажите имя столбца, связанных с ними в связанные таблицы со свойством [RelatedColumn](relatedcolumn-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="6d01d-115">For key columns, specify the name of the related column in the related table with the [RelatedColumn](relatedcolumn-property-adox.md) property.</span></span>

  - <span data-ttu-id="6d01d-116">Для столбцов индекса укажите ли порядок сортировки по возрастанию или по убыванию со свойством [SortOrder](sortorder-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="6d01d-116">For index columns, specify whether the sort order is ascending or descending with the [SortOrder](sortorder-property-adox.md) property.</span></span>

  - <span data-ttu-id="6d01d-117">Доступа к свойствам конкретного поставщика с набором [свойств](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="6d01d-117">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="6d01d-118">Не все свойства **столбца** объектов могут поддерживаться поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="6d01d-118">Not all properties of **Column** objects may be supported by your data provider.</span></span> <span data-ttu-id="6d01d-119">Если выбрать значение для свойства, которое не поддерживает поставщик, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="6d01d-119">An error will occur if you have set a value for a property that the provider does not support.</span></span> <span data-ttu-id="6d01d-120">Для новых объектов **столбца** ошибка возникает при объект добавляется к коллекции.</span><span class="sxs-lookup"><span data-stu-id="6d01d-120">For new **Column** objects, the error will occur when the object is appended to the collection.</span></span> <span data-ttu-id="6d01d-121">Для существующих объектов ошибка возникает, когда для свойства.</span><span class="sxs-lookup"><span data-stu-id="6d01d-121">For existing objects, the error will occur when setting the property.</span></span>
> 
> <span data-ttu-id="6d01d-122">При создании **столбца** объектов, наличие значения по умолчанию для необязательные свойства не гарантирует, что ваш поставщик поддерживает свойство.</span><span class="sxs-lookup"><span data-stu-id="6d01d-122">When creating **Column** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</span></span> <span data-ttu-id="6d01d-123">Для получения дополнительных сведений о свойствах ваш поставщик поддерживает обратитесь к документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="6d01d-123">For more information about which properties your provider supports, see your provider documentation.</span></span>


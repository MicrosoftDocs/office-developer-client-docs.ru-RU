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
# <a name="column-object-adox"></a><span data-ttu-id="e2276-102">Объект Column (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e2276-102">Column object (ADOX)</span></span>


<span data-ttu-id="e2276-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2276-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e2276-104">Представляет столбец из таблицы, индекса или ключа.</span><span class="sxs-lookup"><span data-stu-id="e2276-104">Represents a column from a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2276-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="e2276-105">Remarks</span></span>

<span data-ttu-id="e2276-106">Следующий код создает новый **столбец**:</span><span class="sxs-lookup"><span data-stu-id="e2276-106">The following code creates a new **Column**:</span></span>

`Dim obj As New Column`

<span data-ttu-id="e2276-107">С помощью свойств и коллекций объекта **Column** можно выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="e2276-107">With the properties and collections of a **Column** object, you can:</span></span>

  - <span data-ttu-id="e2276-108">Определите столбец со свойством [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="e2276-108">Identify the column with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="e2276-109">Укажите тип данных столбца с помощью свойства [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) .</span><span class="sxs-lookup"><span data-stu-id="e2276-109">Specify the data type of the column with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property.</span></span>

  - <span data-ttu-id="e2276-110">Определите, является ли столбец фиксированной длиной, или может ли он содержать значения NULL с помощью свойства [Attributes](attributes-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="e2276-110">Determine if the column is fixed-length, or if it can contain null values with the [Attributes](attributes-property-adox.md) property.</span></span>

  - <span data-ttu-id="e2276-111">Указание максимального размера столбца с помощью свойства [DefinedSize](definedsize-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="e2276-111">Specify the maximum size of the column with the [DefinedSize](definedsize-property-adox.md) property.</span></span>

  - <span data-ttu-id="e2276-112">Для числовых значений данных укажите масштаб с помощью свойства [NumericScale](numericscale-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="e2276-112">For numeric data values, specify the scale with the [NumericScale](numericscale-property-adox.md) property.</span></span>

  - <span data-ttu-id="e2276-113">Для числового значения данных укажите максимальную точность со свойством [Precision](precision-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="e2276-113">For numeric data value, specify the maximum precision with the [Precision](precision-property-adox.md) property.</span></span>

  - <span data-ttu-id="e2276-114">Укажите [Каталог](catalog-object-adox.md) , который владеет столбцом, с помощью свойства [ParentCatalog](parentcatalog-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="e2276-114">Specify the [Catalog](catalog-object-adox.md) that owns the column with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

  - <span data-ttu-id="e2276-115">Для ключевых столбцов укажите имя связанного столбца в связанной таблице с помощью свойства [RelatedColumn](relatedcolumn-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="e2276-115">For key columns, specify the name of the related column in the related table with the [RelatedColumn](relatedcolumn-property-adox.md) property.</span></span>

  - <span data-ttu-id="e2276-116">Для столбцов индекса укажите, используется ли порядок сортировки по возрастанию или убыванию с помощью свойства [SortOrder](sortorder-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="e2276-116">For index columns, specify whether the sort order is ascending or descending with the [SortOrder](sortorder-property-adox.md) property.</span></span>

  - <span data-ttu-id="e2276-117">Доступ к свойствам, зависящим от поставщика, с коллекцией [свойств](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e2276-117">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="e2276-118">Поставщик данных может поддерживать не все свойства объектов **Column** .</span><span class="sxs-lookup"><span data-stu-id="e2276-118">Not all properties of **Column** objects may be supported by your data provider.</span></span> <span data-ttu-id="e2276-119">Если для свойства задано значение, которое не поддерживается поставщиком, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="e2276-119">An error will occur if you have set a value for a property that the provider does not support.</span></span> <span data-ttu-id="e2276-120">Для новых объектов **Columns** ошибка будет возникать при добавлении объекта в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="e2276-120">For new **Column** objects, the error will occur when the object is appended to the collection.</span></span> <span data-ttu-id="e2276-121">Для существующих объектов ошибка будет возникать при задании свойства.</span><span class="sxs-lookup"><span data-stu-id="e2276-121">For existing objects, the error will occur when setting the property.</span></span>
> 
> <span data-ttu-id="e2276-122">При создании объектов **Column** наличие соответствующего значения по умолчанию для дополнительного свойства не гарантирует, что поставщик не поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="e2276-122">When creating **Column** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</span></span> <span data-ttu-id="e2276-123">Для получения дополнительных сведений о свойствах, поддерживаемых поставщиком, обратитесь к документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="e2276-123">For more information about which properties your provider supports, see your provider documentation.</span></span>


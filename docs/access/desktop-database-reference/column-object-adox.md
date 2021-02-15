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
# <a name="column-object-adox"></a><span data-ttu-id="c093e-102">Объект Column (ADOX)</span><span class="sxs-lookup"><span data-stu-id="c093e-102">Column object (ADOX)</span></span>


<span data-ttu-id="c093e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c093e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c093e-104">Представляет столбец из таблицы, индекса или ключа.</span><span class="sxs-lookup"><span data-stu-id="c093e-104">Represents a column from a table, index, or key.</span></span>

## <a name="remarks"></a><span data-ttu-id="c093e-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="c093e-105">Remarks</span></span>

<span data-ttu-id="c093e-106">Следующий код создает новый **столбец:**</span><span class="sxs-lookup"><span data-stu-id="c093e-106">The following code creates a new **Column**:</span></span>

`Dim obj As New Column`

<span data-ttu-id="c093e-107">С помощью свойств и коллекций объекта **Column** можно:</span><span class="sxs-lookup"><span data-stu-id="c093e-107">With the properties and collections of a **Column** object, you can:</span></span>

  - <span data-ttu-id="c093e-108">Определите столбец с помощью [свойства Name.](name-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="c093e-108">Identify the column with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="c093e-109">Укажите тип данных столбца со [свойством Type.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox)</span><span class="sxs-lookup"><span data-stu-id="c093e-109">Specify the data type of the column with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) property.</span></span>

  - <span data-ttu-id="c093e-110">Определите, имеет ли столбец фиксированную длину или может ли он содержать значения null со [свойством Attributes.](attributes-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="c093e-110">Determine if the column is fixed-length, or if it can contain null values with the [Attributes](attributes-property-adox.md) property.</span></span>

  - <span data-ttu-id="c093e-111">Укажите максимальный размер столбца с помощью свойства [DefinedSize.](definedsize-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="c093e-111">Specify the maximum size of the column with the [DefinedSize](definedsize-property-adox.md) property.</span></span>

  - <span data-ttu-id="c093e-112">Для численных значений данных укажите масштаб с помощью свойства [NumericScale.](numericscale-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="c093e-112">For numeric data values, specify the scale with the [NumericScale](numericscale-property-adox.md) property.</span></span>

  - <span data-ttu-id="c093e-113">Для числимых значений данных укажите максимальную точность с помощью [свойства Precision.](precision-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="c093e-113">For numeric data value, specify the maximum precision with the [Precision](precision-property-adox.md) property.</span></span>

  - <span data-ttu-id="c093e-114">Укажите [каталог,](catalog-object-adox.md) который является владельцем столбца, со [свойством ParentCatalog.](parentcatalog-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="c093e-114">Specify the [Catalog](catalog-object-adox.md) that owns the column with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

  - <span data-ttu-id="c093e-115">Для ключевых столбцов укажите имя связанного столбца в связанной таблице со [свойством RelatedColumn.](relatedcolumn-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="c093e-115">For key columns, specify the name of the related column in the related table with the [RelatedColumn](relatedcolumn-property-adox.md) property.</span></span>

  - <span data-ttu-id="c093e-116">Для столбцов индекса укажите, является ли порядок сортировки по возрастанию или убыванию с помощью свойства [SortOrder.](sortorder-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="c093e-116">For index columns, specify whether the sort order is ascending or descending with the [SortOrder](sortorder-property-adox.md) property.</span></span>

  - <span data-ttu-id="c093e-117">Доступ к свойствам поставщика с помощью коллекции [Properties.](properties-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="c093e-117">Access provider-specific properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="c093e-118">Поставщик данных может поддерживать не все свойства объектов **Column.**</span><span class="sxs-lookup"><span data-stu-id="c093e-118">Not all properties of **Column** objects may be supported by your data provider.</span></span> <span data-ttu-id="c093e-119">Ошибка возникает, если вы установили значение для свойства, которое поставщик не поддерживает.</span><span class="sxs-lookup"><span data-stu-id="c093e-119">An error will occur if you have set a value for a property that the provider does not support.</span></span> <span data-ttu-id="c093e-120">Для новых **объектов Column** ошибка возникает, когда объект будет сдан в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="c093e-120">For new **Column** objects, the error will occur when the object is appended to the collection.</span></span> <span data-ttu-id="c093e-121">Для существующих объектов ошибка возникает при установке свойства.</span><span class="sxs-lookup"><span data-stu-id="c093e-121">For existing objects, the error will occur when setting the property.</span></span>
> 
> <span data-ttu-id="c093e-122">При создании **объектов Column** наличие соответствующего значения по умолчанию для необязательного свойства не гарантирует, что поставщик поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="c093e-122">When creating **Column** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</span></span> <span data-ttu-id="c093e-123">Дополнительные сведения о свойствах, поддерживаемые поставщиком, см. в документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="c093e-123">For more information about which properties your provider supports, see your provider documentation.</span></span>


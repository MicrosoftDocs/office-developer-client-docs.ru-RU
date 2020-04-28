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
# <a name="table-object-adox"></a><span data-ttu-id="72b79-102">Объект Table (ADOX)</span><span class="sxs-lookup"><span data-stu-id="72b79-102">Table object (ADOX)</span></span>

<span data-ttu-id="72b79-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="72b79-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="72b79-104">Представляет таблицу базы данных, в том числе столбцы, индексы и ключи.</span><span class="sxs-lookup"><span data-stu-id="72b79-104">Represents a database table including columns, indexes, and keys.</span></span>

## <a name="remarks"></a><span data-ttu-id="72b79-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="72b79-105">Remarks</span></span>

<span data-ttu-id="72b79-106">В приведенном ниже коде создается новая **Таблица**:</span><span class="sxs-lookup"><span data-stu-id="72b79-106">The following code creates a new **Table**:</span></span>

`Dim obj As New Table`

<span data-ttu-id="72b79-107">С помощью свойств и коллекций объекта **Table** можно выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="72b79-107">With the properties and collections of a **Table** object, you can:</span></span>

- <span data-ttu-id="72b79-108">Определите таблицу со свойством [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="72b79-108">Identify the table with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="72b79-109">Определите тип таблицы со свойством [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox) .</span><span class="sxs-lookup"><span data-stu-id="72b79-109">Determine the type of table with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox) property.</span></span>

- <span data-ttu-id="72b79-110">Доступ к столбцам базы данных таблицы с помощью коллекции [Columns](columns-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="72b79-110">Access the database columns of the table with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="72b79-111">Доступ к индексам таблицы с помощью коллекции [indexes](indexes-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="72b79-111">Access the indexes of the table with the [Indexes](indexes-collection-adox.md) collection.</span></span>

- <span data-ttu-id="72b79-112">Доступ к ключам таблицы с помощью коллекции [Keys](keys-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="72b79-112">Access the keys of the table with the [Keys](keys-collection-adox.md) collection.</span></span>

- <span data-ttu-id="72b79-113">Укажите [Каталог](catalog-object-adox.md) , который владеет таблицей, с помощью свойства [ParentCatalog](parentcatalog-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="72b79-113">Specify the [Catalog](catalog-object-adox.md) that owns the table with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

- <span data-ttu-id="72b79-114">Сведения о дате возврата с помощью свойств [DateCreated](datecreated-property-adox.md) и [DateModified](datemodified-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="72b79-114">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

- <span data-ttu-id="72b79-115">Доступ к свойствам таблицы, зависящей от поставщика, с коллекцией [свойств](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="72b79-115">Access provider-specific table properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="72b79-116">Поставщик данных может не поддерживать все свойства объектов **Table** .</span><span class="sxs-lookup"><span data-stu-id="72b79-116">Your data provider may not support all properties of **Table** objects.</span></span> <span data-ttu-id="72b79-117">Если для свойства задано значение, которое не поддерживается поставщиком, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="72b79-117">An error will occur if you have set a value for a property that the provider does not support.</span></span> <span data-ttu-id="72b79-118">Для новых объектов **Table** ошибка будет возникать при добавлении объекта в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="72b79-118">For new **Table** objects, the error will occur when the object is appended to the collection.</span></span> <span data-ttu-id="72b79-119">Для существующих объектов ошибка будет возникать при задании свойства.</span><span class="sxs-lookup"><span data-stu-id="72b79-119">For existing objects, the error will occur when setting the property.</span></span>

<span data-ttu-id="72b79-120">При создании объектов **Table** наличие соответствующего значения по умолчанию для дополнительного свойства не гарантирует, что поставщик не поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="72b79-120">When creating **Table** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</span></span> <span data-ttu-id="72b79-121">Для получения дополнительных сведений о свойствах, поддерживаемых поставщиком, обратитесь к документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="72b79-121">For more information about which properties your provider supports, see your provider documentation.</span></span>


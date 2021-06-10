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
# <a name="table-object-adox"></a><span data-ttu-id="0746c-102">Объект Table (ADOX)</span><span class="sxs-lookup"><span data-stu-id="0746c-102">Table object (ADOX)</span></span>

<span data-ttu-id="0746c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0746c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0746c-104">Представляет таблицу баз данных, включаемую столбцы, индексы и клавиши.</span><span class="sxs-lookup"><span data-stu-id="0746c-104">Represents a database table including columns, indexes, and keys.</span></span>

## <a name="remarks"></a><span data-ttu-id="0746c-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="0746c-105">Remarks</span></span>

<span data-ttu-id="0746c-106">Следующий код создает новую **таблицу:**</span><span class="sxs-lookup"><span data-stu-id="0746c-106">The following code creates a new **Table**:</span></span>

`Dim obj As New Table`

<span data-ttu-id="0746c-107">С свойствами и коллекциями объекта **Table** можно:</span><span class="sxs-lookup"><span data-stu-id="0746c-107">With the properties and collections of a **Table** object, you can:</span></span>

- <span data-ttu-id="0746c-108">Определите таблицу с [свойством Name.](name-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="0746c-108">Identify the table with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="0746c-109">Определите тип таблицы с [свойством Type.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox)</span><span class="sxs-lookup"><span data-stu-id="0746c-109">Determine the type of table with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox) property.</span></span>

- <span data-ttu-id="0746c-110">Доступ к столбцам базы данных таблицы с помощью коллекции [Столбцы.](columns-collection-adox.md)</span><span class="sxs-lookup"><span data-stu-id="0746c-110">Access the database columns of the table with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="0746c-111">Доступ к индексам таблицы с помощью коллекции [Indexes.](indexes-collection-adox.md)</span><span class="sxs-lookup"><span data-stu-id="0746c-111">Access the indexes of the table with the [Indexes](indexes-collection-adox.md) collection.</span></span>

- <span data-ttu-id="0746c-112">Доступ к клавишам таблицы с помощью коллекции [Ключей.](keys-collection-adox.md)</span><span class="sxs-lookup"><span data-stu-id="0746c-112">Access the keys of the table with the [Keys](keys-collection-adox.md) collection.</span></span>

- <span data-ttu-id="0746c-113">Укажите [каталог,](catalog-object-adox.md) который владеет таблицей с [свойством ParentCatalog.](parentcatalog-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="0746c-113">Specify the [Catalog](catalog-object-adox.md) that owns the table with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

- <span data-ttu-id="0746c-114">Сведения о дате возврата со свойствами [DateCreated](datecreated-property-adox.md) и [DateModified.](datemodified-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="0746c-114">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

- <span data-ttu-id="0746c-115">Доступ к свойствам таблицы, определенной для поставщика, с [коллекцией свойств.](properties-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="0746c-115">Access provider-specific table properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="0746c-116">Поставщик данных может не поддерживать все свойства объектов **Table.**</span><span class="sxs-lookup"><span data-stu-id="0746c-116">Your data provider may not support all properties of **Table** objects.</span></span> <span data-ttu-id="0746c-117">Ошибка возникает, если установлено значение для свойства, которое поставщик не поддерживает.</span><span class="sxs-lookup"><span data-stu-id="0746c-117">An error will occur if you have set a value for a property that the provider does not support.</span></span> <span data-ttu-id="0746c-118">Для новых **объектов Таблицы** ошибка возникает при приложении объекта к коллекции.</span><span class="sxs-lookup"><span data-stu-id="0746c-118">For new **Table** objects, the error will occur when the object is appended to the collection.</span></span> <span data-ttu-id="0746c-119">Для существующих объектов ошибка возникает при настройке свойства.</span><span class="sxs-lookup"><span data-stu-id="0746c-119">For existing objects, the error will occur when setting the property.</span></span>

<span data-ttu-id="0746c-120">При создании **объектов Table** наличие соответствующего значения по умолчанию для необязательных свойств не гарантирует, что поставщик поддерживает свойство.</span><span class="sxs-lookup"><span data-stu-id="0746c-120">When creating **Table** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</span></span> <span data-ttu-id="0746c-121">Дополнительные сведения о свойствах, поддерживаемых поставщиком, см. в документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="0746c-121">For more information about which properties your provider supports, see your provider documentation.</span></span>


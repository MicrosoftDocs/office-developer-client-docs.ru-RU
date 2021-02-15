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
# <a name="table-object-adox"></a><span data-ttu-id="f86bd-102">Объект Table (ADOX)</span><span class="sxs-lookup"><span data-stu-id="f86bd-102">Table object (ADOX)</span></span>

<span data-ttu-id="f86bd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f86bd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f86bd-104">Представляет таблицу базы данных, включаемую столбцы, индексы и ключи.</span><span class="sxs-lookup"><span data-stu-id="f86bd-104">Represents a database table including columns, indexes, and keys.</span></span>

## <a name="remarks"></a><span data-ttu-id="f86bd-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="f86bd-105">Remarks</span></span>

<span data-ttu-id="f86bd-106">Следующий код создает новую **таблицу:**</span><span class="sxs-lookup"><span data-stu-id="f86bd-106">The following code creates a new **Table**:</span></span>

`Dim obj As New Table`

<span data-ttu-id="f86bd-107">С помощью свойств и коллекций объекта **Table** можно:</span><span class="sxs-lookup"><span data-stu-id="f86bd-107">With the properties and collections of a **Table** object, you can:</span></span>

- <span data-ttu-id="f86bd-108">Определите таблицу с помощью [свойства Name.](name-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="f86bd-108">Identify the table with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="f86bd-109">Определите тип таблицы со [свойством Type.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox)</span><span class="sxs-lookup"><span data-stu-id="f86bd-109">Determine the type of table with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-tableadox) property.</span></span>

- <span data-ttu-id="f86bd-110">Доступ к столбцам базы данных таблицы с помощью коллекции [Columns.](columns-collection-adox.md)</span><span class="sxs-lookup"><span data-stu-id="f86bd-110">Access the database columns of the table with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="f86bd-111">Доступ к индексам таблицы с помощью коллекции [Indexes.](indexes-collection-adox.md)</span><span class="sxs-lookup"><span data-stu-id="f86bd-111">Access the indexes of the table with the [Indexes](indexes-collection-adox.md) collection.</span></span>

- <span data-ttu-id="f86bd-112">Доступ к ключам таблицы с помощью коллекции [Keys.](keys-collection-adox.md)</span><span class="sxs-lookup"><span data-stu-id="f86bd-112">Access the keys of the table with the [Keys](keys-collection-adox.md) collection.</span></span>

- <span data-ttu-id="f86bd-113">Укажите [каталог,](catalog-object-adox.md) который является владельцем таблицы, со [свойством ParentCatalog.](parentcatalog-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="f86bd-113">Specify the [Catalog](catalog-object-adox.md) that owns the table with the [ParentCatalog](parentcatalog-property-adox.md) property.</span></span>

- <span data-ttu-id="f86bd-114">Сведения о дате возврата [со свойствами DateCreated](datecreated-property-adox.md) и [DateModified.](datemodified-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="f86bd-114">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

- <span data-ttu-id="f86bd-115">Доступ к свойствам таблицы для определенного поставщика с помощью коллекции [Properties.](properties-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="f86bd-115">Access provider-specific table properties with the [Properties](properties-collection-ado.md) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="f86bd-116">Поставщик данных может поддерживать не все свойства объектов **Table.**</span><span class="sxs-lookup"><span data-stu-id="f86bd-116">Your data provider may not support all properties of **Table** objects.</span></span> <span data-ttu-id="f86bd-117">Ошибка возникает, если вы установили значение для свойства, которое поставщик не поддерживает.</span><span class="sxs-lookup"><span data-stu-id="f86bd-117">An error will occur if you have set a value for a property that the provider does not support.</span></span> <span data-ttu-id="f86bd-118">Для новых **объектов Table** ошибка возникает, когда объект будет appended к коллекции.</span><span class="sxs-lookup"><span data-stu-id="f86bd-118">For new **Table** objects, the error will occur when the object is appended to the collection.</span></span> <span data-ttu-id="f86bd-119">Для существующих объектов ошибка возникает при установке свойства.</span><span class="sxs-lookup"><span data-stu-id="f86bd-119">For existing objects, the error will occur when setting the property.</span></span>

<span data-ttu-id="f86bd-120">При создании **объектов Table** наличие соответствующего значения по умолчанию для необязательного свойства не гарантирует, что ваш поставщик поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="f86bd-120">When creating **Table** objects, the existence of an appropriate default value for an optional property does not guarantee that your provider supports the property.</span></span> <span data-ttu-id="f86bd-121">Дополнительные сведения о свойствах, поддерживаемые поставщиком, см. в документации поставщика.</span><span class="sxs-lookup"><span data-stu-id="f86bd-121">For more information about which properties your provider supports, see your provider documentation.</span></span>


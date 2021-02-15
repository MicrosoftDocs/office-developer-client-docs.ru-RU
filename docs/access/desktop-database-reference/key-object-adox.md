---
title: Key Object (ADOX - Access desktop database reference)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f56a90b7accd1b64c9a52e0a7cf5385f83fd10d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290754"
---
# <a name="key-object-adox"></a><span data-ttu-id="9e714-102">Key object (ADOX)</span><span class="sxs-lookup"><span data-stu-id="9e714-102">Key object (ADOX)</span></span>


<span data-ttu-id="9e714-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e714-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e714-104">Представляет поле первичного, внешнего или уникального ключа из таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="9e714-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e714-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="9e714-105">Remarks</span></span>

<span data-ttu-id="9e714-106">Следующий код создает новый **ключ:**</span><span class="sxs-lookup"><span data-stu-id="9e714-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="9e714-107">С помощью свойств и коллекций объекта **Key** можно:</span><span class="sxs-lookup"><span data-stu-id="9e714-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="9e714-108">Определите ключ с помощью [свойства Name.](name-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="9e714-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="9e714-109">Определите, является ли ключ первичным, внешним или уникальным с помощью [свойства Type.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox)</span><span class="sxs-lookup"><span data-stu-id="9e714-109">Determine whether the key is primary, foreign, or unique with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property.</span></span>

- <span data-ttu-id="9e714-110">Доступ к столбцам базы данных ключа с помощью коллекции [Columns.](columns-collection-adox.md)</span><span class="sxs-lookup"><span data-stu-id="9e714-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="9e714-111">Укажите имя связанной таблицы со [свойством RelatedTable.](relatedtable-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="9e714-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="9e714-112">Определите действие, выполненное при удалении или обновлении первичного ключа, с помощью свойств [DeleteRule](deleterule-property-adox.md) и [UpdateRule.](updaterule-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="9e714-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>


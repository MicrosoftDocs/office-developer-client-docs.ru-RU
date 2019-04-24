---
title: Объект Key (ADOX — Справочник по базам данных для доступа к рабочему столу)
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
# <a name="key-object-adox"></a><span data-ttu-id="8b033-102">Объект Key (ADOX)</span><span class="sxs-lookup"><span data-stu-id="8b033-102">Key object (ADOX)</span></span>


<span data-ttu-id="8b033-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b033-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b033-104">Представляет первичное, внешнее или уникальное ключевое поле из таблицы базы данных.</span><span class="sxs-lookup"><span data-stu-id="8b033-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b033-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="8b033-105">Remarks</span></span>

<span data-ttu-id="8b033-106">Следующий код создает новый **ключ**:</span><span class="sxs-lookup"><span data-stu-id="8b033-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="8b033-107">С помощью свойств и коллекций объекта **Key** можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="8b033-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="8b033-108">Определите ключ с помощью свойства [Name](name-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="8b033-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="8b033-109">Определите, является ли ключ первичным, внешним или уникальным, с помощью свойства [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) .</span><span class="sxs-lookup"><span data-stu-id="8b033-109">Determine whether the key is primary, foreign, or unique with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property.</span></span>

- <span data-ttu-id="8b033-110">Доступ к столбцам базы данных ключа с помощью [](columns-collection-adox.md) коллекции Columns.</span><span class="sxs-lookup"><span data-stu-id="8b033-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="8b033-111">Укажите имя связанной таблицы с помощью свойства [RelatedTable](relatedtable-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="8b033-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="8b033-112">Определение действия, выполняемого при удалении или обновлении первичного ключа с помощью свойств [DeleteRule](deleterule-property-adox.md) и [UpdateRule](updaterule-property-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="8b033-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>


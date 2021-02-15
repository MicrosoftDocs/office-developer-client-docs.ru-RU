---
title: Свойство ParentCatalog (ADOX)
TOCTitle: ParentCatalog property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d7a10bac3c02a771518038351bc4d0b780c0e774
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287785"
---
# <a name="parentcatalog-property-adox"></a><span data-ttu-id="3e95d-102">Свойство ParentCatalog (ADOX)</span><span class="sxs-lookup"><span data-stu-id="3e95d-102">ParentCatalog property (ADOX)</span></span>


<span data-ttu-id="3e95d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e95d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3e95d-104">Указывает родительский каталог таблицы или столбца для предоставления доступа к свойствам конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="3e95d-104">Specifies the parent catalog of a table or column to provide access to provider-specific properties.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3e95d-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3e95d-105">Settings and return values</span></span>

<span data-ttu-id="3e95d-106">Задает и возвращает объект [Catalog.](catalog-object-adox.md)</span><span class="sxs-lookup"><span data-stu-id="3e95d-106">Sets and returns a [Catalog](catalog-object-adox.md) object.</span></span> <span data-ttu-id="3e95d-107">Установка **параметра ParentCatalog** для открытого каталога позволяет получить доступ к свойствам конкретного поставщика перед присоединением таблицы или столбца к коллекции **каталогов.** </span><span class="sxs-lookup"><span data-stu-id="3e95d-107">Setting **ParentCatalog** to an open **Catalog** allows access to provider-specific properties prior to appending a table or column to a **Catalog** collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e95d-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="3e95d-108">Remarks</span></span>

<span data-ttu-id="3e95d-109">Некоторые поставщики данных позволяют создавать значения свойств для определенных поставщиков только при создании (при добавлении таблицы или столбца в коллекцию **каталогов).**</span><span class="sxs-lookup"><span data-stu-id="3e95d-109">Some data providers allow provider-specific property values to be written only at creation (when a table or column is appended to its **Catalog** collection).</span></span> <span data-ttu-id="3e95d-110">Чтобы получить доступ к этим свойствам перед их  присоединением к каталогу, сначала укажите каталог в свойстве **ParentCatalog.**</span><span class="sxs-lookup"><span data-stu-id="3e95d-110">To access these properties before appending these objects to a **Catalog**, specify the **Catalog** in the **ParentCatalog** property first.</span></span>

<span data-ttu-id="3e95d-111">Ошибка возникает, когда таблица или столбец примеся к каталогу, который отличается **от ParentCatalog.** </span><span class="sxs-lookup"><span data-stu-id="3e95d-111">An error occurs when the table or column is appended to a different **Catalog** than the **ParentCatalog**.</span></span>


---
title: ParentCatalog Property (ADOX)
TOCTitle: ParentCatalog Property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d9fdd4b41578b4f185d199a47204faabd0af3ff8
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603415"
---
# <a name="parentcatalog-property-adox"></a><span data-ttu-id="3dbed-102">ParentCatalog Property (ADOX)</span><span class="sxs-lookup"><span data-stu-id="3dbed-102">ParentCatalog Property (ADOX)</span></span>


<span data-ttu-id="3dbed-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3dbed-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3dbed-104">Указывает каталог родительской таблицы или столбца для предоставления доступа к свойствам конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="3dbed-104">Specifies the parent catalog of a table or column to provide access to provider-specific properties.</span></span>

<span data-ttu-id="3dbed-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="3dbed-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="3dbed-106">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3dbed-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="3dbed-107">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3dbed-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="3dbed-108">master</span><span class="sxs-lookup"><span data-stu-id="3dbed-108">master</span></span>

<span data-ttu-id="3dbed-109">Задает и возвращает объект [каталога](catalog-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="3dbed-109">Sets and returns a [Catalog](catalog-object-adox.md) object.</span></span> <span data-ttu-id="3dbed-110">Параметру **ParentCatalog** open **каталога** позволяет получить доступ к свойствам конкретного поставщика перед добавлением таблицы или столбца в коллекцию **каталога** .</span><span class="sxs-lookup"><span data-stu-id="3dbed-110">Setting **ParentCatalog** to an open **Catalog** allows access to provider-specific properties prior to appending a table or column to a **Catalog** collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dbed-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="3dbed-111">Remarks</span></span>

<span data-ttu-id="3dbed-112">Некоторые поставщики данных Разрешить значения свойства от поставщика для записи только при создании (если таблицы или столбца добавляется к коллекции **каталога** ).</span><span class="sxs-lookup"><span data-stu-id="3dbed-112">Some data providers allow provider-specific property values to be written only at creation (when a table or column is appended to its **Catalog** collection).</span></span> <span data-ttu-id="3dbed-113">Для доступа к этим свойствам перед добавлением этих объектов **каталога**, укажите **каталога** в свойстве **ParentCatalog** сначала.</span><span class="sxs-lookup"><span data-stu-id="3dbed-113">To access these properties before appending these objects to a **Catalog**, specify the **Catalog** in the **ParentCatalog** property first.</span></span>

<span data-ttu-id="3dbed-114">Когда таблицы или столбца добавляется другой **каталог** чем **ParentCatalog**возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="3dbed-114">An error occurs when the table or column is appended to a different **Catalog** than the **ParentCatalog**.</span></span>


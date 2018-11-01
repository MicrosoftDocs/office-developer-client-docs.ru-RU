---
title: Свойство ParentCatalog (ADOX)
TOCTitle: ParentCatalog Property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e316beebd45b39d7cbbb0714499ec7156a4bb270
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883724"
---
# <a name="parentcatalog-property-adox"></a><span data-ttu-id="eaeda-102">Свойство ParentCatalog (ADOX)</span><span class="sxs-lookup"><span data-stu-id="eaeda-102">ParentCatalog Property (ADOX)</span></span>


<span data-ttu-id="eaeda-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eaeda-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eaeda-104">Указывает каталог родительской таблицы или столбца для предоставления доступа к свойствам конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="eaeda-104">Specifies the parent catalog of a table or column to provide access to provider-specific properties.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="eaeda-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="eaeda-105">Settings and return values</span></span>

<span data-ttu-id="eaeda-106">Задает и возвращает объект [каталога](catalog-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="eaeda-106">Sets and returns a [Catalog](catalog-object-adox.md) object.</span></span> <span data-ttu-id="eaeda-107">Параметру **ParentCatalog** open **каталога** позволяет получить доступ к свойствам конкретного поставщика перед добавлением таблицы или столбца в коллекцию **каталога** .</span><span class="sxs-lookup"><span data-stu-id="eaeda-107">Setting **ParentCatalog** to an open **Catalog** allows access to provider-specific properties prior to appending a table or column to a **Catalog** collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaeda-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="eaeda-108">Remarks</span></span>

<span data-ttu-id="eaeda-109">Некоторые поставщики данных Разрешить значения свойства от поставщика для записи только при создании (если таблицы или столбца добавляется к коллекции **каталога** ).</span><span class="sxs-lookup"><span data-stu-id="eaeda-109">Some data providers allow provider-specific property values to be written only at creation (when a table or column is appended to its **Catalog** collection).</span></span> <span data-ttu-id="eaeda-110">Для доступа к этим свойствам перед добавлением этих объектов **каталога**, укажите **каталога** в свойстве **ParentCatalog** сначала.</span><span class="sxs-lookup"><span data-stu-id="eaeda-110">To access these properties before appending these objects to a **Catalog**, specify the **Catalog** in the **ParentCatalog** property first.</span></span>

<span data-ttu-id="eaeda-111">Когда таблицы или столбца добавляется другой **каталог** чем **ParentCatalog**возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="eaeda-111">An error occurs when the table or column is appended to a different **Catalog** than the **ParentCatalog**.</span></span>


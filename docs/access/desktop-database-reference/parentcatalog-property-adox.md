---
title: Свойство ParentCatalog (ADOX)
TOCTitle: ParentCatalog property (ADOX)
ms:assetid: 7eef4ef5-1fa4-73ea-a710-fc8767c9ea21
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249535(v=office.15)
ms:contentKeyID: 48545891
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bbeed0283eaf7982d037cfe7bf4773db9a8c03b5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928455"
---
# <a name="parentcatalog-property-adox"></a><span data-ttu-id="3c1f2-102">Свойство ParentCatalog (ADOX)</span><span class="sxs-lookup"><span data-stu-id="3c1f2-102">ParentCatalog property (ADOX)</span></span>


<span data-ttu-id="3c1f2-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c1f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c1f2-104">Указывает каталог родительской таблицы или столбца для предоставления доступа к свойствам конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="3c1f2-104">Specifies the parent catalog of a table or column to provide access to provider-specific properties.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3c1f2-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3c1f2-105">Settings and return values</span></span>

<span data-ttu-id="3c1f2-106">Задает и возвращает объект [каталога](catalog-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="3c1f2-106">Sets and returns a [Catalog](catalog-object-adox.md) object.</span></span> <span data-ttu-id="3c1f2-107">Параметру **ParentCatalog** open **каталога** позволяет получить доступ к свойствам конкретного поставщика перед добавлением таблицы или столбца в коллекцию **каталога** .</span><span class="sxs-lookup"><span data-stu-id="3c1f2-107">Setting **ParentCatalog** to an open **Catalog** allows access to provider-specific properties prior to appending a table or column to a **Catalog** collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c1f2-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="3c1f2-108">Remarks</span></span>

<span data-ttu-id="3c1f2-109">Некоторые поставщики данных Разрешить значения свойства от поставщика для записи только при создании (если таблицы или столбца добавляется к коллекции **каталога** ).</span><span class="sxs-lookup"><span data-stu-id="3c1f2-109">Some data providers allow provider-specific property values to be written only at creation (when a table or column is appended to its **Catalog** collection).</span></span> <span data-ttu-id="3c1f2-110">Для доступа к этим свойствам перед добавлением этих объектов **каталога**, укажите **каталога** в свойстве **ParentCatalog** сначала.</span><span class="sxs-lookup"><span data-stu-id="3c1f2-110">To access these properties before appending these objects to a **Catalog**, specify the **Catalog** in the **ParentCatalog** property first.</span></span>

<span data-ttu-id="3c1f2-111">Когда таблицы или столбца добавляется другой **каталог** чем **ParentCatalog**возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="3c1f2-111">An error occurs when the table or column is appended to a different **Catalog** than the **ParentCatalog**.</span></span>


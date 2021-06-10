---
title: Свойство DateCreated (ADOX)
TOCTitle: DateCreated property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 59b19ab3be6633daf7295a63a33a31a34b64fbd7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294423"
---
# <a name="datecreated-property-adox"></a><span data-ttu-id="e04c9-102">Свойство DateCreated (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e04c9-102">DateCreated property (ADOX)</span></span>


<span data-ttu-id="e04c9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e04c9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e04c9-104">Указывает дату создания объекта.</span><span class="sxs-lookup"><span data-stu-id="e04c9-104">Indicates the date the object was created.</span></span>

## <a name="return-values"></a><span data-ttu-id="e04c9-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e04c9-105">Return values</span></span>

<span data-ttu-id="e04c9-106">Возвращает значение **Variant,** указывав дату создания.</span><span class="sxs-lookup"><span data-stu-id="e04c9-106">Returns a **Variant** value specifying the date created.</span></span> <span data-ttu-id="e04c9-107">Значение null, если **DateCreated** не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="e04c9-107">The value is null if **DateCreated** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="e04c9-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="e04c9-108">Remarks</span></span>

<span data-ttu-id="e04c9-109">Свойство **DateCreated** является null для вновь пристроенных объектов.</span><span class="sxs-lookup"><span data-stu-id="e04c9-109">The **DateCreated** property is null for newly appended objects.</span></span> <span data-ttu-id="e04c9-110">После придания [](view-object-adox.md) нового представления или процедуры [необходимо](procedure-object-adox.md)вызвать [](views-collection-adox.md) метод [](procedures-collection-adox.md) [Обновления](refresh-method-ado.md) коллекции Просмотры или Процедуры для получения значений для **свойства DateCreated.**</span><span class="sxs-lookup"><span data-stu-id="e04c9-110">After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateCreated** property.</span></span>


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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712619"
---
# <a name="datecreated-property-adox"></a><span data-ttu-id="3bcb8-102">Свойство DateCreated (ADOX)</span><span class="sxs-lookup"><span data-stu-id="3bcb8-102">DateCreated property (ADOX)</span></span>


<span data-ttu-id="3bcb8-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3bcb8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3bcb8-104">Указывает дату создания объекта.</span><span class="sxs-lookup"><span data-stu-id="3bcb8-104">Indicates the date the object was created.</span></span>

## <a name="return-values"></a><span data-ttu-id="3bcb8-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3bcb8-105">Return values</span></span>

<span data-ttu-id="3bcb8-106">Возвращает значение **типа Variant** , определяющее Дата создания.</span><span class="sxs-lookup"><span data-stu-id="3bcb8-106">Returns a **Variant** value specifying the date created.</span></span> <span data-ttu-id="3bcb8-107">Значение null, если **DateCreated** не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="3bcb8-107">The value is null if **DateCreated** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bcb8-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="3bcb8-108">Remarks</span></span>

<span data-ttu-id="3bcb8-109">Свойство **DateCreated** имеет значение null для добавленного объектов.</span><span class="sxs-lookup"><span data-stu-id="3bcb8-109">The **DateCreated** property is null for newly appended objects.</span></span> <span data-ttu-id="3bcb8-110">После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md), необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции для получения значения для свойства **DateCreated** [представления](views-collection-adox.md) или [процедуры](procedures-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="3bcb8-110">After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateCreated** property.</span></span>


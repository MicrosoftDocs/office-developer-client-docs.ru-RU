---
title: DateCreated Property (ADOX)
TOCTitle: DateCreated Property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3f96bdfc7b669aeea279ba746c92bfc299912c70
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602554"
---
# <a name="datecreated-property-adox"></a><span data-ttu-id="469fd-102">DateCreated Property (ADOX)</span><span class="sxs-lookup"><span data-stu-id="469fd-102">DateCreated Property (ADOX)</span></span>


<span data-ttu-id="469fd-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="469fd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="469fd-104">Указывает дату создания объекта.</span><span class="sxs-lookup"><span data-stu-id="469fd-104">Indicates the date the object was created.</span></span>

<span data-ttu-id="469fd-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="469fd-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="469fd-106">Return Values</span><span class="sxs-lookup"><span data-stu-id="469fd-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="469fd-107">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="469fd-107">Return values</span></span>
>>>>>>> <span data-ttu-id="469fd-108">master</span><span class="sxs-lookup"><span data-stu-id="469fd-108">master</span></span>

<span data-ttu-id="469fd-109">Возвращает значение **типа Variant** , определяющее Дата создания.</span><span class="sxs-lookup"><span data-stu-id="469fd-109">Returns a **Variant** value specifying the date created.</span></span> <span data-ttu-id="469fd-110">Значение null, если **DateCreated** не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="469fd-110">The value is null if **DateCreated** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="469fd-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="469fd-111">Remarks</span></span>

<span data-ttu-id="469fd-112">Свойство **DateCreated** имеет значение null для добавленного объектов.</span><span class="sxs-lookup"><span data-stu-id="469fd-112">The **DateCreated** property is null for newly appended objects.</span></span> <span data-ttu-id="469fd-113">После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md), необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции для получения значения для свойства **DateCreated** [представления](views-collection-adox.md) или [процедуры](procedures-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="469fd-113">After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateCreated** property.</span></span>


---
title: DateModified Property (ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ceafd13b33536a77a1d793e7167fe8042609be5e
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603331"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="cf1e7-102">DateModified Property (ADOX)</span><span class="sxs-lookup"><span data-stu-id="cf1e7-102">DateModified Property (ADOX)</span></span>


<span data-ttu-id="cf1e7-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cf1e7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cf1e7-104">Указывает дату последнего изменения объекта.</span><span class="sxs-lookup"><span data-stu-id="cf1e7-104">Indicates the date the object was last modified.</span></span>

<span data-ttu-id="cf1e7-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="cf1e7-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="cf1e7-106">Return Values</span><span class="sxs-lookup"><span data-stu-id="cf1e7-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="cf1e7-107">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="cf1e7-107">Return values</span></span>
>>>>>>> <span data-ttu-id="cf1e7-108">master</span><span class="sxs-lookup"><span data-stu-id="cf1e7-108">master</span></span>

<span data-ttu-id="cf1e7-109">Возвращает значение **типа Variant** , указав дату изменения.</span><span class="sxs-lookup"><span data-stu-id="cf1e7-109">Returns a **Variant** value specifying the date modified.</span></span> <span data-ttu-id="cf1e7-110">Значение null, если **DateModified** не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="cf1e7-110">The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf1e7-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="cf1e7-111">Remarks</span></span>

<span data-ttu-id="cf1e7-112">Свойство **DateModified** имеет значение null для добавленного объектов.</span><span class="sxs-lookup"><span data-stu-id="cf1e7-112">The **DateModified** property is null for newly appended objects.</span></span> <span data-ttu-id="cf1e7-113">После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md), необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции для получения значения для свойства **DateModified** [представления](views-collection-adox.md) или [процедуры](procedures-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="cf1e7-113">After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>


---
title: DateModified Property (ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8465f97565d8519196b8221089121670ceedb275
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480102"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="4f989-102">DateModified Property (ADOX)</span><span class="sxs-lookup"><span data-stu-id="4f989-102">DateModified Property (ADOX)</span></span>


<span data-ttu-id="4f989-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f989-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4f989-104">Указывает дату последнего изменения объекта.</span><span class="sxs-lookup"><span data-stu-id="4f989-104">Indicates the date the object was last modified.</span></span>

## <a name="return-values"></a><span data-ttu-id="4f989-105">Return Values</span><span class="sxs-lookup"><span data-stu-id="4f989-105">Return Values</span></span>

<span data-ttu-id="4f989-106">Возвращает значение **типа Variant** , указав дату изменения.</span><span class="sxs-lookup"><span data-stu-id="4f989-106">Returns a **Variant** value specifying the date modified.</span></span> <span data-ttu-id="4f989-107">Значение null, если **DateModified** не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="4f989-107">The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f989-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="4f989-108">Remarks</span></span>

<span data-ttu-id="4f989-109">Свойство **DateModified** имеет значение null для добавленного объектов.</span><span class="sxs-lookup"><span data-stu-id="4f989-109">The **DateModified** property is null for newly appended objects.</span></span> <span data-ttu-id="4f989-110">После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md), необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции для получения значения для свойства **DateModified** [представления](views-collection-adox.md) или [процедуры](procedures-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="4f989-110">After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>


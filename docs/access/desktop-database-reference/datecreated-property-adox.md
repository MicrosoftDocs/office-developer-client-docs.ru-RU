---
title: Свойство DateCreated (ADOX)
TOCTitle: DateCreated property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 344b193b3ab8d6800fcf81b6bb2d184b1104f9d3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923102"
---
# <a name="datecreated-property-adox"></a><span data-ttu-id="cdc7a-102">Свойство DateCreated (ADOX)</span><span class="sxs-lookup"><span data-stu-id="cdc7a-102">DateCreated property (ADOX)</span></span>


<span data-ttu-id="cdc7a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cdc7a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cdc7a-104">Указывает дату создания объекта.</span><span class="sxs-lookup"><span data-stu-id="cdc7a-104">Indicates the date the object was created.</span></span>

## <a name="return-values"></a><span data-ttu-id="cdc7a-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="cdc7a-105">Return values</span></span>

<span data-ttu-id="cdc7a-106">Возвращает значение **типа Variant** , определяющее Дата создания.</span><span class="sxs-lookup"><span data-stu-id="cdc7a-106">Returns a **Variant** value specifying the date created.</span></span> <span data-ttu-id="cdc7a-107">Значение null, если **DateCreated** не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="cdc7a-107">The value is null if **DateCreated** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdc7a-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="cdc7a-108">Remarks</span></span>

<span data-ttu-id="cdc7a-109">Свойство **DateCreated** имеет значение null для добавленного объектов.</span><span class="sxs-lookup"><span data-stu-id="cdc7a-109">The **DateCreated** property is null for newly appended objects.</span></span> <span data-ttu-id="cdc7a-110">После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md), необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции для получения значения для свойства **DateCreated** [представления](views-collection-adox.md) или [процедуры](procedures-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="cdc7a-110">After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateCreated** property.</span></span>


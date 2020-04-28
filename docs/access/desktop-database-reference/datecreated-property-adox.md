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
# <a name="datecreated-property-adox"></a><span data-ttu-id="dfc8b-102">Свойство DateCreated (ADOX)</span><span class="sxs-lookup"><span data-stu-id="dfc8b-102">DateCreated property (ADOX)</span></span>


<span data-ttu-id="dfc8b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dfc8b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dfc8b-104">Указывает дату создания объекта.</span><span class="sxs-lookup"><span data-stu-id="dfc8b-104">Indicates the date the object was created.</span></span>

## <a name="return-values"></a><span data-ttu-id="dfc8b-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="dfc8b-105">Return values</span></span>

<span data-ttu-id="dfc8b-106">Возвращает значение **типа Variant** , определяющее созданную дату.</span><span class="sxs-lookup"><span data-stu-id="dfc8b-106">Returns a **Variant** value specifying the date created.</span></span> <span data-ttu-id="dfc8b-107">Значение равно null, если **DateCreated** не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="dfc8b-107">The value is null if **DateCreated** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfc8b-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="dfc8b-108">Remarks</span></span>

<span data-ttu-id="dfc8b-109">Для новых добавленных объектов свойство **DateCreated** имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="dfc8b-109">The **DateCreated** property is null for newly appended objects.</span></span> <span data-ttu-id="dfc8b-110">После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md)необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции [представлений](views-collection-adox.md) или [процедур](procedures-collection-adox.md) для получения значений для свойства **DateCreated** .</span><span class="sxs-lookup"><span data-stu-id="dfc8b-110">After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateCreated** property.</span></span>


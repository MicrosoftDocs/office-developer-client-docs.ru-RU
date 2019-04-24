---
title: Свойство DateModified (ADOX)
TOCTitle: DateModified property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: daf72804d51c18b5875e607ce5fdb0dfe20f406c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294409"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="7affb-102">Свойство DateModified (ADOX)</span><span class="sxs-lookup"><span data-stu-id="7affb-102">DateModified property (ADOX)</span></span>


<span data-ttu-id="7affb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7affb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7affb-104">Указывает дату последнего изменения объекта.</span><span class="sxs-lookup"><span data-stu-id="7affb-104">Indicates the date the object was last modified.</span></span>

## <a name="return-values"></a><span data-ttu-id="7affb-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7affb-105">Return values</span></span>

<span data-ttu-id="7affb-106">Возвращает значение **типа Variant** , указывающее дату изменения.</span><span class="sxs-lookup"><span data-stu-id="7affb-106">Returns a **Variant** value specifying the date modified.</span></span> <span data-ttu-id="7affb-107">Значение равно null, если **DateModified** не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="7affb-107">The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="7affb-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="7affb-108">Remarks</span></span>

<span data-ttu-id="7affb-109">Для новых добавленных объектов свойство **DateModified** имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="7affb-109">The **DateModified** property is null for newly appended objects.</span></span> <span data-ttu-id="7affb-110">После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md)необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции [представлений](views-collection-adox.md) или [процедур](procedures-collection-adox.md) для получения значений для свойства **DateModified** .</span><span class="sxs-lookup"><span data-stu-id="7affb-110">After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>


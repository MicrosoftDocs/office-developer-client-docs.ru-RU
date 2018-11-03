---
title: Свойство DateModified (ADOX)
TOCTitle: DateModified property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 447b7c609dd122d825d97a7430349eb88f8f7b0b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923954"
---
# <a name="datemodified-property-adox"></a><span data-ttu-id="7fd53-102">Свойство DateModified (ADOX)</span><span class="sxs-lookup"><span data-stu-id="7fd53-102">DateModified property (ADOX)</span></span>


<span data-ttu-id="7fd53-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7fd53-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7fd53-104">Указывает дату последнего изменения объекта.</span><span class="sxs-lookup"><span data-stu-id="7fd53-104">Indicates the date the object was last modified.</span></span>

## <a name="return-values"></a><span data-ttu-id="7fd53-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="7fd53-105">Return values</span></span>

<span data-ttu-id="7fd53-106">Возвращает значение **типа Variant** , указав дату изменения.</span><span class="sxs-lookup"><span data-stu-id="7fd53-106">Returns a **Variant** value specifying the date modified.</span></span> <span data-ttu-id="7fd53-107">Значение null, если **DateModified** не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="7fd53-107">The value is null if **DateModified** is not supported by the provider.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fd53-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="7fd53-108">Remarks</span></span>

<span data-ttu-id="7fd53-109">Свойство **DateModified** имеет значение null для добавленного объектов.</span><span class="sxs-lookup"><span data-stu-id="7fd53-109">The **DateModified** property is null for newly appended objects.</span></span> <span data-ttu-id="7fd53-110">После добавления нового [представления](view-object-adox.md) или [процедуры](procedure-object-adox.md), необходимо вызвать метод [Refresh](refresh-method-ado.md) коллекции для получения значения для свойства **DateModified** [представления](views-collection-adox.md) или [процедуры](procedures-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="7fd53-110">After appending a new [View](view-object-adox.md) or [Procedure](procedure-object-adox.md), you must call the [Refresh](refresh-method-ado.md) method of the [Views](views-collection-adox.md) or [Procedures](procedures-collection-adox.md) collection to obtain values for the **DateModified** property.</span></span>


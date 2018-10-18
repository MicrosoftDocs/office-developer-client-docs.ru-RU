---
title: Name Property (ADO MD)
TOCTitle: Name Property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90a77ae9d8c32ff8d0a13eacb146fc0e3ab3f397
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602470"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="a9b49-102">Name Property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="a9b49-102">Name Property (ADO MD)</span></span>


<span data-ttu-id="a9b49-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9b49-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a9b49-104">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="a9b49-104">Indicates the name of an object.</span></span>

<span data-ttu-id="a9b49-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="a9b49-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="a9b49-106">Return Values</span><span class="sxs-lookup"><span data-stu-id="a9b49-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="a9b49-107">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="a9b49-107">Return values</span></span>
>>>>>>> <span data-ttu-id="a9b49-108">master</span><span class="sxs-lookup"><span data-stu-id="a9b49-108">master</span></span>

<span data-ttu-id="a9b49-109">Возвращает **строку** и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a9b49-109">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9b49-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="a9b49-110">Remarks</span></span>

<span data-ttu-id="a9b49-111">Свойство **Name** объекта можно извлечь с помощью порядковый номер ссылки, после чего можно обратиться к объекту непосредственно по имени.</span><span class="sxs-lookup"><span data-stu-id="a9b49-111">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="a9b49-112">Например если cdf. CubeDefs(0). Имя уступает «Bobs видео хранилища», можно ссылаться на этот [CubeDef](cubedef-object-ado-md.md) как cdf. CubeDefs ("Bobs видео хранилище").</span><span class="sxs-lookup"><span data-stu-id="a9b49-112">For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>


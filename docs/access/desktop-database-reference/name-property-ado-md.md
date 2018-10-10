---
title: Name Property (ADO MD)
TOCTitle: Name Property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0cc7a89e0d6b9cdaed2c54d3269b61280ce3306c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480560"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="97d70-102">Name Property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="97d70-102">Name Property (ADO MD)</span></span>


<span data-ttu-id="97d70-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="97d70-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="97d70-104">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="97d70-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="97d70-105">Return Values</span><span class="sxs-lookup"><span data-stu-id="97d70-105">Return Values</span></span>

<span data-ttu-id="97d70-106">Возвращает **строку** и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="97d70-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="97d70-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="97d70-107">Remarks</span></span>

<span data-ttu-id="97d70-108">Свойство **Name** объекта можно извлечь с помощью порядковый номер ссылки, после чего можно обратиться к объекту непосредственно по имени.</span><span class="sxs-lookup"><span data-stu-id="97d70-108">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="97d70-109">Например если cdf. CubeDefs(0). Имя уступает «Bobs видео хранилища», можно ссылаться на этот [CubeDef](cubedef-object-ado-md.md) как cdf. CubeDefs ("Bobs видео хранилище").</span><span class="sxs-lookup"><span data-stu-id="97d70-109">For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>


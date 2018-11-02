---
title: Свойство Name (ADO MD)
TOCTitle: Name property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 971a528c0efe97626f08ff94490e8aee25230f60
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926537"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="18feb-102">Свойство Name (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="18feb-102">Name property (ADO MD)</span></span>


<span data-ttu-id="18feb-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="18feb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18feb-104">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="18feb-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="18feb-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="18feb-105">Return values</span></span>

<span data-ttu-id="18feb-106">Возвращает **строку** и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="18feb-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="18feb-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="18feb-107">Remarks</span></span>

<span data-ttu-id="18feb-108">Свойство **Name** объекта можно извлечь с помощью порядковый номер ссылки, после чего можно обратиться к объекту непосредственно по имени.</span><span class="sxs-lookup"><span data-stu-id="18feb-108">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="18feb-109">Например если cdf. CubeDefs(0). Имя уступает «Bobs видео хранилища», можно ссылаться на этот [CubeDef](cubedef-object-ado-md.md) как cdf. CubeDefs ("Bobs видео хранилище").</span><span class="sxs-lookup"><span data-stu-id="18feb-109">For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>


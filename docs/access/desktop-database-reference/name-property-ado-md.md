---
title: Свойство Name (ADO MD)
TOCTitle: Name property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4e27870a0c1dbb38b7c0be31c439a95f6aae671
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704156"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="62d63-102">Свойство Name (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="62d63-102">Name property (ADO MD)</span></span>


<span data-ttu-id="62d63-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="62d63-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="62d63-104">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="62d63-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="62d63-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="62d63-105">Return values</span></span>

<span data-ttu-id="62d63-106">Возвращает **строку** и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="62d63-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="62d63-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="62d63-107">Remarks</span></span>

<span data-ttu-id="62d63-108">Свойство **Name** объекта можно извлечь с помощью порядковый номер ссылки, после чего можно обратиться к объекту непосредственно по имени.</span><span class="sxs-lookup"><span data-stu-id="62d63-108">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="62d63-109">Например если cdf. CubeDefs(0). Имя уступает «Bobs видео хранилища», можно ссылаться на этот [CubeDef](cubedef-object-ado-md.md) как cdf. CubeDefs ("Bobs видео хранилище").</span><span class="sxs-lookup"><span data-stu-id="62d63-109">For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>


---
title: Свойство Name (ADO MD)
TOCTitle: Name Property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 63e098a8b97bb37fad2ef256affb2da142daf434
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878649"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="8d2d5-102">Свойство Name (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="8d2d5-102">Name Property (ADO MD)</span></span>


<span data-ttu-id="8d2d5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d2d5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d2d5-104">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="8d2d5-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="8d2d5-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="8d2d5-105">Return values</span></span>

<span data-ttu-id="8d2d5-106">Возвращает **строку** и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8d2d5-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d2d5-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="8d2d5-107">Remarks</span></span>

<span data-ttu-id="8d2d5-108">Свойство **Name** объекта можно извлечь с помощью порядковый номер ссылки, после чего можно обратиться к объекту непосредственно по имени.</span><span class="sxs-lookup"><span data-stu-id="8d2d5-108">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="8d2d5-109">Например если cdf. CubeDefs(0). Имя уступает «Bobs видео хранилища», можно ссылаться на этот [CubeDef](cubedef-object-ado-md.md) как cdf. CubeDefs ("Bobs видео хранилище").</span><span class="sxs-lookup"><span data-stu-id="8d2d5-109">For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>


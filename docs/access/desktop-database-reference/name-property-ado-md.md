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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288660"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="9aeb7-102">Свойство Name (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="9aeb7-102">Name property (ADO MD)</span></span>


<span data-ttu-id="9aeb7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9aeb7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9aeb7-104">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="9aeb7-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="9aeb7-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9aeb7-105">Return values</span></span>

<span data-ttu-id="9aeb7-106">Возвращает **строку** и доступна только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9aeb7-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="9aeb7-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="9aeb7-107">Remarks</span></span>

<span data-ttu-id="9aeb7-108">Вы можете получить свойство **Name** объекта по порядковому номеру, после чего вы можете ссылаться на объект напрямую по имени.</span><span class="sxs-lookup"><span data-stu-id="9aeb7-108">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="9aeb7-109">Например, если CDF. Коллекция cubedefs (0). Name дает "Бобс Video Store", вы можете ссылаться на этот [CubeDef](cubedef-object-ado-md.md) как на CDF. Коллекция cubedefs ("Бобс Video Store").</span><span class="sxs-lookup"><span data-stu-id="9aeb7-109">For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>


---
title: Свойство Description (ADO MD)
TOCTitle: Description property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f74532693f1054dd9d187757af840a3a00b451f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293940"
---
# <a name="description-property-ado-md"></a><span data-ttu-id="25a3a-102">Свойство Description (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="25a3a-102">Description property (ADO MD)</span></span>


<span data-ttu-id="25a3a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="25a3a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="25a3a-104">Возвращает текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="25a3a-104">Returns a text explanation of the current object.</span></span>

## <a name="return-values"></a><span data-ttu-id="25a3a-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="25a3a-105">Return values</span></span>

<span data-ttu-id="25a3a-106">Возвращает **строку** и доступна только для чтения.</span><span class="sxs-lookup"><span data-stu-id="25a3a-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="25a3a-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="25a3a-107">Remarks</span></span>

<span data-ttu-id="25a3a-108">Для объектов [member](member-object-ado-md.md) **Описание** применяется только к элементам Measure и Measure.</span><span class="sxs-lookup"><span data-stu-id="25a3a-108">For [Member](member-object-ado-md.md) objects, **Description** applies only to measure and formula members.</span></span> <span data-ttu-id="25a3a-109">**Description** возвращает пустую строку ("") для всех других типов элементов.</span><span class="sxs-lookup"><span data-stu-id="25a3a-109">**Description** returns an empty string ("") for all other types of members.</span></span> <span data-ttu-id="25a3a-110">Дополнительные сведения о различных типах членов можно узнать в свойстве [Type](type-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="25a3a-110">For more information about the various types of members, see the [Type](type-property-ado-md.md) property.</span></span>

<span data-ttu-id="25a3a-111">Это свойство поддерживается только для объектов **member** , принадлежащих объекту [уровня](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="25a3a-111">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="25a3a-112">При обращении к этому свойству из объектов **member** , принадлежащих объекту [position](position-object-ado-md.md) , возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="25a3a-112">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>


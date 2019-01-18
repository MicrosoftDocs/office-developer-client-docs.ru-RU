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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720620"
---
# <a name="description-property-ado-md"></a><span data-ttu-id="2ce82-102">Свойство Description (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="2ce82-102">Description property (ADO MD)</span></span>


<span data-ttu-id="2ce82-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ce82-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2ce82-104">Возвращает описание текста текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="2ce82-104">Returns a text explanation of the current object.</span></span>

## <a name="return-values"></a><span data-ttu-id="2ce82-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="2ce82-105">Return values</span></span>

<span data-ttu-id="2ce82-106">Возвращает **строку** и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2ce82-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ce82-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="2ce82-107">Remarks</span></span>

<span data-ttu-id="2ce82-108">Для объектов [члена](member-object-ado-md.md) **Описание** относится только к измерения и формул элементы.</span><span class="sxs-lookup"><span data-stu-id="2ce82-108">For [Member](member-object-ado-md.md) objects, **Description** applies only to measure and formula members.</span></span> <span data-ttu-id="2ce82-109">**Описание** возвращает пустую строку ("») для всех остальных типов элементов.</span><span class="sxs-lookup"><span data-stu-id="2ce82-109">**Description** returns an empty string ("") for all other types of members.</span></span> <span data-ttu-id="2ce82-110">Дополнительные сведения о различных типах элементов [типа](type-property-ado-md.md) см.</span><span class="sxs-lookup"><span data-stu-id="2ce82-110">For more information about the various types of members, see the [Type](type-property-ado-md.md) property.</span></span>

<span data-ttu-id="2ce82-111">Это свойство поддерживается только для объектов **члена** , принадлежащих к объекту [уровень](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="2ce82-111">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="2ce82-112">Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="2ce82-112">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>


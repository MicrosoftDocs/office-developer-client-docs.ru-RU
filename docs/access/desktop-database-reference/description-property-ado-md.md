---
title: Description Property (ADO MD)
TOCTitle: Description Property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 29c6723d710fcf3a8114fb4460326d87261c3fc1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480472"
---
# <a name="description-property-ado-md"></a><span data-ttu-id="452d4-102">Description Property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="452d4-102">Description Property (ADO MD)</span></span>


<span data-ttu-id="452d4-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="452d4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="452d4-104">Возвращает описание текста текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="452d4-104">Returns a text explanation of the current object.</span></span>

## <a name="return-values"></a><span data-ttu-id="452d4-105">Return Values</span><span class="sxs-lookup"><span data-stu-id="452d4-105">Return Values</span></span>

<span data-ttu-id="452d4-106">Возвращает **строку** и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="452d4-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="452d4-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="452d4-107">Remarks</span></span>

<span data-ttu-id="452d4-108">Для объектов [члена](member-object-ado-md.md) **Описание** относится только к измерения и формул элементы.</span><span class="sxs-lookup"><span data-stu-id="452d4-108">For [Member](member-object-ado-md.md) objects, **Description** applies only to measure and formula members.</span></span> <span data-ttu-id="452d4-109">**Описание** возвращает пустую строку ("») для всех остальных типов элементов.</span><span class="sxs-lookup"><span data-stu-id="452d4-109">**Description** returns an empty string ("") for all other types of members.</span></span> <span data-ttu-id="452d4-110">Дополнительные сведения о различных типах элементов [типа](type-property-ado-md.md) см.</span><span class="sxs-lookup"><span data-stu-id="452d4-110">For more information about the various types of members, see the [Type](type-property-ado-md.md) property.</span></span>

<span data-ttu-id="452d4-111">Это свойство поддерживается только для объектов **члена** , принадлежащих к объекту [уровень](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="452d4-111">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="452d4-112">Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="452d4-112">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>


---
title: Свойство Description (ADO MD)
TOCTitle: Description property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cf0e9751e822e5ff2250a15138546678deb76bc8
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921098"
---
# <a name="description-property-ado-md"></a><span data-ttu-id="49dfe-102">Свойство Description (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="49dfe-102">Description property (ADO MD)</span></span>


<span data-ttu-id="49dfe-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49dfe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49dfe-104">Возвращает описание текста текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="49dfe-104">Returns a text explanation of the current object.</span></span>

## <a name="return-values"></a><span data-ttu-id="49dfe-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="49dfe-105">Return values</span></span>

<span data-ttu-id="49dfe-106">Возвращает **строку** и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="49dfe-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="49dfe-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="49dfe-107">Remarks</span></span>

<span data-ttu-id="49dfe-108">Для объектов [члена](member-object-ado-md.md) **Описание** относится только к измерения и формул элементы.</span><span class="sxs-lookup"><span data-stu-id="49dfe-108">For [Member](member-object-ado-md.md) objects, **Description** applies only to measure and formula members.</span></span> <span data-ttu-id="49dfe-109">**Описание** возвращает пустую строку ("») для всех остальных типов элементов.</span><span class="sxs-lookup"><span data-stu-id="49dfe-109">**Description** returns an empty string ("") for all other types of members.</span></span> <span data-ttu-id="49dfe-110">Дополнительные сведения о различных типах элементов [типа](type-property-ado-md.md) см.</span><span class="sxs-lookup"><span data-stu-id="49dfe-110">For more information about the various types of members, see the [Type](type-property-ado-md.md) property.</span></span>

<span data-ttu-id="49dfe-111">Это свойство поддерживается только для объектов **члена** , принадлежащих к объекту [уровень](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="49dfe-111">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object.</span></span> <span data-ttu-id="49dfe-112">Ошибка происходит, когда это свойство является ссылка из объектов **члена** , относящегося к объекту [позиции](position-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="49dfe-112">An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>


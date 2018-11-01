---
title: Метод CompareBookmarks (ADO)
TOCTitle: CompareBookmarks Method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 26f8cb17473daf21be3769f6f48a3bb368c1d082
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876976"
---
# <a name="comparebookmarks-method-ado"></a><span data-ttu-id="568b4-102">Метод CompareBookmarks (ADO)</span><span class="sxs-lookup"><span data-stu-id="568b4-102">CompareBookmarks Method (ADO)</span></span>


<span data-ttu-id="568b4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="568b4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="568b4-104">Сравнение двух закладки и возвращает сведения об их значения.</span><span class="sxs-lookup"><span data-stu-id="568b4-104">Compares two bookmarks and returns an indication of their relative values.</span></span>

## <a name="syntax"></a><span data-ttu-id="568b4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="568b4-105">Syntax</span></span>

<span data-ttu-id="568b4-106">*результат* = *набора записей*. CompareBookmarks (*Bookmark1*, *Bookmark2*)</span><span class="sxs-lookup"><span data-stu-id="568b4-106">*result* = *recordset*.CompareBookmarks(*Bookmark1*, *Bookmark2*)</span></span>

## <a name="return-value"></a><span data-ttu-id="568b4-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="568b4-107">Return value</span></span>

<span data-ttu-id="568b4-108">Возвращает [CompareEnum](compareenum.md) значение, указывающее положение относительно строки из двух записей, представленное закладок.</span><span class="sxs-lookup"><span data-stu-id="568b4-108">Returns a [CompareEnum](compareenum.md) value that indicates the relative row position of two records represented by their bookmarks.</span></span>

## <a name="parameters"></a><span data-ttu-id="568b4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="568b4-109">Parameters</span></span>

  - <span data-ttu-id="568b4-110">*Bookmark1*</span><span class="sxs-lookup"><span data-stu-id="568b4-110">*Bookmark1*</span></span>

  - <span data-ttu-id="568b4-111">Закладка первой строки.</span><span class="sxs-lookup"><span data-stu-id="568b4-111">The bookmark of the first row.</span></span>

  - <span data-ttu-id="568b4-112">*Bookmark2*</span><span class="sxs-lookup"><span data-stu-id="568b4-112">*Bookmark2*</span></span>

  - <span data-ttu-id="568b4-113">Закладка второй строке.</span><span class="sxs-lookup"><span data-stu-id="568b4-113">The bookmark of the second row.</span></span>

## <a name="remarks"></a><span data-ttu-id="568b4-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="568b4-114">Remarks</span></span>

<span data-ttu-id="568b4-115">Закладки необходимо установить на тот же объект [набора записей](recordset-object-ado.md) или объекта **набора записей** и его [копия](clone-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="568b4-115">The bookmarks must apply to the same [Recordset](recordset-object-ado.md) object, or a **Recordset** object and its [clone](clone-method-ado.md).</span></span> <span data-ttu-id="568b4-116">Сравнение надежно закладок из разных объектов **набора записей** , даже в том случае, если они были созданы на основе команду или источника.</span><span class="sxs-lookup"><span data-stu-id="568b4-116">You cannot reliably compare bookmarks from different **Recordset** objects, even if they were created from the same source or command.</span></span> <span data-ttu-id="568b4-117">Ни сравнение закладки для объекта **набора записей** , основной поставщик не поддерживает сравнения.</span><span class="sxs-lookup"><span data-stu-id="568b4-117">Nor can you compare bookmarks for a **Recordset** object whose underlying provider does not support comparisons.</span></span>

<span data-ttu-id="568b4-118">Закладка уникально идентифицирует строки в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="568b4-118">A bookmark uniquely identifies a row in a **Recordset** object.</span></span> <span data-ttu-id="568b4-119">Свойство [закладку](bookmark-property-ado.md) текущей строки используется для получения ее закладки.</span><span class="sxs-lookup"><span data-stu-id="568b4-119">Use the current row's [Bookmark](bookmark-property-ado.md) property to obtain its bookmark.</span></span>

<span data-ttu-id="568b4-120">Так как тип данных закладки зависит от поставщика, ADO представляет его как переменную типа Variant.</span><span class="sxs-lookup"><span data-stu-id="568b4-120">Because the data type of a bookmark is provider specific, ADO exposes it as a Variant.</span></span> <span data-ttu-id="568b4-121">К примеру, закладки SQL Server имеют тип DBTYPE\_R8 (Double).</span><span class="sxs-lookup"><span data-stu-id="568b4-121">For example, SQL Server bookmarks are of type DBTYPE\_R8 (Double).</span></span> <span data-ttu-id="568b4-122">ADO предоставить этот тип в качестве типа Variant с подтипом типа Double.</span><span class="sxs-lookup"><span data-stu-id="568b4-122">ADO would expose this type as a Variant with a subtype of Double.</span></span>

<span data-ttu-id="568b4-123">При сравнении закладки, ADO не пытается любого типа приведения.</span><span class="sxs-lookup"><span data-stu-id="568b4-123">When comparing bookmarks, ADO does not attempt any type of coercion.</span></span> <span data-ttu-id="568b4-124">Значения, просто передаются в поставщик где происходит сравнить.</span><span class="sxs-lookup"><span data-stu-id="568b4-124">The values are simply passed to the provider where the compare occurs.</span></span> <span data-ttu-id="568b4-125">Если закладки, переданной в метод **CompareBookmarks** хранятся в переменных различных типов, его можно создать ошибка type mismatch «Аргументы имеют неправильный тип, находятся вне допустимого диапазона или конфликтуют друг с другом.»</span><span class="sxs-lookup"><span data-stu-id="568b4-125">If bookmarks passed to the **CompareBookmarks** method are stored in variables of differing types, it can generate the type mismatch error, "Arguments are of the wrong type, are out of the acceptable range, or are in conflict with each other."</span></span>

<span data-ttu-id="568b4-126">Закладки, который не является допустимым или неправильно сформированные приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="568b4-126">A bookmark that is not valid or incorrectly formed will cause an error.</span></span>


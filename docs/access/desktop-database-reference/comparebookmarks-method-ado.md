---
title: Метод CompareBookmarks (ADO)
TOCTitle: CompareBookmarks method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 460a77284141daad1834699c4dc1775be05c5c26
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296096"
---
# <a name="comparebookmarks-method-ado"></a><span data-ttu-id="d2cbf-102">Метод CompareBookmarks (ADO)</span><span class="sxs-lookup"><span data-stu-id="d2cbf-102">CompareBookmarks method (ADO)</span></span>

<span data-ttu-id="d2cbf-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2cbf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2cbf-104">Сравнивает две закладки и возвращает сведения об их относительных значениях.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-104">Compares two bookmarks and returns an indication of their relative values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2cbf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2cbf-105">Syntax</span></span>

<span data-ttu-id="d2cbf-106">*результирующий* = *набор записей*. CompareBookmarks (*Bookmark1*, *Bookmark2*)</span><span class="sxs-lookup"><span data-stu-id="d2cbf-106">*result* = *recordset*.CompareBookmarks(*Bookmark1*, *Bookmark2*)</span></span>

## <a name="return-value"></a><span data-ttu-id="d2cbf-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2cbf-107">Return value</span></span>

<span data-ttu-id="d2cbf-108">Возвращает значение [компаринум](compareenum.md) , которое указывает положение относительной строки двух записей, представленных своими закладками.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-108">Returns a [CompareEnum](compareenum.md) value that indicates the relative row position of two records represented by their bookmarks.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2cbf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2cbf-109">Parameters</span></span>

|<span data-ttu-id="d2cbf-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="d2cbf-110">Parameter</span></span>|<span data-ttu-id="d2cbf-111">Описание</span><span class="sxs-lookup"><span data-stu-id="d2cbf-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d2cbf-112">*Bookmark1*</span><span class="sxs-lookup"><span data-stu-id="d2cbf-112">*Bookmark1*</span></span> |<span data-ttu-id="d2cbf-113">Закладка первой строки.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-113">The bookmark of the first row.</span></span>|
|<span data-ttu-id="d2cbf-114">*Bookmark2*</span><span class="sxs-lookup"><span data-stu-id="d2cbf-114">*Bookmark2*</span></span> |<span data-ttu-id="d2cbf-115">Закладка второй строки.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-115">The bookmark of the second row.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d2cbf-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="d2cbf-116">Remarks</span></span>

<span data-ttu-id="d2cbf-117">Закладки должны применяться к одному объекту [Recordset](recordset-object-ado.md) или объекту **Recordset** и его [клону](clone-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="d2cbf-117">The bookmarks must apply to the same [Recordset](recordset-object-ado.md) object, or a **Recordset** object and its [clone](clone-method-ado.md).</span></span> <span data-ttu-id="d2cbf-118">Вы не можете надежно сравнивать закладки из разных объектов **Recordset** , даже если они были созданы с помощью одного и того же источника или команды.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-118">You cannot reliably compare bookmarks from different **Recordset** objects, even if they were created from the same source or command.</span></span> <span data-ttu-id="d2cbf-119">Также можно сравнивать закладки для объекта **Recordset** , базовый поставщик которого не поддерживает сравнения.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-119">Nor can you compare bookmarks for a **Recordset** object whose underlying provider does not support comparisons.</span></span>

<span data-ttu-id="d2cbf-120">Закладка уникально идентифицирует строку в объекте **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="d2cbf-120">A bookmark uniquely identifies a row in a **Recordset** object.</span></span> <span data-ttu-id="d2cbf-121">Используйте свойство [Bookmark](bookmark-property-ado.md) текущей строки, чтобы получить его закладку.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-121">Use the current row's [Bookmark](bookmark-property-ado.md) property to obtain its bookmark.</span></span>

<span data-ttu-id="d2cbf-122">Так как тип данных закладки относится к конкретному поставщику, ADO предоставляет его как вариант.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-122">Because the data type of a bookmark is provider specific, ADO exposes it as a Variant.</span></span> <span data-ttu-id="d2cbf-123">Например, закладки SQL Server имеют тип DBTYPE\_R8 (Double).</span><span class="sxs-lookup"><span data-stu-id="d2cbf-123">For example, SQL Server bookmarks are of type DBTYPE\_R8 (Double).</span></span> <span data-ttu-id="d2cbf-124">ADO предоставит этот тип как Variant с подтипом Double.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-124">ADO would expose this type as a Variant with a subtype of Double.</span></span>

<span data-ttu-id="d2cbf-125">При сравнении закладок ADO не пытается приведение типов.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-125">When comparing bookmarks, ADO does not attempt any type of coercion.</span></span> <span data-ttu-id="d2cbf-126">Значения просто передаются поставщику, на котором выполняется сравнение.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-126">The values are simply passed to the provider where the compare occurs.</span></span> <span data-ttu-id="d2cbf-127">Если закладки, переданные в метод **CompareBookmarks** , хранятся в переменных различных типов, может возникать ошибка несовпадения типов, "аргументы имеют неправильный тип, выходят из допустимого диапазона или конфликтуют друг с другом".</span><span class="sxs-lookup"><span data-stu-id="d2cbf-127">If bookmarks passed to the **CompareBookmarks** method are stored in variables of differing types, it can generate the type mismatch error, "Arguments are of the wrong type, are out of the acceptable range, or are in conflict with each other."</span></span>

<span data-ttu-id="d2cbf-128">Недопустимый или неправильно сформированный закладка приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-128">A bookmark that is not valid or incorrectly formed will cause an error.</span></span>


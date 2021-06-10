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
# <a name="comparebookmarks-method-ado"></a><span data-ttu-id="4dd6b-102">Метод CompareBookmarks (ADO)</span><span class="sxs-lookup"><span data-stu-id="4dd6b-102">CompareBookmarks method (ADO)</span></span>

<span data-ttu-id="4dd6b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4dd6b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4dd6b-104">Сравнивает две закладки и возвращает указание их относительных значений.</span><span class="sxs-lookup"><span data-stu-id="4dd6b-104">Compares two bookmarks and returns an indication of their relative values.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd6b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4dd6b-105">Syntax</span></span>

<span data-ttu-id="4dd6b-106">*результат*  =  *набор записей.* CompareBookmarks *(Bookmark1*, *Bookmark2*)</span><span class="sxs-lookup"><span data-stu-id="4dd6b-106">*result* = *recordset*.CompareBookmarks(*Bookmark1*, *Bookmark2*)</span></span>

## <a name="return-value"></a><span data-ttu-id="4dd6b-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4dd6b-107">Return value</span></span>

<span data-ttu-id="4dd6b-108">Возвращает значение [CompareEnum,](compareenum.md) которое указывает относительное положение строки двух записей, представленных их закладки.</span><span class="sxs-lookup"><span data-stu-id="4dd6b-108">Returns a [CompareEnum](compareenum.md) value that indicates the relative row position of two records represented by their bookmarks.</span></span>

## <a name="parameters"></a><span data-ttu-id="4dd6b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4dd6b-109">Parameters</span></span>

|<span data-ttu-id="4dd6b-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="4dd6b-110">Parameter</span></span>|<span data-ttu-id="4dd6b-111">Описание</span><span class="sxs-lookup"><span data-stu-id="4dd6b-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4dd6b-112">*Bookmark1*</span><span class="sxs-lookup"><span data-stu-id="4dd6b-112">*Bookmark1*</span></span> |<span data-ttu-id="4dd6b-113">Закладка первой строки.</span><span class="sxs-lookup"><span data-stu-id="4dd6b-113">The bookmark of the first row.</span></span>|
|<span data-ttu-id="4dd6b-114">*Bookmark2*</span><span class="sxs-lookup"><span data-stu-id="4dd6b-114">*Bookmark2*</span></span> |<span data-ttu-id="4dd6b-115">Закладка второго ряда.</span><span class="sxs-lookup"><span data-stu-id="4dd6b-115">The bookmark of the second row.</span></span>|

## <a name="remarks"></a><span data-ttu-id="4dd6b-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="4dd6b-116">Remarks</span></span>

<span data-ttu-id="4dd6b-117">Закладки должны применяться к одному объекту [Recordset](recordset-object-ado.md) или **объекту Recordset** и его [клону.](clone-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4dd6b-117">The bookmarks must apply to the same [Recordset](recordset-object-ado.md) object, or a **Recordset** object and its [clone](clone-method-ado.md).</span></span> <span data-ttu-id="4dd6b-118">Невозможно надежно сравнить закладки из различных объектов **Recordset,** даже если они были созданы из одного источника или команды.</span><span class="sxs-lookup"><span data-stu-id="4dd6b-118">You cannot reliably compare bookmarks from different **Recordset** objects, even if they were created from the same source or command.</span></span> <span data-ttu-id="4dd6b-119">Нельзя также сравнивать закладки для объекта **Recordset,** чей поставщик не поддерживает сравнения.</span><span class="sxs-lookup"><span data-stu-id="4dd6b-119">Nor can you compare bookmarks for a **Recordset** object whose underlying provider does not support comparisons.</span></span>

<span data-ttu-id="4dd6b-120">Закладки однозначно идентифицируют строку в **объекте Recordset.**</span><span class="sxs-lookup"><span data-stu-id="4dd6b-120">A bookmark uniquely identifies a row in a **Recordset** object.</span></span> <span data-ttu-id="4dd6b-121">Чтобы получить закладки, используйте свойство [Закладки](bookmark-property-ado.md) текущей строки.</span><span class="sxs-lookup"><span data-stu-id="4dd6b-121">Use the current row's [Bookmark](bookmark-property-ado.md) property to obtain its bookmark.</span></span>

<span data-ttu-id="4dd6b-122">Так как тип данных закладки является конкретным поставщиком, ADO предоставляет его как Вариант.</span><span class="sxs-lookup"><span data-stu-id="4dd6b-122">Because the data type of a bookmark is provider specific, ADO exposes it as a Variant.</span></span> <span data-ttu-id="4dd6b-123">Например, SQL Server закладки типа DBTYPE \_ R8 (Double).</span><span class="sxs-lookup"><span data-stu-id="4dd6b-123">For example, SQL Server bookmarks are of type DBTYPE\_R8 (Double).</span></span> <span data-ttu-id="4dd6b-124">ADO выставит этот тип как вариант с подтипом Double.</span><span class="sxs-lookup"><span data-stu-id="4dd6b-124">ADO would expose this type as a Variant with a subtype of Double.</span></span>

<span data-ttu-id="4dd6b-125">При сравнении закладок ADO не пытается принуждения.</span><span class="sxs-lookup"><span data-stu-id="4dd6b-125">When comparing bookmarks, ADO does not attempt any type of coercion.</span></span> <span data-ttu-id="4dd6b-126">Значения просто передаются поставщику, где происходит сравнение.</span><span class="sxs-lookup"><span data-stu-id="4dd6b-126">The values are simply passed to the provider where the compare occurs.</span></span> <span data-ttu-id="4dd6b-127">Если закладки, переданные методу **CompareBookmarks,** хранятся в переменных различных типов, это может привести к ошибке несоответствия типа: "Аргументы неправильного типа, находятся вне допустимого диапазона или находятся в конфликте друг с другом".</span><span class="sxs-lookup"><span data-stu-id="4dd6b-127">If bookmarks passed to the **CompareBookmarks** method are stored in variables of differing types, it can generate the type mismatch error, "Arguments are of the wrong type, are out of the acceptable range, or are in conflict with each other."</span></span>

<span data-ttu-id="4dd6b-128">Закладки, которые не являются действительными или неправильно сформированы приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="4dd6b-128">A bookmark that is not valid or incorrectly formed will cause an error.</span></span>


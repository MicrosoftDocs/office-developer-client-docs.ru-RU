---
title: Метод GetString (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ea28efb8fdeaa0643d1d940419b7650527ddf6e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292190"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="3b3e6-102">Метод GetString (ADO)</span><span class="sxs-lookup"><span data-stu-id="3b3e6-102">GetString method (ADO)</span></span>

<span data-ttu-id="3b3e6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b3e6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b3e6-104">Возвращает набор [записей в](recordset-object-ado.md) качестве строки.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b3e6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b3e6-105">Syntax</span></span>

<span data-ttu-id="3b3e6-106">*Variant*  =  *recordset*. GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="3b3e6-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="3b3e6-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3b3e6-107">Return value</span></span>

<span data-ttu-id="3b3e6-108">Возвращает набор **записей в** качестве значения строки **Variant** (BSTR).</span><span class="sxs-lookup"><span data-stu-id="3b3e6-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="3b3e6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b3e6-109">Parameters</span></span>

|<span data-ttu-id="3b3e6-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="3b3e6-110">Parameter</span></span>|<span data-ttu-id="3b3e6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3b3e6-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3b3e6-112">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="3b3e6-112">*StringFormat*</span></span> |<span data-ttu-id="3b3e6-113">Значение [StringFormatEnum,](stringformatenum.md) которое указывает, как **набор записей** должен быть преобразован в строку.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-113">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string.</span></span> <span data-ttu-id="3b3e6-114">Параметры *RowDelimiter,* *ColumnDelimiter* и *NullExpr* используются только с *параметром StringFormat* **adClipString.**</span><span class="sxs-lookup"><span data-stu-id="3b3e6-114">The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>|
|<span data-ttu-id="3b3e6-115">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="3b3e6-115">*NumRows*</span></span> |<span data-ttu-id="3b3e6-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-116">Optional.</span></span> <span data-ttu-id="3b3e6-117">Количество строк, которые необходимо преобразовать в **наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="3b3e6-117">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="3b3e6-118">Если *NumRows* не указан или превышает общее число строк в наборе **recordset,** то все строки в **наборе Recordset** преобразуются.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-118">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>|
|<span data-ttu-id="3b3e6-119">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="3b3e6-119">*ColumnDelimiter*</span></span> |<span data-ttu-id="3b3e6-120">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-120">Optional.</span></span> <span data-ttu-id="3b3e6-121">В противном случае используется разнородных столбцов, если они указаны, в противном случае символ TAB.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-121">A delimiter used between columns, if specified, otherwise the TAB character.</span></span>|
|<span data-ttu-id="3b3e6-122">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="3b3e6-122">*RowDelimiter*</span></span> |<span data-ttu-id="3b3e6-123">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-123">Optional.</span></span> <span data-ttu-id="3b3e6-124">В противном случае используется разность между строками, если они указаны, в противном случае символ ВОЗВРАТА КАРЕТА.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-124">A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>|
|<span data-ttu-id="3b3e6-125">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="3b3e6-125">*NullExpr*</span></span> |<span data-ttu-id="3b3e6-126">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-126">Optional.</span></span> <span data-ttu-id="3b3e6-127">Выражение, используемое в качестве значения null,если указано, в противном случае пустая строка.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-127">An expression used in place of a null value, if specified, otherwise the empty string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="3b3e6-128">Заметки</span><span class="sxs-lookup"><span data-stu-id="3b3e6-128">Remarks</span></span>

<span data-ttu-id="3b3e6-129">Данные строки, но не данные схемы, сохраняются в строке.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-129">Row data, but no schema data, is saved to the string.</span></span> <span data-ttu-id="3b3e6-130">Поэтому набор **записей нельзя** повторно открыть с помощью этой строки.</span><span class="sxs-lookup"><span data-stu-id="3b3e6-130">Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="3b3e6-131">Этот метод эквивалентен методу RDO **GetClipString.**</span><span class="sxs-lookup"><span data-stu-id="3b3e6-131">This method is equivalent to the RDO **GetClipString** method.</span></span>


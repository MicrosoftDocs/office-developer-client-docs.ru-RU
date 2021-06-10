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
# <a name="getstring-method-ado"></a><span data-ttu-id="8eeb7-102">Метод GetString (ADO)</span><span class="sxs-lookup"><span data-stu-id="8eeb7-102">GetString method (ADO)</span></span>

<span data-ttu-id="8eeb7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8eeb7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8eeb7-104">Возвращает набор [записей в](recordset-object-ado.md) качестве строки.</span><span class="sxs-lookup"><span data-stu-id="8eeb7-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eeb7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8eeb7-105">Syntax</span></span>

<span data-ttu-id="8eeb7-106">*Variant*  =  *набор записей.* GetString *(StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="8eeb7-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="8eeb7-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8eeb7-107">Return value</span></span>

<span data-ttu-id="8eeb7-108">Возвращает набор **записей** в качестве строковой версии **(BSTR).**</span><span class="sxs-lookup"><span data-stu-id="8eeb7-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="8eeb7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8eeb7-109">Parameters</span></span>

|<span data-ttu-id="8eeb7-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="8eeb7-110">Parameter</span></span>|<span data-ttu-id="8eeb7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8eeb7-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8eeb7-112">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="8eeb7-112">*StringFormat*</span></span> |<span data-ttu-id="8eeb7-113">Значение [StringFormatEnum,](stringformatenum.md) которое указывает, как следует преобразовать **набор recordset** в строку.</span><span class="sxs-lookup"><span data-stu-id="8eeb7-113">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string.</span></span> <span data-ttu-id="8eeb7-114">Параметры *RowDelimiter,* *ColumnDelimiter* и *NullExpr* используются только с *помощью stringFormat* **adClipString.**</span><span class="sxs-lookup"><span data-stu-id="8eeb7-114">The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>|
|<span data-ttu-id="8eeb7-115">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="8eeb7-115">*NumRows*</span></span> |<span data-ttu-id="8eeb7-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="8eeb7-116">Optional.</span></span> <span data-ttu-id="8eeb7-117">Количество строк, которые необходимо преобразовать в **Наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="8eeb7-117">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="8eeb7-118">Если *NumRows* не указан или больше общего числа строк в **Наборе** записей, то все строки в **Наборе** записей преобразуются.</span><span class="sxs-lookup"><span data-stu-id="8eeb7-118">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>|
|<span data-ttu-id="8eeb7-119">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="8eeb7-119">*ColumnDelimiter*</span></span> |<span data-ttu-id="8eeb7-120">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="8eeb7-120">Optional.</span></span> <span data-ttu-id="8eeb7-121">Делимитер, используемый между столбцами, если задан, в противном случае символ TAB.</span><span class="sxs-lookup"><span data-stu-id="8eeb7-121">A delimiter used between columns, if specified, otherwise the TAB character.</span></span>|
|<span data-ttu-id="8eeb7-122">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="8eeb7-122">*RowDelimiter*</span></span> |<span data-ttu-id="8eeb7-123">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="8eeb7-123">Optional.</span></span> <span data-ttu-id="8eeb7-124">Делимитер, используемый между строками, если задан, в противном случае символ CARRIAGE RETURN.</span><span class="sxs-lookup"><span data-stu-id="8eeb7-124">A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>|
|<span data-ttu-id="8eeb7-125">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="8eeb7-125">*NullExpr*</span></span> |<span data-ttu-id="8eeb7-126">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="8eeb7-126">Optional.</span></span> <span data-ttu-id="8eeb7-127">Выражение, используемое на месте значения null, если указано, в противном случае пустая строка.</span><span class="sxs-lookup"><span data-stu-id="8eeb7-127">An expression used in place of a null value, if specified, otherwise the empty string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="8eeb7-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="8eeb7-128">Remarks</span></span>

<span data-ttu-id="8eeb7-129">Данные строки, но не данные схемы, сохраняются в строке.</span><span class="sxs-lookup"><span data-stu-id="8eeb7-129">Row data, but no schema data, is saved to the string.</span></span> <span data-ttu-id="8eeb7-130">Поэтому с помощью этой **строки нельзя** открыть набор recordset.</span><span class="sxs-lookup"><span data-stu-id="8eeb7-130">Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="8eeb7-131">Этот метод эквивалентен методу **RDO GetClipString.**</span><span class="sxs-lookup"><span data-stu-id="8eeb7-131">This method is equivalent to the RDO **GetClipString** method.</span></span>


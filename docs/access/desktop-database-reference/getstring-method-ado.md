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
# <a name="getstring-method-ado"></a><span data-ttu-id="feaf9-102">Метод GetString (ADO)</span><span class="sxs-lookup"><span data-stu-id="feaf9-102">GetString method (ADO)</span></span>

<span data-ttu-id="feaf9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="feaf9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="feaf9-104">Возвращает объект [Recordset](recordset-object-ado.md) в виде строки.</span><span class="sxs-lookup"><span data-stu-id="feaf9-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="feaf9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="feaf9-105">Syntax</span></span>

<span data-ttu-id="feaf9-106">*Variant* = *Набор записей*Variant. GetString (*стрингформат*, *нумровс*, *колумнделимитер*, *ровделимитер*, *нуллекспр*)</span><span class="sxs-lookup"><span data-stu-id="feaf9-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="feaf9-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="feaf9-107">Return value</span></span>

<span data-ttu-id="feaf9-108">Возвращает объект **Recordset** как **Variant** со строковым значением (BSTR).</span><span class="sxs-lookup"><span data-stu-id="feaf9-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="feaf9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="feaf9-109">Parameters</span></span>

|<span data-ttu-id="feaf9-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="feaf9-110">Parameter</span></span>|<span data-ttu-id="feaf9-111">Описание</span><span class="sxs-lookup"><span data-stu-id="feaf9-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="feaf9-112">*стрингформат*</span><span class="sxs-lookup"><span data-stu-id="feaf9-112">*StringFormat*</span></span> |<span data-ttu-id="feaf9-113">Значение [стрингформатенум](stringformatenum.md) , задающее способ преобразования **набора записей** в строку.</span><span class="sxs-lookup"><span data-stu-id="feaf9-113">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string.</span></span> <span data-ttu-id="feaf9-114">Параметры *ровделимитер*, *колумнделимитер*и *Нуллекспр* используются только в *стрингформат* **адклипстринг**.</span><span class="sxs-lookup"><span data-stu-id="feaf9-114">The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>|
|<span data-ttu-id="feaf9-115">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="feaf9-115">*NumRows*</span></span> |<span data-ttu-id="feaf9-116">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="feaf9-116">Optional.</span></span> <span data-ttu-id="feaf9-117">Число строк, преобразуемых в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="feaf9-117">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="feaf9-118">Если *нумровс* не указан или превышает общее количество строк в **наборе записей**, все строки в **наборе записей** преобразуются.</span><span class="sxs-lookup"><span data-stu-id="feaf9-118">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>|
|<span data-ttu-id="feaf9-119">*колумнделимитер*</span><span class="sxs-lookup"><span data-stu-id="feaf9-119">*ColumnDelimiter*</span></span> |<span data-ttu-id="feaf9-120">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="feaf9-120">Optional.</span></span> <span data-ttu-id="feaf9-121">Разделитель, используемый между столбцами, если он указан, в противном случае — символ ТАБУЛЯЦИи.</span><span class="sxs-lookup"><span data-stu-id="feaf9-121">A delimiter used between columns, if specified, otherwise the TAB character.</span></span>|
|<span data-ttu-id="feaf9-122">*ровделимитер*</span><span class="sxs-lookup"><span data-stu-id="feaf9-122">*RowDelimiter*</span></span> |<span data-ttu-id="feaf9-123">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="feaf9-123">Optional.</span></span> <span data-ttu-id="feaf9-124">Разделитель, используемый между строками, если он указан, в противном случае — символ возврата КАРЕТки.</span><span class="sxs-lookup"><span data-stu-id="feaf9-124">A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>|
|<span data-ttu-id="feaf9-125">*нуллекспр*</span><span class="sxs-lookup"><span data-stu-id="feaf9-125">*NullExpr*</span></span> |<span data-ttu-id="feaf9-126">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="feaf9-126">Optional.</span></span> <span data-ttu-id="feaf9-127">Выражение, используемое вместо значения NULL, если оно указано, в противном случае — пустая строка.</span><span class="sxs-lookup"><span data-stu-id="feaf9-127">An expression used in place of a null value, if specified, otherwise the empty string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="feaf9-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="feaf9-128">Remarks</span></span>

<span data-ttu-id="feaf9-129">Данные строки, но не данные схемы, сохраняются в строке.</span><span class="sxs-lookup"><span data-stu-id="feaf9-129">Row data, but no schema data, is saved to the string.</span></span> <span data-ttu-id="feaf9-130">Таким образом, невозможно повторно открыть объект **Recordset** с помощью этой строки.</span><span class="sxs-lookup"><span data-stu-id="feaf9-130">Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="feaf9-131">Этот метод эквивалентен методу RDO **жетклипстринг** .</span><span class="sxs-lookup"><span data-stu-id="feaf9-131">This method is equivalent to the RDO **GetClipString** method.</span></span>


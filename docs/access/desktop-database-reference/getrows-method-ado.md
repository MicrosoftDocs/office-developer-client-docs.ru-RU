---
title: GetRows Method (ADO)
TOCTitle: GetRows Method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b0f7f38e44e26238e5a55feaaad302bbf427d678
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606152"
---
# <a name="getrows-method-ado"></a><span data-ttu-id="a7da4-102">GetRows Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="a7da4-102">GetRows Method (ADO)</span></span>


<span data-ttu-id="a7da4-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7da4-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="a7da4-104">Извлекает нескольких записей объекта [набора записей](recordset-object-ado.md) в массив.</span><span class="sxs-lookup"><span data-stu-id="a7da4-104">Retrieves multiple records of a [Recordset](recordset-object-ado.md) object into an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7da4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7da4-105">Syntax</span></span>

<span data-ttu-id="a7da4-106">*Массив* = *набора записей*. Получение строк (*строк*, *запустите*, *полей* )</span><span class="sxs-lookup"><span data-stu-id="a7da4-106">*array* = *recordset*.GetRows(*Rows*, *Start*, *Fields* )</span></span>

<span data-ttu-id="a7da4-107"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="a7da4-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="a7da4-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7da4-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="a7da4-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7da4-109">Return value</span></span>
>>>>>>> <span data-ttu-id="a7da4-110">master</span><span class="sxs-lookup"><span data-stu-id="a7da4-110">master</span></span>

<span data-ttu-id="a7da4-111">Возвращает значение **типа Variant** , значение которого равно двумерного массива.</span><span class="sxs-lookup"><span data-stu-id="a7da4-111">Returns a **Variant** whose value is a two-dimensional array.</span></span>

## <a name="parameters"></a><span data-ttu-id="a7da4-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7da4-112">Parameters</span></span>

  - <span data-ttu-id="a7da4-113">*Строк*</span><span class="sxs-lookup"><span data-stu-id="a7da4-113">*Rows*</span></span>

  - <span data-ttu-id="a7da4-114">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="a7da4-114">Optional.</span></span> <span data-ttu-id="a7da4-115">[GetRowsOptionEnum](getrowsoptionenum.md) значение, указывающее количество записей для извлечения.</span><span class="sxs-lookup"><span data-stu-id="a7da4-115">A [GetRowsOptionEnum](getrowsoptionenum.md) value that indicates the number of records to retrieve.</span></span> <span data-ttu-id="a7da4-116">Значение по умолчанию — **adGetRowsRest**.</span><span class="sxs-lookup"><span data-stu-id="a7da4-116">The default is **adGetRowsRest**.</span></span>

  - <span data-ttu-id="a7da4-117">*Start*</span><span class="sxs-lookup"><span data-stu-id="a7da4-117">*Start*</span></span>

  - <span data-ttu-id="a7da4-118">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="a7da4-118">Optional.</span></span> <span data-ttu-id="a7da4-119">Значение **String** или **Variant** , которое оценивается как закладку для записи, с которого следует начать операции **получения строк** .</span><span class="sxs-lookup"><span data-stu-id="a7da4-119">A **String** value or **Variant** that evaluates to the bookmark for the record from which the **GetRows** operation should begin.</span></span> <span data-ttu-id="a7da4-120">Можно также использовать значение [BookmarkEnum](bookmarkenum.md) .</span><span class="sxs-lookup"><span data-stu-id="a7da4-120">You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>

  - <span data-ttu-id="a7da4-121">*Поля*</span><span class="sxs-lookup"><span data-stu-id="a7da4-121">*Fields*</span></span>

  - <span data-ttu-id="a7da4-122">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="a7da4-122">Optional.</span></span> <span data-ttu-id="a7da4-123">**Variant** , который представляет одного поля имя или порядковый номер или массив имена полей или номера порядковый номер.</span><span class="sxs-lookup"><span data-stu-id="a7da4-123">A **Variant** that represents a single field name or ordinal position, or an array of field names or ordinal position numbers.</span></span> <span data-ttu-id="a7da4-124">ADO возвращает только данные в этих полях.</span><span class="sxs-lookup"><span data-stu-id="a7da4-124">ADO returns only the data in these fields.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7da4-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="a7da4-125">Remarks</span></span>

<span data-ttu-id="a7da4-126">Используйте метод **получения строк** для копирования записей из **набора записей** в двумерного массива.</span><span class="sxs-lookup"><span data-stu-id="a7da4-126">Use the **GetRows** method to copy records from a **Recordset** into a two-dimensional array.</span></span> <span data-ttu-id="a7da4-127">Первый индекс определяет поля и второй номер записи.</span><span class="sxs-lookup"><span data-stu-id="a7da4-127">The first subscript identifies the field and the second identifies the record number.</span></span> <span data-ttu-id="a7da4-128">Переменной *массива* автоматически задан в правильном размере при возвращении метода **получения строк** данных.</span><span class="sxs-lookup"><span data-stu-id="a7da4-128">The *array* variable is automatically dimensioned to the correct size when the **GetRows** method returns the data.</span></span>

<span data-ttu-id="a7da4-129">Если не указать значение для аргумента *строк* , метод **получения строк** автоматически извлекает все записи в объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="a7da4-129">If you do not specify a value for the *Rows* argument, the **GetRows** method automatically retrieves all the records in the **Recordset** object.</span></span> <span data-ttu-id="a7da4-130">При запросе несколько записей, чем доступно, **Получение строк** возвращает число доступных записей.</span><span class="sxs-lookup"><span data-stu-id="a7da4-130">If you request more records than are available, **GetRows** returns only the number of available records.</span></span>

<span data-ttu-id="a7da4-131">Если объекта **набора записей** поддерживает закладки, можно указать, на какие записи метода **получения строк** должна начинать извлечения данных, передав значение свойства [Bookmark](bookmark-property-ado.md) этой записи в аргументе *запустить* .</span><span class="sxs-lookup"><span data-stu-id="a7da4-131">If the **Recordset** object supports bookmarks, you can specify at which record the **GetRows** method should begin retrieving data by passing the value of that record's [Bookmark](bookmark-property-ado.md) property in the *Start* argument.</span></span>

<span data-ttu-id="a7da4-132">Если требуется ограничить поля, возвращается **Получение строк** , вы можете передать одного поля имя или номер или массив имена и номера полей в аргументе *поля* .</span><span class="sxs-lookup"><span data-stu-id="a7da4-132">If you want to restrict the fields that the **GetRows** call returns, you can pass either a single field name/number or an array of field names/numbers in the *Fields* argument.</span></span>

<span data-ttu-id="a7da4-133">После вызова метода **получения строк**следующую запись непрочитанные становится текущей или свойство [EOF](bof-eof-properties-ado.md) имеет значение **True** , если нет несколько записей.</span><span class="sxs-lookup"><span data-stu-id="a7da4-133">After you call **GetRows**, the next unread record becomes the current record, or the [EOF](bof-eof-properties-ado.md) property is set to **True** if there are no more records.</span></span>


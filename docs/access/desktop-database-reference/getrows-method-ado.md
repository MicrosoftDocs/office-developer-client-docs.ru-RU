---
title: Метод GetRows (ADO)
TOCTitle: GetRows method (ADO)
ms:assetid: 570e6f1c-c17a-7d9a-c172-387894a3a1f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249292(v=office.15)
ms:contentKeyID: 48544963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 61f7ce441eb837b76e824b55393741e0cf821bb5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292225"
---
# <a name="getrows-method-ado"></a><span data-ttu-id="a8667-102">Метод GetRows (ADO)</span><span class="sxs-lookup"><span data-stu-id="a8667-102">GetRows method (ADO)</span></span>

<span data-ttu-id="a8667-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8667-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a8667-104">Извлекает несколько записей объекта [Recordset](recordset-object-ado.md) в массив.</span><span class="sxs-lookup"><span data-stu-id="a8667-104">Retrieves multiple records of a [Recordset](recordset-object-ado.md) object into an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8667-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8667-105">Syntax</span></span>

<span data-ttu-id="a8667-106">*array*  =  *recordset*. GetRows(*Rows,* *Start*, *Fields* )</span><span class="sxs-lookup"><span data-stu-id="a8667-106">*array* = *recordset*.GetRows(*Rows*, *Start*, *Fields* )</span></span>

## <a name="return-value"></a><span data-ttu-id="a8667-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8667-107">Return value</span></span>

<span data-ttu-id="a8667-108">Возвращает **вариант,** значение которого является двумерным массивом.</span><span class="sxs-lookup"><span data-stu-id="a8667-108">Returns a **Variant** whose value is a two-dimensional array.</span></span>

## <a name="parameters"></a><span data-ttu-id="a8667-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8667-109">Parameters</span></span>

|<span data-ttu-id="a8667-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="a8667-110">Parameter</span></span>|<span data-ttu-id="a8667-111">Описание</span><span class="sxs-lookup"><span data-stu-id="a8667-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a8667-112">*Rows*</span><span class="sxs-lookup"><span data-stu-id="a8667-112">*Rows*</span></span> |<span data-ttu-id="a8667-113">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="a8667-113">Optional.</span></span> <span data-ttu-id="a8667-114">Значение [GetRowsOptionEnum,](getrowsoptionenum.md) которое указывает количество извлекаемой записи.</span><span class="sxs-lookup"><span data-stu-id="a8667-114">A [GetRowsOptionEnum](getrowsoptionenum.md) value that indicates the number of records to retrieve.</span></span> <span data-ttu-id="a8667-115">Значение по умолчанию **— adGetRowsRest.**</span><span class="sxs-lookup"><span data-stu-id="a8667-115">The default is **adGetRowsRest**.</span></span>|
|<span data-ttu-id="a8667-116">*Начало*</span><span class="sxs-lookup"><span data-stu-id="a8667-116">*Start*</span></span> |<span data-ttu-id="a8667-117">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="a8667-117">Optional.</span></span> <span data-ttu-id="a8667-118">Строка или **значение Variant,** оцениваемая в закладке для записи, с которой должна начинаться операция  **GetRows.**</span><span class="sxs-lookup"><span data-stu-id="a8667-118">A **String** value or **Variant** that evaluates to the bookmark for the record from which the **GetRows** operation should begin.</span></span> <span data-ttu-id="a8667-119">Также можно использовать значение [BookmarkEnum.](bookmarkenum.md)</span><span class="sxs-lookup"><span data-stu-id="a8667-119">You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>|
|<span data-ttu-id="a8667-120">*Fields*</span><span class="sxs-lookup"><span data-stu-id="a8667-120">*Fields*</span></span> |<span data-ttu-id="a8667-121">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="a8667-121">Optional.</span></span> <span data-ttu-id="a8667-122">**Вариант,** который представляет одно имя поля или порядковую позицию, или массив имен полей или порядковых номеров позиции.</span><span class="sxs-lookup"><span data-stu-id="a8667-122">A **Variant** that represents a single field name or ordinal position, or an array of field names or ordinal position numbers.</span></span> <span data-ttu-id="a8667-123">ADO возвращает только данные в этих полях.</span><span class="sxs-lookup"><span data-stu-id="a8667-123">ADO returns only the data in these fields.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a8667-124">Заметки</span><span class="sxs-lookup"><span data-stu-id="a8667-124">Remarks</span></span>

<span data-ttu-id="a8667-125">Используйте метод **GetRows** для копирования записей из **объекта Recordset** в двумерный массив.</span><span class="sxs-lookup"><span data-stu-id="a8667-125">Use the **GetRows** method to copy records from a **Recordset** into a two-dimensional array.</span></span> <span data-ttu-id="a8667-126">Первый подписок определяет поле, а второй определяет номер записи.</span><span class="sxs-lookup"><span data-stu-id="a8667-126">The first subscript identifies the field and the second identifies the record number.</span></span> <span data-ttu-id="a8667-127">*Переменная* массива автоматически размерируется до нужного размера, когда метод **GetRows** возвращает данные.</span><span class="sxs-lookup"><span data-stu-id="a8667-127">The *array* variable is automatically dimensioned to the correct size when the **GetRows** method returns the data.</span></span>

<span data-ttu-id="a8667-128">Если значение аргумента *Rows* не указано, метод **GetRows** автоматически извлекает все записи в **объекте Recordset.**</span><span class="sxs-lookup"><span data-stu-id="a8667-128">If you do not specify a value for the *Rows* argument, the **GetRows** method automatically retrieves all the records in the **Recordset** object.</span></span> <span data-ttu-id="a8667-129">Если запрашивается больше записей, чем доступно, **GetRows** возвращает только количество доступных записей.</span><span class="sxs-lookup"><span data-stu-id="a8667-129">If you request more records than are available, **GetRows** returns only the number of available records.</span></span>

<span data-ttu-id="a8667-130">Если объект **Recordset** поддерживает закладки, можно указать, с какой записи метод **GetRows** должен начать получать данные, передав значение свойства [bookmark](bookmark-property-ado.md) этой записи в аргументе *Start.*</span><span class="sxs-lookup"><span data-stu-id="a8667-130">If the **Recordset** object supports bookmarks, you can specify at which record the **GetRows** method should begin retrieving data by passing the value of that record's [Bookmark](bookmark-property-ado.md) property in the *Start* argument.</span></span>

<span data-ttu-id="a8667-131">Если необходимо ограничить поля, возвращаемые вызовом **GetRows,** можно передать одно имя/номер поля или массив имен и номеров полей в *аргументе Fields.*</span><span class="sxs-lookup"><span data-stu-id="a8667-131">If you want to restrict the fields that the **GetRows** call returns, you can pass either a single field name/number or an array of field names/numbers in the *Fields* argument.</span></span>

<span data-ttu-id="a8667-132">После вызова **GetRows** следующая непрочитанные записи становится текущей записью,  или свойство [EOF](bof-eof-properties-ado.md) имеет true, если больше нет записей.</span><span class="sxs-lookup"><span data-stu-id="a8667-132">After you call **GetRows**, the next unread record becomes the current record, or the [EOF](bof-eof-properties-ado.md) property is set to **True** if there are no more records.</span></span>


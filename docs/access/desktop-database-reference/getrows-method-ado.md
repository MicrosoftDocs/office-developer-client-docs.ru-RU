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
# <a name="getrows-method-ado"></a><span data-ttu-id="f86ca-102">Метод GetRows (ADO)</span><span class="sxs-lookup"><span data-stu-id="f86ca-102">GetRows method (ADO)</span></span>

<span data-ttu-id="f86ca-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f86ca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f86ca-104">Получает несколько записей объекта [Recordset](recordset-object-ado.md) в массив.</span><span class="sxs-lookup"><span data-stu-id="f86ca-104">Retrieves multiple records of a [Recordset](recordset-object-ado.md) object into an array.</span></span>

## <a name="syntax"></a><span data-ttu-id="f86ca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f86ca-105">Syntax</span></span>

<span data-ttu-id="f86ca-106">*массив* = *Recordset*. GetRows (*строки*, *Начало*, *поля* )</span><span class="sxs-lookup"><span data-stu-id="f86ca-106">*array* = *recordset*.GetRows(*Rows*, *Start*, *Fields* )</span></span>

## <a name="return-value"></a><span data-ttu-id="f86ca-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f86ca-107">Return value</span></span>

<span data-ttu-id="f86ca-108">Возвращает объект **Variant** , значение которого является двумерным массивом.</span><span class="sxs-lookup"><span data-stu-id="f86ca-108">Returns a **Variant** whose value is a two-dimensional array.</span></span>

## <a name="parameters"></a><span data-ttu-id="f86ca-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f86ca-109">Parameters</span></span>

|<span data-ttu-id="f86ca-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="f86ca-110">Parameter</span></span>|<span data-ttu-id="f86ca-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f86ca-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f86ca-112">*Rows*</span><span class="sxs-lookup"><span data-stu-id="f86ca-112">*Rows*</span></span> |<span data-ttu-id="f86ca-113">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="f86ca-113">Optional.</span></span> <span data-ttu-id="f86ca-114">Значение [жетровсоптионенум](getrowsoptionenum.md) , которое указывает количество извлекаемых записей.</span><span class="sxs-lookup"><span data-stu-id="f86ca-114">A [GetRowsOptionEnum](getrowsoptionenum.md) value that indicates the number of records to retrieve.</span></span> <span data-ttu-id="f86ca-115">Значение по умолчанию — **аджетровсрест**.</span><span class="sxs-lookup"><span data-stu-id="f86ca-115">The default is **adGetRowsRest**.</span></span>|
|<span data-ttu-id="f86ca-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="f86ca-116">*Start*</span></span> |<span data-ttu-id="f86ca-117">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="f86ca-117">Optional.</span></span> <span data-ttu-id="f86ca-118">**Строковое** значение или **Variant** , определяющее закладку для записи, из которой должна начинаться операция **GetRows** .</span><span class="sxs-lookup"><span data-stu-id="f86ca-118">A **String** value or **Variant** that evaluates to the bookmark for the record from which the **GetRows** operation should begin.</span></span> <span data-ttu-id="f86ca-119">Вы также можете использовать значение [букмаркенум](bookmarkenum.md) .</span><span class="sxs-lookup"><span data-stu-id="f86ca-119">You can also use a [BookmarkEnum](bookmarkenum.md) value.</span></span>|
|<span data-ttu-id="f86ca-120">*Fields*</span><span class="sxs-lookup"><span data-stu-id="f86ca-120">*Fields*</span></span> |<span data-ttu-id="f86ca-121">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="f86ca-121">Optional.</span></span> <span data-ttu-id="f86ca-122">**Variant** , представляющий одно имя поля или порядковый номер, или массив имен полей или номеров порядковых номеров.</span><span class="sxs-lookup"><span data-stu-id="f86ca-122">A **Variant** that represents a single field name or ordinal position, or an array of field names or ordinal position numbers.</span></span> <span data-ttu-id="f86ca-123">ADO возвращает только данные из этих полей.</span><span class="sxs-lookup"><span data-stu-id="f86ca-123">ADO returns only the data in these fields.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f86ca-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="f86ca-124">Remarks</span></span>

<span data-ttu-id="f86ca-125">Метод **GetRows** используется для копирования записей из **набора записей** в двухмерный массив.</span><span class="sxs-lookup"><span data-stu-id="f86ca-125">Use the **GetRows** method to copy records from a **Recordset** into a two-dimensional array.</span></span> <span data-ttu-id="f86ca-126">Первый подстрочный знак определяет поле, а второй — номер записи.</span><span class="sxs-lookup"><span data-stu-id="f86ca-126">The first subscript identifies the field and the second identifies the record number.</span></span> <span data-ttu-id="f86ca-127">Переменная *массива* автоматически изменяется до соответствующего размера, когда метод **GetRows** возвращает данные.</span><span class="sxs-lookup"><span data-stu-id="f86ca-127">The *array* variable is automatically dimensioned to the correct size when the **GetRows** method returns the data.</span></span>

<span data-ttu-id="f86ca-128">Если не указать значение аргумента Rows, метод *GetRows* автоматически извлекает все \*\*\*\* записи в объекте **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="f86ca-128">If you do not specify a value for the *Rows* argument, the **GetRows** method automatically retrieves all the records in the **Recordset** object.</span></span> <span data-ttu-id="f86ca-129">Если вы запрашиваете больше записей, чем доступно, **GetRows** возвращает только число доступных записей.</span><span class="sxs-lookup"><span data-stu-id="f86ca-129">If you request more records than are available, **GetRows** returns only the number of available records.</span></span>

<span data-ttu-id="f86ca-130">Если объект **Recordset** поддерживает закладки, можно указать, по какой записи метод **GetRows** должен начать извлечение данных, передав значение свойства [закладки](bookmark-property-ado.md) этой записи в аргументе *Start* .</span><span class="sxs-lookup"><span data-stu-id="f86ca-130">If the **Recordset** object supports bookmarks, you can specify at which record the **GetRows** method should begin retrieving data by passing the value of that record's [Bookmark](bookmark-property-ado.md) property in the *Start* argument.</span></span>

<span data-ttu-id="f86ca-131">Если необходимо ограничить количество полей, возвращаемых вызовом **GetRows** , можно передать одно имя или число или массив имен полей в аргументе *Fields* .</span><span class="sxs-lookup"><span data-stu-id="f86ca-131">If you want to restrict the fields that the **GetRows** call returns, you can pass either a single field name/number or an array of field names/numbers in the *Fields* argument.</span></span>

<span data-ttu-id="f86ca-132">После вызова **GetRows**Следующая непрочитанная запись становится текущей, или свойство [EOF](bof-eof-properties-ado.md) имеет значение **true** , если записей больше нет.</span><span class="sxs-lookup"><span data-stu-id="f86ca-132">After you call **GetRows**, the next unread record becomes the current record, or the [EOF](bof-eof-properties-ado.md) property is set to **True** if there are no more records.</span></span>


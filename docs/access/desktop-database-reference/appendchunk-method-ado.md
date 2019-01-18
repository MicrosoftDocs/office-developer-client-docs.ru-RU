---
title: Метод AppendChunk (ADO)
TOCTitle: AppendChunk method (ADO)
ms:assetid: 3fa931a3-2cd7-a3b0-a750-40e18bc9937e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249179(v=office.15)
ms:contentKeyID: 48544405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 89a75ebe8a3fe704c4f755a0f744eac4d068ec0a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702931"
---
# <a name="appendchunk-method-ado"></a><span data-ttu-id="b9c31-102">Метод AppendChunk (ADO)</span><span class="sxs-lookup"><span data-stu-id="b9c31-102">AppendChunk method (ADO)</span></span>

<span data-ttu-id="b9c31-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9c31-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b9c31-104">Добавляет данные большого текстового или двоичных данных [поля](field-object-ado.md)или к объекту [параметра](parameter-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b9c31-104">Appends data to a large text or binary data [Field](field-object-ado.md), or to a [Parameter](parameter-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9c31-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9c31-105">Syntax</span></span>

<span data-ttu-id="b9c31-106">*объект.* AppendChunk *данных*</span><span class="sxs-lookup"><span data-stu-id="b9c31-106">*object.* AppendChunk *Data*</span></span>

## <a name="parameters"></a><span data-ttu-id="b9c31-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="b9c31-107">Parameters</span></span>

|<span data-ttu-id="b9c31-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="b9c31-108">Parameter</span></span>|<span data-ttu-id="b9c31-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b9c31-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b9c31-110">*object*</span><span class="sxs-lookup"><span data-stu-id="b9c31-110">*object*</span></span> |<span data-ttu-id="b9c31-111">Объект **поля** или **параметра** .</span><span class="sxs-lookup"><span data-stu-id="b9c31-111">A **Field** or **Parameter** object.</span></span>|
|<span data-ttu-id="b9c31-112">*Данные*</span><span class="sxs-lookup"><span data-stu-id="b9c31-112">*Data*</span></span> |<span data-ttu-id="b9c31-113">**Variant** , который содержит данные для добавления к объекту.</span><span class="sxs-lookup"><span data-stu-id="b9c31-113">A **Variant** that contains the data to append to the object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b9c31-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b9c31-114">Remarks</span></span>

<span data-ttu-id="b9c31-115">Используйте метод **AppendChunk** для **поля** или **параметра** объекта для наполнения данными длинный двоичные или знак.</span><span class="sxs-lookup"><span data-stu-id="b9c31-115">Use the **AppendChunk** method on a **Field** or **Parameter** object to fill it with long binary or character data.</span></span> <span data-ttu-id="b9c31-116">В случаях, когда системной памяти ограниченный можно использовать метод **AppendChunk** для работы с длинные значения в части, а не полностью.</span><span class="sxs-lookup"><span data-stu-id="b9c31-116">In situations where system memory is limited, you can use the **AppendChunk** method to manipulate long values in portions rather than in their entirety.</span></span>

### <a name="field"></a><span data-ttu-id="b9c31-117">Поле</span><span class="sxs-lookup"><span data-stu-id="b9c31-117">Field</span></span>

<span data-ttu-id="b9c31-118">Если бит **adFldLong** в свойство [Attributes](attributes-property-ado.md) объекта **поля** задано значение true, можно использовать метод **AppendChunk** для этого поля.</span><span class="sxs-lookup"><span data-stu-id="b9c31-118">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to true, you can use the **AppendChunk** method for that field.</span></span>

<span data-ttu-id="b9c31-119">Первый вызов **AppendChunk** для объекта **поля** записывает данные в поле перезапись существующих данных.</span><span class="sxs-lookup"><span data-stu-id="b9c31-119">The first **AppendChunk** call on a **Field** object writes data to the field, overwriting any existing data.</span></span> <span data-ttu-id="b9c31-120">Последующие вызовы **AppendChunk** добавьте существующих данных.</span><span class="sxs-lookup"><span data-stu-id="b9c31-120">Subsequent **AppendChunk** calls add to existing data.</span></span> <span data-ttu-id="b9c31-121">При добавлении данных в одном поле, а затем задайте или читать значение другого поля в текущей записи, ADO предполагается, что окончании добавления данных до первого поля.</span><span class="sxs-lookup"><span data-stu-id="b9c31-121">If you are appending data to one field and then you set or read the value of another field in the current record, ADO assumes that you are finished appending data to the first field.</span></span> <span data-ttu-id="b9c31-122">При вызове метода **AppendChunk** в первом поле еще раз, ADO интерпретирует звонок как операции создания **AppendChunk** и перезапись существующих данных.</span><span class="sxs-lookup"><span data-stu-id="b9c31-122">If you call the **AppendChunk** method on the first field again, ADO interprets the call as a new **AppendChunk** operation and overwrites the existing data.</span></span> <span data-ttu-id="b9c31-123">Доступ к полей в другие объекты [набора записей](recordset-object-ado.md) , которые не копирует первый объект **набора записей** не нарушить **AppendChunk** операций.</span><span class="sxs-lookup"><span data-stu-id="b9c31-123">Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **AppendChunk** operations.</span></span>

<span data-ttu-id="b9c31-124">Если отсутствует текущий запись при вызове **AppendChunk** объекта **поля** , возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="b9c31-124">If there is no current record when you call **AppendChunk** on a **Field** object, an error occurs.</span></span>

> [!NOTE]
> <span data-ttu-id="b9c31-125">Метод **AppendChunk** не работают с объектами **поля** объект [записи](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b9c31-125">The **AppendChunk** method does not operate on **Field** objects of a [Record](record-object-ado.md) object.</span></span> <span data-ttu-id="b9c31-126">Он не выполнять любые операции и приведет к ошибке времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="b9c31-126">It does not perform any operation and will produce a run-time error.</span></span>

### <a name="parameters"></a><span data-ttu-id="b9c31-127">Parameters</span><span class="sxs-lookup"><span data-stu-id="b9c31-127">Parameters</span></span>

<span data-ttu-id="b9c31-128">Если бит **adParamLong** в свойстве **атрибуты** объекта **параметр** имеет значение true, можно использовать метод **AppendChunk** для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="b9c31-128">If the **adParamLong** bit in the **Attributes** property of a **Parameter** object is set to true, you can use the **AppendChunk** method for that parameter.</span></span>

<span data-ttu-id="b9c31-129">Первый вызов **AppendChunk** на объект **параметра** записывает данные параметр перезаписи существующих данных.</span><span class="sxs-lookup"><span data-stu-id="b9c31-129">The first **AppendChunk** call on a **Parameter** object writes data to the parameter, overwriting any existing data.</span></span> <span data-ttu-id="b9c31-130">Последующие вызовы **AppendChunk** объект **параметра** добавьте существующих параметров данных.</span><span class="sxs-lookup"><span data-stu-id="b9c31-130">Subsequent **AppendChunk** calls on a **Parameter** object add to existing parameter data.</span></span> <span data-ttu-id="b9c31-131">**AppendChunk** вызов, который передает значение null удаляет все данные параметра.</span><span class="sxs-lookup"><span data-stu-id="b9c31-131">An **AppendChunk** call that passes a null value discards all of the parameter data.</span></span>


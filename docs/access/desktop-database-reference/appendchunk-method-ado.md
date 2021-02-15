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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297027"
---
# <a name="appendchunk-method-ado"></a><span data-ttu-id="1ba67-102">Метод AppendChunk (ADO)</span><span class="sxs-lookup"><span data-stu-id="1ba67-102">AppendChunk method (ADO)</span></span>

<span data-ttu-id="1ba67-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ba67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ba67-104">Appends data to a large text or binary data [Field](field-object-ado.md), or to a [Parameter](parameter-object-ado.md) object.</span><span class="sxs-lookup"><span data-stu-id="1ba67-104">Appends data to a large text or binary data [Field](field-object-ado.md), or to a [Parameter](parameter-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ba67-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ba67-105">Syntax</span></span>

<span data-ttu-id="1ba67-106">*object.* Данные AppendChunk </span><span class="sxs-lookup"><span data-stu-id="1ba67-106">*object.* AppendChunk *Data*</span></span>

## <a name="parameters"></a><span data-ttu-id="1ba67-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ba67-107">Parameters</span></span>

|<span data-ttu-id="1ba67-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="1ba67-108">Parameter</span></span>|<span data-ttu-id="1ba67-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1ba67-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1ba67-110">*object*</span><span class="sxs-lookup"><span data-stu-id="1ba67-110">*object*</span></span> |<span data-ttu-id="1ba67-111">Объект **Field** или **Parameter.**</span><span class="sxs-lookup"><span data-stu-id="1ba67-111">A **Field** or **Parameter** object.</span></span>|
|<span data-ttu-id="1ba67-112">*Data*</span><span class="sxs-lookup"><span data-stu-id="1ba67-112">*Data*</span></span> |<span data-ttu-id="1ba67-113">**Вариант,** содержащий данные, которые необходимо примедить к объекту.</span><span class="sxs-lookup"><span data-stu-id="1ba67-113">A **Variant** that contains the data to append to the object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1ba67-114">Заметки</span><span class="sxs-lookup"><span data-stu-id="1ba67-114">Remarks</span></span>

<span data-ttu-id="1ba67-115">Используйте метод **AppendChunk** для объекта **Field** или **Parameter,** чтобы заполнить его длинными двоичными или символьными данными.</span><span class="sxs-lookup"><span data-stu-id="1ba67-115">Use the **AppendChunk** method on a **Field** or **Parameter** object to fill it with long binary or character data.</span></span> <span data-ttu-id="1ba67-116">В ситуациях, когда системная память ограничена, можно использовать метод **AppendChunk** для управления длинными значениями по частям, а не полностью.</span><span class="sxs-lookup"><span data-stu-id="1ba67-116">In situations where system memory is limited, you can use the **AppendChunk** method to manipulate long values in portions rather than in their entirety.</span></span>

### <a name="field"></a><span data-ttu-id="1ba67-117">Поле</span><span class="sxs-lookup"><span data-stu-id="1ba67-117">Field</span></span>

<span data-ttu-id="1ba67-118">Если бит **adFldLong** в свойстве [Attributes](attributes-property-ado.md) объекта **Field** имеет true, можно использовать метод **AppendChunk** для этого поля.</span><span class="sxs-lookup"><span data-stu-id="1ba67-118">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to true, you can use the **AppendChunk** method for that field.</span></span>

<span data-ttu-id="1ba67-119">Первый вызов **AppendChunk** для объекта **Field** записывает данные в поле, переописав все существующие данные.</span><span class="sxs-lookup"><span data-stu-id="1ba67-119">The first **AppendChunk** call on a **Field** object writes data to the field, overwriting any existing data.</span></span> <span data-ttu-id="1ba67-120">Последующие **вызовы AppendChunk** добавляются в существующие данные.</span><span class="sxs-lookup"><span data-stu-id="1ba67-120">Subsequent **AppendChunk** calls add to existing data.</span></span> <span data-ttu-id="1ba67-121">Если вы при добавлении данных в одно поле и затем установили или считыали значение другого поля в текущей записи, ADO предполагает, что вы завершили добавление данных в первое поле.</span><span class="sxs-lookup"><span data-stu-id="1ba67-121">If you are appending data to one field and then you set or read the value of another field in the current record, ADO assumes that you are finished appending data to the first field.</span></span> <span data-ttu-id="1ba67-122">При повторном вызове метода **AppendChunk** в первом поле ADO интерпретирует вызов как новую операцию **AppendChunk** и переоценит существующие данные.</span><span class="sxs-lookup"><span data-stu-id="1ba67-122">If you call the **AppendChunk** method on the first field again, ADO interprets the call as a new **AppendChunk** operation and overwrites the existing data.</span></span> <span data-ttu-id="1ba67-123">Доступ к полям в других [объектах Recordset,](recordset-object-ado.md) которые не являются клонами первого объекта **Recordset,** не нарушит операции **AppendChunk.**</span><span class="sxs-lookup"><span data-stu-id="1ba67-123">Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **AppendChunk** operations.</span></span>

<span data-ttu-id="1ba67-124">Если при вызове **AppendChunk** для объекта **Field** нет текущей записи, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="1ba67-124">If there is no current record when you call **AppendChunk** on a **Field** object, an error occurs.</span></span>

> [!NOTE]
> <span data-ttu-id="1ba67-125">Метод **AppendChunk** не работает с **объектами Field** объекта [Record.](record-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="1ba67-125">The **AppendChunk** method does not operate on **Field** objects of a [Record](record-object-ado.md) object.</span></span> <span data-ttu-id="1ba67-126">Он не выполняет никаких операций и создает ошибку во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="1ba67-126">It does not perform any operation and will produce a run-time error.</span></span>

### <a name="parameters"></a><span data-ttu-id="1ba67-127">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ba67-127">Parameters</span></span>

<span data-ttu-id="1ba67-128">Если бит **adParamLong** в свойстве **Attributes** объекта **Parameter** имеет true, для этого параметра можно использовать метод **AppendChunk.**</span><span class="sxs-lookup"><span data-stu-id="1ba67-128">If the **adParamLong** bit in the **Attributes** property of a **Parameter** object is set to true, you can use the **AppendChunk** method for that parameter.</span></span>

<span data-ttu-id="1ba67-129">Первый вызов **AppendChunk** для объекта **Parameter** записывает данные в параметр, переописав все существующие данные.</span><span class="sxs-lookup"><span data-stu-id="1ba67-129">The first **AppendChunk** call on a **Parameter** object writes data to the parameter, overwriting any existing data.</span></span> <span data-ttu-id="1ba67-130">Последующие **вызовы AppendChunk** для объекта **Parameter** добавляются к существующим данным параметра.</span><span class="sxs-lookup"><span data-stu-id="1ba67-130">Subsequent **AppendChunk** calls on a **Parameter** object add to existing parameter data.</span></span> <span data-ttu-id="1ba67-131">Вызов **AppendChunk,** который передает значение null, удаляет все данные параметра.</span><span class="sxs-lookup"><span data-stu-id="1ba67-131">An **AppendChunk** call that passes a null value discards all of the parameter data.</span></span>


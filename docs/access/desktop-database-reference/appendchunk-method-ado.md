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
# <a name="appendchunk-method-ado"></a><span data-ttu-id="a59ef-102">Метод AppendChunk (ADO)</span><span class="sxs-lookup"><span data-stu-id="a59ef-102">AppendChunk method (ADO)</span></span>

<span data-ttu-id="a59ef-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a59ef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a59ef-104">Добавляет данные в [поле](field-object-ado.md)большого текста или двоичных данных или в объект [Parameter](parameter-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a59ef-104">Appends data to a large text or binary data [Field](field-object-ado.md), or to a [Parameter](parameter-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a59ef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a59ef-105">Syntax</span></span>

<span data-ttu-id="a59ef-106">*объект.* *Данные* AppendChunk</span><span class="sxs-lookup"><span data-stu-id="a59ef-106">*object.* AppendChunk *Data*</span></span>

## <a name="parameters"></a><span data-ttu-id="a59ef-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a59ef-107">Parameters</span></span>

|<span data-ttu-id="a59ef-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="a59ef-108">Parameter</span></span>|<span data-ttu-id="a59ef-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a59ef-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a59ef-110">*object*</span><span class="sxs-lookup"><span data-stu-id="a59ef-110">*object*</span></span> |<span data-ttu-id="a59ef-111">Объект **field** или **Parameter** .</span><span class="sxs-lookup"><span data-stu-id="a59ef-111">A **Field** or **Parameter** object.</span></span>|
|<span data-ttu-id="a59ef-112">*Data*</span><span class="sxs-lookup"><span data-stu-id="a59ef-112">*Data*</span></span> |<span data-ttu-id="a59ef-113">**Переменная типа Variant** , содержащая данные, которые необходимо добавить в объект.</span><span class="sxs-lookup"><span data-stu-id="a59ef-113">A **Variant** that contains the data to append to the object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a59ef-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a59ef-114">Remarks</span></span>

<span data-ttu-id="a59ef-115">Используйте метод **AppendChunk** для **поля** или объекта **Parameter** , чтобы заполнить его длинными двоичными или символьными данными.</span><span class="sxs-lookup"><span data-stu-id="a59ef-115">Use the **AppendChunk** method on a **Field** or **Parameter** object to fill it with long binary or character data.</span></span> <span data-ttu-id="a59ef-116">В ситуациях, когда ограничена системная память, можно использовать метод **AppendChunk** для управления длинными значениями в частях, а не целиком.</span><span class="sxs-lookup"><span data-stu-id="a59ef-116">In situations where system memory is limited, you can use the **AppendChunk** method to manipulate long values in portions rather than in their entirety.</span></span>

### <a name="field"></a><span data-ttu-id="a59ef-117">Поле</span><span class="sxs-lookup"><span data-stu-id="a59ef-117">Field</span></span>

<span data-ttu-id="a59ef-118">Если для бита **адфлдлонг** в свойстве [Attribute](attributes-property-ado.md) объекта **field** задано значение true, можно использовать метод **AppendChunk** для этого поля.</span><span class="sxs-lookup"><span data-stu-id="a59ef-118">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to true, you can use the **AppendChunk** method for that field.</span></span>

<span data-ttu-id="a59ef-119">Первый вызов **AppendChunk** для объекта **field** записывает данные в поле, перезаписывая существующие данные.</span><span class="sxs-lookup"><span data-stu-id="a59ef-119">The first **AppendChunk** call on a **Field** object writes data to the field, overwriting any existing data.</span></span> <span data-ttu-id="a59ef-120">Последующие вызовы **AppendChunk** добавляются к существующим данным.</span><span class="sxs-lookup"><span data-stu-id="a59ef-120">Subsequent **AppendChunk** calls add to existing data.</span></span> <span data-ttu-id="a59ef-121">Если вы добавляете данные в одно поле, а затем задаете или просматриваете значение другого поля в текущей записи, ADO считает, что вы завершили добавление данных в первое поле.</span><span class="sxs-lookup"><span data-stu-id="a59ef-121">If you are appending data to one field and then you set or read the value of another field in the current record, ADO assumes that you are finished appending data to the first field.</span></span> <span data-ttu-id="a59ef-122">Если вызвать метод **AppendChunk** для первого поля еще раз, ADO интерпретирует вызов как новую операцию **AppendChunk** и перезаписывает существующие данные.</span><span class="sxs-lookup"><span data-stu-id="a59ef-122">If you call the **AppendChunk** method on the first field again, ADO interprets the call as a new **AppendChunk** operation and overwrites the existing data.</span></span> <span data-ttu-id="a59ef-123">Доступ к полям в других объектах [Recordset](recordset-object-ado.md) , которые не являются клонами первого объекта **Recordset** , не приводит к нарушению операций **AppendChunk** .</span><span class="sxs-lookup"><span data-stu-id="a59ef-123">Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **AppendChunk** operations.</span></span>

<span data-ttu-id="a59ef-124">Если при вызове **AppendChunk** для объекта **field** отсутствует текущая запись, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="a59ef-124">If there is no current record when you call **AppendChunk** on a **Field** object, an error occurs.</span></span>

> [!NOTE]
> <span data-ttu-id="a59ef-125">Метод **AppendChunk** не работает с объектами **field** объекта [Record](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a59ef-125">The **AppendChunk** method does not operate on **Field** objects of a [Record](record-object-ado.md) object.</span></span> <span data-ttu-id="a59ef-126">Она не выполняет никаких операций и создает ошибку во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="a59ef-126">It does not perform any operation and will produce a run-time error.</span></span>

### <a name="parameters"></a><span data-ttu-id="a59ef-127">Параметры</span><span class="sxs-lookup"><span data-stu-id="a59ef-127">Parameters</span></span>

<span data-ttu-id="a59ef-128">Если бит **адпарамлонг** в свойстве **Attributes** объекта **Parameter** имеет значение true, можно использовать метод **AppendChunk** для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="a59ef-128">If the **adParamLong** bit in the **Attributes** property of a **Parameter** object is set to true, you can use the **AppendChunk** method for that parameter.</span></span>

<span data-ttu-id="a59ef-129">Первый вызов **AppendChunk** для объекта **Parameter** записывает данные в параметр, перезаписывая существующие данные.</span><span class="sxs-lookup"><span data-stu-id="a59ef-129">The first **AppendChunk** call on a **Parameter** object writes data to the parameter, overwriting any existing data.</span></span> <span data-ttu-id="a59ef-130">Последующие вызовы **AppendChunk** для объекта **Parameter** добавляют существующие данные параметров.</span><span class="sxs-lookup"><span data-stu-id="a59ef-130">Subsequent **AppendChunk** calls on a **Parameter** object add to existing parameter data.</span></span> <span data-ttu-id="a59ef-131">Вызов **AppendChunk** , который передает значение null, отклоняет все данные параметра.</span><span class="sxs-lookup"><span data-stu-id="a59ef-131">An **AppendChunk** call that passes a null value discards all of the parameter data.</span></span>


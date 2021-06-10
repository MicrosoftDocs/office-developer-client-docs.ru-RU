---
title: Метод CreateParameter (ADO)
TOCTitle: CreateParameter method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fa060811f60379e720e06be9f94e9403477c7869
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295396"
---
# <a name="createparameter-method-ado"></a><span data-ttu-id="771c3-102">Метод CreateParameter (ADO)</span><span class="sxs-lookup"><span data-stu-id="771c3-102">CreateParameter method (ADO)</span></span>

<span data-ttu-id="771c3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="771c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="771c3-104">Создает новый объект [Parameter](parameter-object-ado.md) с указанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="771c3-104">Creates a new [Parameter](parameter-object-ado.md) object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="771c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="771c3-105">Syntax</span></span>

<span data-ttu-id="771c3-106">**Задана**   =  *команда параметров*. CreateParameter *(Имя,* *Тип,* *Направление,* *Размер*, *Значение*)</span><span class="sxs-lookup"><span data-stu-id="771c3-106">**Set** *parameter* = *command*.CreateParameter (*Name*, *Type*, *Direction*, *Size*, *Value*)</span></span>

## <a name="return-value"></a><span data-ttu-id="771c3-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="771c3-107">Return value</span></span>

<span data-ttu-id="771c3-108">Возвращает объект **Parameter.**</span><span class="sxs-lookup"><span data-stu-id="771c3-108">Returns a **Parameter** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="771c3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="771c3-109">Parameters</span></span>

|<span data-ttu-id="771c3-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="771c3-110">Parameter</span></span>|<span data-ttu-id="771c3-111">Описание</span><span class="sxs-lookup"><span data-stu-id="771c3-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="771c3-112">*Name*</span><span class="sxs-lookup"><span data-stu-id="771c3-112">*Name*</span></span> |<span data-ttu-id="771c3-113">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="771c3-113">Optional.</span></span> <span data-ttu-id="771c3-114">Значение **String,** содержаное имя объекта **Параметр.**</span><span class="sxs-lookup"><span data-stu-id="771c3-114">A **String** value that contains the name of the **Parameter** object.</span></span>|
|<span data-ttu-id="771c3-115">*Тип*</span><span class="sxs-lookup"><span data-stu-id="771c3-115">*Type*</span></span> |<span data-ttu-id="771c3-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="771c3-116">Optional.</span></span> <span data-ttu-id="771c3-117">Значение [DataTypeEnum,](datatypeenum.md) которое указывает тип данных объекта **Parameter.**</span><span class="sxs-lookup"><span data-stu-id="771c3-117">A [DataTypeEnum](datatypeenum.md) value that specifies the data type of the **Parameter** object.</span></span>|
|<span data-ttu-id="771c3-118">*Направление*</span><span class="sxs-lookup"><span data-stu-id="771c3-118">*Direction*</span></span> |<span data-ttu-id="771c3-119">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="771c3-119">Optional.</span></span> <span data-ttu-id="771c3-120">Значение [ParameterDirectionEnum,](parameterdirectionenum.md) которое указывает тип **объекта Parameter.**</span><span class="sxs-lookup"><span data-stu-id="771c3-120">A [ParameterDirectionEnum](parameterdirectionenum.md) value that specifies the type of **Parameter** object.</span></span>|
|<span data-ttu-id="771c3-121">*Размер*</span><span class="sxs-lookup"><span data-stu-id="771c3-121">*Size*</span></span> |<span data-ttu-id="771c3-122">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="771c3-122">Optional.</span></span> <span data-ttu-id="771c3-123">**Длинное** значение, которое указывает максимальную длину значения параметра в символах или bytes.</span><span class="sxs-lookup"><span data-stu-id="771c3-123">A **Long** value that specifies the maximum length for the parameter value in characters or bytes.</span></span>|
|<span data-ttu-id="771c3-124">*Значение*</span><span class="sxs-lookup"><span data-stu-id="771c3-124">*Value*</span></span> |<span data-ttu-id="771c3-125">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="771c3-125">Optional.</span></span> <span data-ttu-id="771c3-126">**Вариант,** который указывает значение объекта **Параметр.**</span><span class="sxs-lookup"><span data-stu-id="771c3-126">A **Variant** that specifies the value for the **Parameter** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="771c3-127">Примечания</span><span class="sxs-lookup"><span data-stu-id="771c3-127">Remarks</span></span>

<span data-ttu-id="771c3-128">Используйте метод **CreateParameter** для создания нового объекта **Parameter** с заданным именем, типом, направлением, размером и значением.</span><span class="sxs-lookup"><span data-stu-id="771c3-128">Use the **CreateParameter** method to create a new **Parameter** object with a specified name, type, direction, size, and value.</span></span> <span data-ttu-id="771c3-129">Любые значения, которые вы передаете в аргументах, записаны в соответствующие свойства **параметра.**</span><span class="sxs-lookup"><span data-stu-id="771c3-129">Any values you pass in the arguments are written to the corresponding **Parameter** properties.</span></span>

<span data-ttu-id="771c3-130">Этот метод автоматически не привносим объект **Parameter** в коллекцию **Параметры** объекта [Command.](command-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="771c3-130">This method does not automatically append the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object.</span></span> <span data-ttu-id="771c3-131">Это позволяет задать дополнительные свойства, значения которых ADO будет проверять при добавлении объекта **Parameter** в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="771c3-131">This lets you set additional properties whose values ADO will validate when you append the **Parameter** object to the collection.</span></span>

<span data-ttu-id="771c3-132">Если в аргументе Type указывается  тип данных переменной длины, необходимо либо передать аргумент *Size,* либо задать свойство [Size](size-property-ado.md) объекта **Parameter** перед его примесями к коллекции **Параметры;** в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="771c3-132">If you specify a variable-length data type in the *Type* argument, you must either pass a *Size* argument or set the [Size](size-property-ado.md) property of the **Parameter** object before appending it to the **Parameters** collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="771c3-133">Если в аргументе *Type* указывается числовой тип данных **(adNumeric** или **adDecimal),** необходимо также задать свойства [NumericScale](numericscale-property-ado.md) и [Precision.](precision-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="771c3-133">If you specify a numeric data type (**adNumeric** or **adDecimal**) in the *Type* argument, then you must also set the [NumericScale](numericscale-property-ado.md) and [Precision](precision-property-ado.md) properties.</span></span>


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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700684"
---
# <a name="createparameter-method-ado"></a><span data-ttu-id="2fbc0-102">Метод CreateParameter (ADO)</span><span class="sxs-lookup"><span data-stu-id="2fbc0-102">CreateParameter method (ADO)</span></span>

<span data-ttu-id="2fbc0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2fbc0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2fbc0-104">Создает новый объект [параметр](parameter-object-ado.md) с указанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="2fbc0-104">Creates a new [Parameter](parameter-object-ado.md) object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fbc0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2fbc0-105">Syntax</span></span>

<span data-ttu-id="2fbc0-106">**Установка** *параметр*  =  *команды*. CreateParameter (*имя*, *Тип*, *направление*, *размер*, *значение*)</span><span class="sxs-lookup"><span data-stu-id="2fbc0-106">**Set** *parameter* = *command*.CreateParameter (*Name*, *Type*, *Direction*, *Size*, *Value*)</span></span>

## <a name="return-value"></a><span data-ttu-id="2fbc0-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2fbc0-107">Return value</span></span>

<span data-ttu-id="2fbc0-108">Возвращает объект **параметра** .</span><span class="sxs-lookup"><span data-stu-id="2fbc0-108">Returns a **Parameter** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="2fbc0-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="2fbc0-109">Parameters</span></span>

|<span data-ttu-id="2fbc0-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="2fbc0-110">Parameter</span></span>|<span data-ttu-id="2fbc0-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2fbc0-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2fbc0-112">*Name*</span><span class="sxs-lookup"><span data-stu-id="2fbc0-112">*Name*</span></span> |<span data-ttu-id="2fbc0-113">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="2fbc0-113">Optional.</span></span> <span data-ttu-id="2fbc0-114">**Строковое** значение, содержащее имя объекта **параметра** .</span><span class="sxs-lookup"><span data-stu-id="2fbc0-114">A **String** value that contains the name of the **Parameter** object.</span></span>|
|<span data-ttu-id="2fbc0-115">*Type*</span><span class="sxs-lookup"><span data-stu-id="2fbc0-115">*Type*</span></span> |<span data-ttu-id="2fbc0-116">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="2fbc0-116">Optional.</span></span> <span data-ttu-id="2fbc0-117">[DataTypeEnum](datatypeenum.md) значение, задающее тип данных **параметра** объекта.</span><span class="sxs-lookup"><span data-stu-id="2fbc0-117">A [DataTypeEnum](datatypeenum.md) value that specifies the data type of the **Parameter** object.</span></span>|
|<span data-ttu-id="2fbc0-118">*Direction*</span><span class="sxs-lookup"><span data-stu-id="2fbc0-118">*Direction*</span></span> |<span data-ttu-id="2fbc0-119">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="2fbc0-119">Optional.</span></span> <span data-ttu-id="2fbc0-120">[ParameterDirectionEnum](parameterdirectionenum.md) значение, задающее тип объекта **параметра** .</span><span class="sxs-lookup"><span data-stu-id="2fbc0-120">A [ParameterDirectionEnum](parameterdirectionenum.md) value that specifies the type of **Parameter** object.</span></span>|
|<span data-ttu-id="2fbc0-121">*Size*</span><span class="sxs-lookup"><span data-stu-id="2fbc0-121">*Size*</span></span> |<span data-ttu-id="2fbc0-122">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="2fbc0-122">Optional.</span></span> <span data-ttu-id="2fbc0-123">Значение типа **Long** , определяет максимальную длину значения параметра в символы или в байтах.</span><span class="sxs-lookup"><span data-stu-id="2fbc0-123">A **Long** value that specifies the maximum length for the parameter value in characters or bytes.</span></span>|
|<span data-ttu-id="2fbc0-124">*Value*</span><span class="sxs-lookup"><span data-stu-id="2fbc0-124">*Value*</span></span> |<span data-ttu-id="2fbc0-125">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="2fbc0-125">Optional.</span></span> <span data-ttu-id="2fbc0-126">**Variant** , который задает значение для **параметра** объекта.</span><span class="sxs-lookup"><span data-stu-id="2fbc0-126">A **Variant** that specifies the value for the **Parameter** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="2fbc0-127">Замечания</span><span class="sxs-lookup"><span data-stu-id="2fbc0-127">Remarks</span></span>

<span data-ttu-id="2fbc0-128">Используйте метод **CreateParameter** для создания нового объекта **параметра** с указанным именем, типом, направление, размер и значение.</span><span class="sxs-lookup"><span data-stu-id="2fbc0-128">Use the **CreateParameter** method to create a new **Parameter** object with a specified name, type, direction, size, and value.</span></span> <span data-ttu-id="2fbc0-129">Все значения, передаваемого в аргументах записываются в соответствующие свойства **параметра** .</span><span class="sxs-lookup"><span data-stu-id="2fbc0-129">Any values you pass in the arguments are written to the corresponding **Parameter** properties.</span></span>

<span data-ttu-id="2fbc0-130">Этот метод не добавляет автоматически объект **параметра** в коллекцию **параметров** объекта [Command](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="2fbc0-130">This method does not automatically append the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object.</span></span> <span data-ttu-id="2fbc0-131">Это позволяет задавать дополнительные свойства, чьи значения ADO будет проверять при добавьте объект **параметра** в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="2fbc0-131">This lets you set additional properties whose values ADO will validate when you append the **Parameter** object to the collection.</span></span>

<span data-ttu-id="2fbc0-132">Если указан тип данных переменной длины в аргументе *типа* , необходимо передать аргумент *размер* или задать свойство [размер](size-property-ado.md) объекта **параметра** перед добавлением в коллекцию **параметров** ; в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="2fbc0-132">If you specify a variable-length data type in the *Type* argument, you must either pass a *Size* argument or set the [Size](size-property-ado.md) property of the **Parameter** object before appending it to the **Parameters** collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="2fbc0-133">При указании числовым типом данных (**adNumeric** или **adDecimal**) в качестве аргумента *типа* , необходимо также установить свойства [NumericScale](numericscale-property-ado.md) и [точность](precision-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="2fbc0-133">If you specify a numeric data type (**adNumeric** or **adDecimal**) in the *Type* argument, then you must also set the [NumericScale](numericscale-property-ado.md) and [Precision](precision-property-ado.md) properties.</span></span>


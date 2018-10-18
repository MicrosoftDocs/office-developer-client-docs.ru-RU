---
title: CreateParameter Method (ADO)
TOCTitle: CreateParameter Method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 00a2c5e2eb8613434b80c80e2a51cbf5d1deb644
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605487"
---
# <a name="createparameter-method-ado"></a><span data-ttu-id="b9d51-102">CreateParameter Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="b9d51-102">CreateParameter Method (ADO)</span></span>


<span data-ttu-id="b9d51-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b9d51-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="b9d51-104">Создает новый объект [параметр](parameter-object-ado.md) с указанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="b9d51-104">Creates a new [Parameter](parameter-object-ado.md) object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9d51-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b9d51-105">Syntax</span></span>

<span data-ttu-id="b9d51-106">**Установка** *параметр*  =  *команды*. CreateParameter (*имя*, *Тип*, *направление*, *размер*, *значение*)</span><span class="sxs-lookup"><span data-stu-id="b9d51-106">**Set** *parameter* = *command*.CreateParameter (*Name*, *Type*, *Direction*, *Size*, *Value*)</span></span>

<span data-ttu-id="b9d51-107"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="b9d51-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="b9d51-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9d51-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="b9d51-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b9d51-109">Return value</span></span>
>>>>>>> <span data-ttu-id="b9d51-110">master</span><span class="sxs-lookup"><span data-stu-id="b9d51-110">master</span></span>

<span data-ttu-id="b9d51-111">Возвращает объект **параметра** .</span><span class="sxs-lookup"><span data-stu-id="b9d51-111">Returns a **Parameter** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b9d51-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9d51-112">Parameters</span></span>

  - <span data-ttu-id="b9d51-113">*Имя*</span><span class="sxs-lookup"><span data-stu-id="b9d51-113">*Name*</span></span>

  - <span data-ttu-id="b9d51-114">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="b9d51-114">Optional.</span></span> <span data-ttu-id="b9d51-115">**Строковое** значение, содержащее имя объекта **параметра** .</span><span class="sxs-lookup"><span data-stu-id="b9d51-115">A **String** value that contains the name of the **Parameter** object.</span></span>

  - <span data-ttu-id="b9d51-116">*Тип*</span><span class="sxs-lookup"><span data-stu-id="b9d51-116">*Type*</span></span>

  - <span data-ttu-id="b9d51-117">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="b9d51-117">Optional.</span></span> <span data-ttu-id="b9d51-118">[DataTypeEnum](datatypeenum.md) значение, задающее тип данных **параметра** объекта.</span><span class="sxs-lookup"><span data-stu-id="b9d51-118">A [DataTypeEnum](datatypeenum.md) value that specifies the data type of the **Parameter** object.</span></span>

  - <span data-ttu-id="b9d51-119">*Direction*</span><span class="sxs-lookup"><span data-stu-id="b9d51-119">*Direction*</span></span>

  - <span data-ttu-id="b9d51-120">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="b9d51-120">Optional.</span></span> <span data-ttu-id="b9d51-121">[ParameterDirectionEnum](parameterdirectionenum.md) значение, задающее тип объекта **параметра** .</span><span class="sxs-lookup"><span data-stu-id="b9d51-121">A [ParameterDirectionEnum](parameterdirectionenum.md) value that specifies the type of **Parameter** object.</span></span>

  - <span data-ttu-id="b9d51-122">*Размер*</span><span class="sxs-lookup"><span data-stu-id="b9d51-122">*Size*</span></span>

  - <span data-ttu-id="b9d51-123">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="b9d51-123">Optional.</span></span> <span data-ttu-id="b9d51-124">Значение типа **Long** , определяет максимальную длину значения параметра в символы или в байтах.</span><span class="sxs-lookup"><span data-stu-id="b9d51-124">A **Long** value that specifies the maximum length for the parameter value in characters or bytes.</span></span>

  - <span data-ttu-id="b9d51-125">*Значение*</span><span class="sxs-lookup"><span data-stu-id="b9d51-125">*Value*</span></span>

  - <span data-ttu-id="b9d51-126">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="b9d51-126">Optional.</span></span> <span data-ttu-id="b9d51-127">**Variant** , который задает значение для **параметра** объекта.</span><span class="sxs-lookup"><span data-stu-id="b9d51-127">A **Variant** that specifies the value for the **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9d51-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="b9d51-128">Remarks</span></span>

<span data-ttu-id="b9d51-129">Используйте метод **CreateParameter** для создания нового объекта **параметра** с указанным именем, типом, направление, размер и значение.</span><span class="sxs-lookup"><span data-stu-id="b9d51-129">Use the **CreateParameter** method to create a new **Parameter** object with a specified name, type, direction, size, and value.</span></span> <span data-ttu-id="b9d51-130">Все значения, передаваемого в аргументах записываются в соответствующие свойства **параметра** .</span><span class="sxs-lookup"><span data-stu-id="b9d51-130">Any values you pass in the arguments are written to the corresponding **Parameter** properties.</span></span>

<span data-ttu-id="b9d51-131">Этот метод не добавляет автоматически объект **параметра** в коллекцию **параметров** объекта [Command](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b9d51-131">This method does not automatically append the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object.</span></span> <span data-ttu-id="b9d51-132">Это позволяет задавать дополнительные свойства, чьи значения ADO будет проверять при добавьте объект **параметра** в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="b9d51-132">This lets you set additional properties whose values ADO will validate when you append the **Parameter** object to the collection.</span></span>

<span data-ttu-id="b9d51-133">Если указан тип данных переменной длины в аргументе *типа* , необходимо передать аргумент *размер* или задать свойство [размер](size-property-ado.md) объекта **параметра** перед добавлением в коллекцию **параметров** ; в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="b9d51-133">If you specify a variable-length data type in the *Type* argument, you must either pass a *Size* argument or set the [Size](size-property-ado.md) property of the **Parameter** object before appending it to the **Parameters** collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="b9d51-134">При указании числовым типом данных (**adNumeric** или **adDecimal**) в качестве аргумента *типа* , необходимо также установить свойства [NumericScale](numericscale-property-ado.md) и [точность](precision-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b9d51-134">If you specify a numeric data type (**adNumeric** or **adDecimal**) in the *Type* argument, then you must also set the [NumericScale](numericscale-property-ado.md) and [Precision](precision-property-ado.md) properties.</span></span>


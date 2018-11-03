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
ms.openlocfilehash: 88a5d62cc94aa707c2e90467d74dc07d80a0af02
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928945"
---
# <a name="createparameter-method-ado"></a><span data-ttu-id="bac3a-102">Метод CreateParameter (ADO)</span><span class="sxs-lookup"><span data-stu-id="bac3a-102">CreateParameter method (ADO)</span></span>


<span data-ttu-id="bac3a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bac3a-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="bac3a-104">Создает новый объект [параметр](parameter-object-ado.md) с указанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="bac3a-104">Creates a new [Parameter](parameter-object-ado.md) object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bac3a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bac3a-105">Syntax</span></span>

<span data-ttu-id="bac3a-106">**Установка** *параметр*  =  *команды*. CreateParameter (*имя*, *Тип*, *направление*, *размер*, *значение*)</span><span class="sxs-lookup"><span data-stu-id="bac3a-106">**Set** *parameter* = *command*.CreateParameter (*Name*, *Type*, *Direction*, *Size*, *Value*)</span></span>

## <a name="return-value"></a><span data-ttu-id="bac3a-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bac3a-107">Return value</span></span>

<span data-ttu-id="bac3a-108">Возвращает объект **параметра** .</span><span class="sxs-lookup"><span data-stu-id="bac3a-108">Returns a **Parameter** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="bac3a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bac3a-109">Parameters</span></span>

  - <span data-ttu-id="bac3a-110">*Имя*</span><span class="sxs-lookup"><span data-stu-id="bac3a-110">*Name*</span></span>

  - <span data-ttu-id="bac3a-111">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="bac3a-111">Optional.</span></span> <span data-ttu-id="bac3a-112">**Строковое** значение, содержащее имя объекта **параметра** .</span><span class="sxs-lookup"><span data-stu-id="bac3a-112">A **String** value that contains the name of the **Parameter** object.</span></span>

  - <span data-ttu-id="bac3a-113">*Тип*</span><span class="sxs-lookup"><span data-stu-id="bac3a-113">*Type*</span></span>

  - <span data-ttu-id="bac3a-114">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="bac3a-114">Optional.</span></span> <span data-ttu-id="bac3a-115">[DataTypeEnum](datatypeenum.md) значение, задающее тип данных **параметра** объекта.</span><span class="sxs-lookup"><span data-stu-id="bac3a-115">A [DataTypeEnum](datatypeenum.md) value that specifies the data type of the **Parameter** object.</span></span>

  - <span data-ttu-id="bac3a-116">*Direction*</span><span class="sxs-lookup"><span data-stu-id="bac3a-116">*Direction*</span></span>

  - <span data-ttu-id="bac3a-117">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="bac3a-117">Optional.</span></span> <span data-ttu-id="bac3a-118">[ParameterDirectionEnum](parameterdirectionenum.md) значение, задающее тип объекта **параметра** .</span><span class="sxs-lookup"><span data-stu-id="bac3a-118">A [ParameterDirectionEnum](parameterdirectionenum.md) value that specifies the type of **Parameter** object.</span></span>

  - <span data-ttu-id="bac3a-119">*Размер*</span><span class="sxs-lookup"><span data-stu-id="bac3a-119">*Size*</span></span>

  - <span data-ttu-id="bac3a-120">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="bac3a-120">Optional.</span></span> <span data-ttu-id="bac3a-121">Значение типа **Long** , определяет максимальную длину значения параметра в символы или в байтах.</span><span class="sxs-lookup"><span data-stu-id="bac3a-121">A **Long** value that specifies the maximum length for the parameter value in characters or bytes.</span></span>

  - <span data-ttu-id="bac3a-122">*Значение*</span><span class="sxs-lookup"><span data-stu-id="bac3a-122">*Value*</span></span>

  - <span data-ttu-id="bac3a-123">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="bac3a-123">Optional.</span></span> <span data-ttu-id="bac3a-124">**Variant** , который задает значение для **параметра** объекта.</span><span class="sxs-lookup"><span data-stu-id="bac3a-124">A **Variant** that specifies the value for the **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bac3a-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="bac3a-125">Remarks</span></span>

<span data-ttu-id="bac3a-126">Используйте метод **CreateParameter** для создания нового объекта **параметра** с указанным именем, типом, направление, размер и значение.</span><span class="sxs-lookup"><span data-stu-id="bac3a-126">Use the **CreateParameter** method to create a new **Parameter** object with a specified name, type, direction, size, and value.</span></span> <span data-ttu-id="bac3a-127">Все значения, передаваемого в аргументах записываются в соответствующие свойства **параметра** .</span><span class="sxs-lookup"><span data-stu-id="bac3a-127">Any values you pass in the arguments are written to the corresponding **Parameter** properties.</span></span>

<span data-ttu-id="bac3a-128">Этот метод не добавляет автоматически объект **параметра** в коллекцию **параметров** объекта [Command](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bac3a-128">This method does not automatically append the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object.</span></span> <span data-ttu-id="bac3a-129">Это позволяет задавать дополнительные свойства, чьи значения ADO будет проверять при добавьте объект **параметра** в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="bac3a-129">This lets you set additional properties whose values ADO will validate when you append the **Parameter** object to the collection.</span></span>

<span data-ttu-id="bac3a-130">Если указан тип данных переменной длины в аргументе *типа* , необходимо передать аргумент *размер* или задать свойство [размер](size-property-ado.md) объекта **параметра** перед добавлением в коллекцию **параметров** ; в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="bac3a-130">If you specify a variable-length data type in the *Type* argument, you must either pass a *Size* argument or set the [Size](size-property-ado.md) property of the **Parameter** object before appending it to the **Parameters** collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="bac3a-131">При указании числовым типом данных (**adNumeric** или **adDecimal**) в качестве аргумента *типа* , необходимо также установить свойства [NumericScale](numericscale-property-ado.md) и [точность](precision-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bac3a-131">If you specify a numeric data type (**adNumeric** or **adDecimal**) in the *Type* argument, then you must also set the [NumericScale](numericscale-property-ado.md) and [Precision](precision-property-ado.md) properties.</span></span>


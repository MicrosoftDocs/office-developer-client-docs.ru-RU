---
title: Методического блока данных (ADO)
TOCTitle: GetChunk method (ADO)
ms:assetid: 1ef1c37a-8453-8d3b-251a-d16e0d519fd7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248979(v=office.15)
ms:contentKeyID: 48543629
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 44cd0cb5632e64811de14f9abd3c78aac9203705
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292288"
---
# <a name="getchunk-method-ado"></a><span data-ttu-id="d9e0d-102">Методического блока данных (ADO)</span><span class="sxs-lookup"><span data-stu-id="d9e0d-102">GetChunk method (ADO)</span></span>

<span data-ttu-id="d9e0d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9e0d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d9e0d-104">Возвращает всю часть содержимого большого текстового или двоичного [поля](field-object-ado.md) данных или ее часть.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-104">Returns all, or a portion, of the contents of a large text or binary data [Field](field-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9e0d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9e0d-105">Syntax</span></span>

<span data-ttu-id="d9e0d-106">\*\* = *поле*переменной. ПереФрагмент (*size* )</span><span class="sxs-lookup"><span data-stu-id="d9e0d-106">*variable* = *field*.GetChunk(*Size* )</span></span>

## <a name="return-value"></a><span data-ttu-id="d9e0d-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9e0d-107">Return value</span></span>

<span data-ttu-id="d9e0d-108">Возвращает **значение типа Variant**.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-108">Returns a **Variant**.</span></span>

## <a name="parameters"></a><span data-ttu-id="d9e0d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9e0d-109">Parameters</span></span>

|<span data-ttu-id="d9e0d-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="d9e0d-110">Parameter</span></span>|<span data-ttu-id="d9e0d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="d9e0d-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d9e0d-112">*Размер*</span><span class="sxs-lookup"><span data-stu-id="d9e0d-112">*Size*</span></span> |<span data-ttu-id="d9e0d-113">**Длинное** выражение, равное количеству байтов или символов, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-113">A **Long** expression that is equal to the number of bytes or characters that you want to retrieve.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d9e0d-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="d9e0d-114">Remarks</span></span>

<span data-ttu-id="d9e0d-115">Используйте метод \*\*\*\* GetObject для объекта **field** , чтобы извлечь часть или все его длинные двоичные или символьные данные.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-115">Use the **GetChunk** method on a **Field** object to retrieve part or all of its long binary or character data.</span></span> <span data-ttu-id="d9e0d-116">В ситуациях, когда ограничена системная память, можно использовать метод методомического **блока** для управления длинными значениями в частях, а не целиком.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-116">In situations where system memory is limited, you can use the **GetChunk** method to manipulate long values in portions, rather than in their entirety.</span></span>

<span data-ttu-id="d9e0d-117">Данные, возвращаемые вызовом функции- **блока** , назначаются *переменной*.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-117">The data that a **GetChunk** call returns is assigned to *variable*.</span></span> <span data-ttu-id="d9e0d-118">Если *Размер* больше остальных данных, метод IsEmpty возвращает только \*\*\*\* оставшиеся данные без *переменной* заполнения с пустыми пробелами.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-118">If *Size* is greater than the remaining data, the **GetChunk** method returns only the remaining data without padding *variable* with empty spaces.</span></span> <span data-ttu-id="d9e0d-119">Если поле не заполнено, метод **блока** данных возвращает значение null.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-119">If the field is empty, the **GetChunk** method returns a null value.</span></span>

<span data-ttu-id="d9e0d-120">Каждый последующий вызов метода возвращает данные, начиная с того места, где предыдущий вызов **блока** . \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d9e0d-120">Each subsequent **GetChunk** call retrieves data starting from where the previous **GetChunk** call left off.</span></span> <span data-ttu-id="d9e0d-121">Тем не менее, если вы получаете данные из одного поля, а затем задаете или просматриваете значение другого поля в текущей записи, то в ADO предполагается, что вы завершили извлечение данных из первого поля.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-121">However, if you are retrieving data from one field and then you set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field.</span></span> <span data-ttu-id="d9e0d-122">При повторном вызове метода переФрагмента для первого поля, ADO интерпретирует вызов как новую операцию, а \*\*\*\* затем начинает чтение с начала данных. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d9e0d-122">If you call the **GetChunk** method on the first field again, ADO interprets the call as a new **GetChunk** operation and starts reading from the beginning of the data.</span></span> <span data-ttu-id="d9e0d-123">Доступ к полям в других объектах [Recordset](recordset-object-ado.md) , которые не являются клонами первого объекта **Recordset** , не приводит к нарушению операций с **блоком** .</span><span class="sxs-lookup"><span data-stu-id="d9e0d-123">Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **GetChunk** operations.</span></span>

<span data-ttu-id="d9e0d-124">Если для бита **адфлдлонг** в свойстве [Attribute](attributes-property-ado.md) объекта **field** задано **значение true**, можно использовать метод GetObject для этого \*\*\*\* поля.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-124">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to **True**, you can use the **GetChunk** method for that field.</span></span>

<span data-ttu-id="d9e0d-125">Если не существует текущей записи при использовании метода GetObject для \*\*\*\* объекта **field** , возникает ошибка 3021 (нет текущей записи).</span><span class="sxs-lookup"><span data-stu-id="d9e0d-125">If there is no current record when you use the **GetChunk** method on a **Field** object, error 3021 (no current record) occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="d9e0d-126">Метод \*\*\*\* GetObject не работает с объектами **field** объекта [Record](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e0d-126">The **GetChunk** method does not operate on **Field** objects of a [Record](record-object-ado.md) object.</span></span> <span data-ttu-id="d9e0d-127">Она не выполняет никаких операций и создает ошибку во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="d9e0d-127">It does not perform any operation and will produce a run-time error.</span></span>



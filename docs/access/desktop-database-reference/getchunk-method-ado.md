---
title: Метод GetChunk (ADO)
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
# <a name="getchunk-method-ado"></a><span data-ttu-id="675cb-102">Метод GetChunk (ADO)</span><span class="sxs-lookup"><span data-stu-id="675cb-102">GetChunk method (ADO)</span></span>

<span data-ttu-id="675cb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="675cb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="675cb-104">Возвращает все или часть содержимого большого объекта поля текстовых или двоичных [данных.](field-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="675cb-104">Returns all, or a portion, of the contents of a large text or binary data [Field](field-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="675cb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="675cb-105">Syntax</span></span>

<span data-ttu-id="675cb-106">*переменная*  =  *поле*. GetChunk *(Размер)*</span><span class="sxs-lookup"><span data-stu-id="675cb-106">*variable* = *field*.GetChunk(*Size* )</span></span>

## <a name="return-value"></a><span data-ttu-id="675cb-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="675cb-107">Return value</span></span>

<span data-ttu-id="675cb-108">Возвращает **вариант**.</span><span class="sxs-lookup"><span data-stu-id="675cb-108">Returns a **Variant**.</span></span>

## <a name="parameters"></a><span data-ttu-id="675cb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="675cb-109">Parameters</span></span>

|<span data-ttu-id="675cb-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="675cb-110">Parameter</span></span>|<span data-ttu-id="675cb-111">Описание</span><span class="sxs-lookup"><span data-stu-id="675cb-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="675cb-112">*Размер*</span><span class="sxs-lookup"><span data-stu-id="675cb-112">*Size*</span></span> |<span data-ttu-id="675cb-113">**Длинное** выражение, равное количеству bytes или символов, которые вы хотите получить.</span><span class="sxs-lookup"><span data-stu-id="675cb-113">A **Long** expression that is equal to the number of bytes or characters that you want to retrieve.</span></span>|

## <a name="remarks"></a><span data-ttu-id="675cb-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="675cb-114">Remarks</span></span>

<span data-ttu-id="675cb-115">Используйте метод **GetChunk** на **объекте Field,** чтобы получить часть или все его длинные двоичные или данные символов.</span><span class="sxs-lookup"><span data-stu-id="675cb-115">Use the **GetChunk** method on a **Field** object to retrieve part or all of its long binary or character data.</span></span> <span data-ttu-id="675cb-116">В ситуациях, когда память системы ограничена, можно использовать метод **GetChunk** для обработки длинных значений частями, а не целиком.</span><span class="sxs-lookup"><span data-stu-id="675cb-116">In situations where system memory is limited, you can use the **GetChunk** method to manipulate long values in portions, rather than in their entirety.</span></span>

<span data-ttu-id="675cb-117">Данные, **возвращаемые вызовом GetChunk,** назначены *переменной.*</span><span class="sxs-lookup"><span data-stu-id="675cb-117">The data that a **GetChunk** call returns is assigned to *variable*.</span></span> <span data-ttu-id="675cb-118">Если *размер* больше остальных данных, метод **GetChunk** возвращает только оставшиеся данные без переменной заполнения *пустыми* пробелами.</span><span class="sxs-lookup"><span data-stu-id="675cb-118">If *Size* is greater than the remaining data, the **GetChunk** method returns only the remaining data without padding *variable* with empty spaces.</span></span> <span data-ttu-id="675cb-119">Если поле пусто, метод **GetChunk** возвращает значение null.</span><span class="sxs-lookup"><span data-stu-id="675cb-119">If the field is empty, the **GetChunk** method returns a null value.</span></span>

<span data-ttu-id="675cb-120">Каждый **последующий вызов GetChunk** извлекает данные, начиная с того места, где был отключен предыдущий вызов **GetChunk.**</span><span class="sxs-lookup"><span data-stu-id="675cb-120">Each subsequent **GetChunk** call retrieves data starting from where the previous **GetChunk** call left off.</span></span> <span data-ttu-id="675cb-121">Однако при сборе данных из одного поля, а затем задайте или считывайте значение другого поля в текущей записи, ADO предполагает, что вы закончили сбор данных из первого поля.</span><span class="sxs-lookup"><span data-stu-id="675cb-121">However, if you are retrieving data from one field and then you set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field.</span></span> <span data-ttu-id="675cb-122">Если снова вызвать метод **GetChunk** в первом поле, ADO интерпретирует вызов как новую операцию **GetChunk** и начинает чтение с самого начала данных.</span><span class="sxs-lookup"><span data-stu-id="675cb-122">If you call the **GetChunk** method on the first field again, ADO interprets the call as a new **GetChunk** operation and starts reading from the beginning of the data.</span></span> <span data-ttu-id="675cb-123">Доступ к полям в других [объектах Recordset,](recordset-object-ado.md) которые не являются клонами первого объекта **Recordset,** не будет нарушать **операции GetChunk.**</span><span class="sxs-lookup"><span data-stu-id="675cb-123">Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **GetChunk** operations.</span></span>

<span data-ttu-id="675cb-124">Если бит **adFldLong** в свойстве [Атрибуты](attributes-property-ado.md) объекта **Field** настроен на **True,** для этого поля можно использовать метод **GetChunk.**</span><span class="sxs-lookup"><span data-stu-id="675cb-124">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to **True**, you can use the **GetChunk** method for that field.</span></span>

<span data-ttu-id="675cb-125">Если нет текущей записи при использовании метода **GetChunk** на объекте **Field,** возникает ошибка 3021 (текущая запись не существует).</span><span class="sxs-lookup"><span data-stu-id="675cb-125">If there is no current record when you use the **GetChunk** method on a **Field** object, error 3021 (no current record) occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="675cb-126">Метод **GetChunk** не работает на **объектах Field** объекта [Record.](record-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="675cb-126">The **GetChunk** method does not operate on **Field** objects of a [Record](record-object-ado.md) object.</span></span> <span data-ttu-id="675cb-127">Он не выполняет никаких операций и создает ошибку во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="675cb-127">It does not perform any operation and will produce a run-time error.</span></span>



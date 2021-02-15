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
# <a name="getchunk-method-ado"></a><span data-ttu-id="a4852-102">Метод GetChunk (ADO)</span><span class="sxs-lookup"><span data-stu-id="a4852-102">GetChunk method (ADO)</span></span>

<span data-ttu-id="a4852-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a4852-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a4852-104">Возвращает все (или часть) содержимое большого текста или двоичного объекта [field.](field-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="a4852-104">Returns all, or a portion, of the contents of a large text or binary data [Field](field-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4852-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4852-105">Syntax</span></span>

<span data-ttu-id="a4852-106">*переменная*  =  *field*. GetChunk(*Size* )</span><span class="sxs-lookup"><span data-stu-id="a4852-106">*variable* = *field*.GetChunk(*Size* )</span></span>

## <a name="return-value"></a><span data-ttu-id="a4852-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4852-107">Return value</span></span>

<span data-ttu-id="a4852-108">Возвращает **вариант**.</span><span class="sxs-lookup"><span data-stu-id="a4852-108">Returns a **Variant**.</span></span>

## <a name="parameters"></a><span data-ttu-id="a4852-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4852-109">Parameters</span></span>

|<span data-ttu-id="a4852-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="a4852-110">Parameter</span></span>|<span data-ttu-id="a4852-111">Описание</span><span class="sxs-lookup"><span data-stu-id="a4852-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a4852-112">*Размер*</span><span class="sxs-lookup"><span data-stu-id="a4852-112">*Size*</span></span> |<span data-ttu-id="a4852-113">**Длинное** выражение, равное количеству извлекаемого количества символов или символов.</span><span class="sxs-lookup"><span data-stu-id="a4852-113">A **Long** expression that is equal to the number of bytes or characters that you want to retrieve.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a4852-114">Заметки</span><span class="sxs-lookup"><span data-stu-id="a4852-114">Remarks</span></span>

<span data-ttu-id="a4852-115">Используйте метод **GetChunk** для объекта **Field,** чтобы получить часть или все длинные двоичные или символьные данные.</span><span class="sxs-lookup"><span data-stu-id="a4852-115">Use the **GetChunk** method on a **Field** object to retrieve part or all of its long binary or character data.</span></span> <span data-ttu-id="a4852-116">В ситуациях, когда системная память ограничена, можно использовать метод **GetChunk** для управления длинными значениями по частям, а не полностью.</span><span class="sxs-lookup"><span data-stu-id="a4852-116">In situations where system memory is limited, you can use the **GetChunk** method to manipulate long values in portions, rather than in their entirety.</span></span>

<span data-ttu-id="a4852-117">Данные, возвращаемые вызовом **GetChunk,** назначены *переменной.*</span><span class="sxs-lookup"><span data-stu-id="a4852-117">The data that a **GetChunk** call returns is assigned to *variable*.</span></span> <span data-ttu-id="a4852-118">Если *размер* больше остальных данных, метод **GetChunk** возвращает только оставшиеся данные без переменной заполнения *с* пустыми пробелами.</span><span class="sxs-lookup"><span data-stu-id="a4852-118">If *Size* is greater than the remaining data, the **GetChunk** method returns only the remaining data without padding *variable* with empty spaces.</span></span> <span data-ttu-id="a4852-119">Если поле пустое, метод **GetChunk** возвращает значение null.</span><span class="sxs-lookup"><span data-stu-id="a4852-119">If the field is empty, the **GetChunk** method returns a null value.</span></span>

<span data-ttu-id="a4852-120">Каждый **последующий вызов GetChunk** извлекает данные, начиная с того места, где был отключен предыдущий вызов **GetChunk.**</span><span class="sxs-lookup"><span data-stu-id="a4852-120">Each subsequent **GetChunk** call retrieves data starting from where the previous **GetChunk** call left off.</span></span> <span data-ttu-id="a4852-121">Однако если вы искомые данные из одного поля, а затем задайте или считайте значение другого поля в текущей записи, ADO предполагает, что вы завершили искомые данные из первого поля.</span><span class="sxs-lookup"><span data-stu-id="a4852-121">However, if you are retrieving data from one field and then you set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field.</span></span> <span data-ttu-id="a4852-122">При повторном вызове метода **GetChunk** в первом поле ADO интерпретирует вызов как новую операцию **GetChunk** и начинает чтение с начала данных.</span><span class="sxs-lookup"><span data-stu-id="a4852-122">If you call the **GetChunk** method on the first field again, ADO interprets the call as a new **GetChunk** operation and starts reading from the beginning of the data.</span></span> <span data-ttu-id="a4852-123">Доступ к полям в других [объектах Recordset,](recordset-object-ado.md) которые не являются клонами первого объекта **Recordset,** не нарушит операции **GetChunk.**</span><span class="sxs-lookup"><span data-stu-id="a4852-123">Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **GetChunk** operations.</span></span>

<span data-ttu-id="a4852-124">Если бит **adFldLong** в свойстве [Attributes](attributes-property-ado.md) объекта **Field** имеет свойство **True,** можно использовать метод **GetChunk** для этого поля.</span><span class="sxs-lookup"><span data-stu-id="a4852-124">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to **True**, you can use the **GetChunk** method for that field.</span></span>

<span data-ttu-id="a4852-125">Если при использовании метода **GetChunk** для объекта **Field** нет текущей записи, возникает ошибка 3021 (текущая запись не возникает).</span><span class="sxs-lookup"><span data-stu-id="a4852-125">If there is no current record when you use the **GetChunk** method on a **Field** object, error 3021 (no current record) occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="a4852-126">Метод **GetChunk** не работает с **объектами Field** объекта [Record.](record-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="a4852-126">The **GetChunk** method does not operate on **Field** objects of a [Record](record-object-ado.md) object.</span></span> <span data-ttu-id="a4852-127">Он не выполняет никаких операций и создает ошибку во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="a4852-127">It does not perform any operation and will produce a run-time error.</span></span>



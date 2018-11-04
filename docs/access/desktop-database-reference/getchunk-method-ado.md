---
title: Метод GetChunk (ADO)
TOCTitle: GetChunk method (ADO)
ms:assetid: 1ef1c37a-8453-8d3b-251a-d16e0d519fd7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248979(v=office.15)
ms:contentKeyID: 48543629
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 27d6f2c9884441042d67615072738c7762f4f789
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949917"
---
# <a name="getchunk-method-ado"></a><span data-ttu-id="adfb7-102">Метод GetChunk (ADO)</span><span class="sxs-lookup"><span data-stu-id="adfb7-102">GetChunk method (ADO)</span></span>

<span data-ttu-id="adfb7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="adfb7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="adfb7-104">Возвращает все или часть содержимого большого текстового или объекта [поля](field-object-ado.md) двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="adfb7-104">Returns all, or a portion, of the contents of a large text or binary data [Field](field-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="adfb7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="adfb7-105">Syntax</span></span>

<span data-ttu-id="adfb7-106">*переменная* = *поля*. Методы GetChunk (*размер* )</span><span class="sxs-lookup"><span data-stu-id="adfb7-106">*variable* = *field*.GetChunk(*Size* )</span></span>

## <a name="return-value"></a><span data-ttu-id="adfb7-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="adfb7-107">Return value</span></span>

<span data-ttu-id="adfb7-108">Возвращает значение **типа Variant**.</span><span class="sxs-lookup"><span data-stu-id="adfb7-108">Returns a **Variant**.</span></span>

## <a name="parameters"></a><span data-ttu-id="adfb7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="adfb7-109">Parameters</span></span>

|<span data-ttu-id="adfb7-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="adfb7-110">Parameter</span></span>|<span data-ttu-id="adfb7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="adfb7-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="adfb7-112">*Размер*</span><span class="sxs-lookup"><span data-stu-id="adfb7-112">*Size*</span></span> |<span data-ttu-id="adfb7-113">**Длинные** выражения, равный число байтов или символов, которые необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="adfb7-113">A **Long** expression that is equal to the number of bytes or characters that you want to retrieve.</span></span>|

## <a name="remarks"></a><span data-ttu-id="adfb7-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="adfb7-114">Remarks</span></span>

<span data-ttu-id="adfb7-115">Используйте метод **GetChunk** для объекта **поля** для извлечения или часть ее длинные двоичный или данных символов.</span><span class="sxs-lookup"><span data-stu-id="adfb7-115">Use the **GetChunk** method on a **Field** object to retrieve part or all of its long binary or character data.</span></span> <span data-ttu-id="adfb7-116">В случаях, когда системной памяти ограниченный можно использовать метод **GetChunk** для работы с длинные значения в частях, а не полностью.</span><span class="sxs-lookup"><span data-stu-id="adfb7-116">In situations where system memory is limited, you can use the **GetChunk** method to manipulate long values in portions, rather than in their entirety.</span></span>

<span data-ttu-id="adfb7-117">Данные, вызов **GetChunk** возвращает назначается *переменной*.</span><span class="sxs-lookup"><span data-stu-id="adfb7-117">The data that a **GetChunk** call returns is assigned to *variable*.</span></span> <span data-ttu-id="adfb7-118">Если *размер* больше, чем остальные данные, метод **GetChunk** возвращает только оставшихся данных без заполнения *переменной* пробелами.</span><span class="sxs-lookup"><span data-stu-id="adfb7-118">If *Size* is greater than the remaining data, the **GetChunk** method returns only the remaining data without padding *variable* with empty spaces.</span></span> <span data-ttu-id="adfb7-119">Если поле не заполнено, метод **GetChunk** возвращает значение null.</span><span class="sxs-lookup"><span data-stu-id="adfb7-119">If the field is empty, the **GetChunk** method returns a null value.</span></span>

<span data-ttu-id="adfb7-120">Каждый последующий вызов **GetChunk** возвращает данные, начиная с предыдущего звонка **GetChunk** же места.</span><span class="sxs-lookup"><span data-stu-id="adfb7-120">Each subsequent **GetChunk** call retrieves data starting from where the previous **GetChunk** call left off.</span></span> <span data-ttu-id="adfb7-121">Тем не менее если необходимо извлечь данные из одного поля, а затем можно устанавливать или читать значение другого поля в текущей записи, ADO предполагается, что завершения извлечения данных из первого поля.</span><span class="sxs-lookup"><span data-stu-id="adfb7-121">However, if you are retrieving data from one field and then you set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field.</span></span> <span data-ttu-id="adfb7-122">При вызове метода **GetChunk** в первом поле еще раз, ADO интерпретирует звонок как операции создания **GetChunk** и запускает чтения с самого начала данных.</span><span class="sxs-lookup"><span data-stu-id="adfb7-122">If you call the **GetChunk** method on the first field again, ADO interprets the call as a new **GetChunk** operation and starts reading from the beginning of the data.</span></span> <span data-ttu-id="adfb7-123">Доступ к полей в другие объекты [набора записей](recordset-object-ado.md) , которые не копирует первый объект **набора записей** не нарушить **GetChunk** операций.</span><span class="sxs-lookup"><span data-stu-id="adfb7-123">Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **GetChunk** operations.</span></span>

<span data-ttu-id="adfb7-124">Если бит **adFldLong** в свойство [Attributes](attributes-property-ado.md) объекта **поля** задано значение **True**, можно использовать метод **GetChunk** для этого поля.</span><span class="sxs-lookup"><span data-stu-id="adfb7-124">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to **True**, you can use the **GetChunk** method for that field.</span></span>

<span data-ttu-id="adfb7-125">Если при использовании метода **GetChunk** для объекта **поля** нет текущей записи, возникает ошибка 3021 (текущая запись).</span><span class="sxs-lookup"><span data-stu-id="adfb7-125">If there is no current record when you use the **GetChunk** method on a **Field** object, error 3021 (no current record) occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="adfb7-126">Метод **GetChunk** не работают с объектами **поля** объект [записи](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="adfb7-126">The **GetChunk** method does not operate on **Field** objects of a [Record](record-object-ado.md) object.</span></span> <span data-ttu-id="adfb7-127">Он не выполнять любые операции и приведет к ошибке времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="adfb7-127">It does not perform any operation and will produce a run-time error.</span></span>



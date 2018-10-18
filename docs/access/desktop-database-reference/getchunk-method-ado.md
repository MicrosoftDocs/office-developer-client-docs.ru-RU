---
title: GetChunk Method (ADO)
TOCTitle: GetChunk Method (ADO)
ms:assetid: 1ef1c37a-8453-8d3b-251a-d16e0d519fd7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248979(v=office.15)
ms:contentKeyID: 48543629
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ae3cc867c00930c71d379e8ce5bb139075d229d8
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602505"
---
# <a name="getchunk-method-ado"></a><span data-ttu-id="2f747-102">GetChunk Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="2f747-102">GetChunk Method (ADO)</span></span>


<span data-ttu-id="2f747-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f747-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="2f747-104">Возвращает все или часть содержимого большого текстового или объекта [поля](field-object-ado.md) двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="2f747-104">Returns all, or a portion, of the contents of a large text or binary data [Field](field-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f747-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f747-105">Syntax</span></span>

<span data-ttu-id="2f747-106">*переменная* = *поля*. Методы GetChunk (*размер* )</span><span class="sxs-lookup"><span data-stu-id="2f747-106">*variable* = *field*.GetChunk(*Size* )</span></span>

<span data-ttu-id="2f747-107"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="2f747-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="2f747-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f747-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="2f747-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f747-109">Return value</span></span>
>>>>>>> <span data-ttu-id="2f747-110">master</span><span class="sxs-lookup"><span data-stu-id="2f747-110">master</span></span>

<span data-ttu-id="2f747-111">Возвращает значение **типа Variant**.</span><span class="sxs-lookup"><span data-stu-id="2f747-111">Returns a **Variant**.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f747-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f747-112">Parameters</span></span>

  - <span data-ttu-id="2f747-113">*Размер*</span><span class="sxs-lookup"><span data-stu-id="2f747-113">*Size*</span></span>

  - <span data-ttu-id="2f747-114">**Длинные** выражения, равный число байтов или символов, которые необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="2f747-114">A **Long** expression that is equal to the number of bytes or characters that you want to retrieve.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f747-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="2f747-115">Remarks</span></span>

<span data-ttu-id="2f747-116">Используйте метод **GetChunk** для объекта **поля** для извлечения или часть ее длинные двоичный или данных символов.</span><span class="sxs-lookup"><span data-stu-id="2f747-116">Use the **GetChunk** method on a **Field** object to retrieve part or all of its long binary or character data.</span></span> <span data-ttu-id="2f747-117">В случаях, когда системной памяти ограниченный можно использовать метод **GetChunk** для работы с длинные значения в частях, а не полностью.</span><span class="sxs-lookup"><span data-stu-id="2f747-117">In situations where system memory is limited, you can use the **GetChunk** method to manipulate long values in portions, rather than in their entirety.</span></span>

<span data-ttu-id="2f747-118">Данные, вызов **GetChunk** возвращает назначается *переменной*.</span><span class="sxs-lookup"><span data-stu-id="2f747-118">The data that a **GetChunk** call returns is assigned to *variable*.</span></span> <span data-ttu-id="2f747-119">Если *размер* больше, чем остальные данные, метод **GetChunk** возвращает только оставшихся данных без заполнения *переменной* пробелами.</span><span class="sxs-lookup"><span data-stu-id="2f747-119">If *Size* is greater than the remaining data, the **GetChunk** method returns only the remaining data without padding *variable* with empty spaces.</span></span> <span data-ttu-id="2f747-120">Если поле не заполнено, метод **GetChunk** возвращает значение null.</span><span class="sxs-lookup"><span data-stu-id="2f747-120">If the field is empty, the **GetChunk** method returns a null value.</span></span>

<span data-ttu-id="2f747-121">Каждый последующий вызов **GetChunk** возвращает данные, начиная с предыдущего звонка **GetChunk** же места.</span><span class="sxs-lookup"><span data-stu-id="2f747-121">Each subsequent **GetChunk** call retrieves data starting from where the previous **GetChunk** call left off.</span></span> <span data-ttu-id="2f747-122">Тем не менее если необходимо извлечь данные из одного поля, а затем можно устанавливать или читать значение другого поля в текущей записи, ADO предполагается, что завершения извлечения данных из первого поля.</span><span class="sxs-lookup"><span data-stu-id="2f747-122">However, if you are retrieving data from one field and then you set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field.</span></span> <span data-ttu-id="2f747-123">При вызове метода **GetChunk** в первом поле еще раз, ADO интерпретирует звонок как операции создания **GetChunk** и запускает чтения с самого начала данных.</span><span class="sxs-lookup"><span data-stu-id="2f747-123">If you call the **GetChunk** method on the first field again, ADO interprets the call as a new **GetChunk** operation and starts reading from the beginning of the data.</span></span> <span data-ttu-id="2f747-124">Доступ к полей в другие объекты [набора записей](recordset-object-ado.md) , которые не копирует первый объект **набора записей** не нарушить **GetChunk** операций.</span><span class="sxs-lookup"><span data-stu-id="2f747-124">Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **GetChunk** operations.</span></span>

<span data-ttu-id="2f747-125">Если бит **adFldLong** в свойство [Attributes](attributes-property-ado.md) объекта **поля** задано значение **True**, можно использовать метод **GetChunk** для этого поля.</span><span class="sxs-lookup"><span data-stu-id="2f747-125">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to **True**, you can use the **GetChunk** method for that field.</span></span>

<span data-ttu-id="2f747-126">Если при использовании метода **GetChunk** для объекта **поля** нет текущей записи, возникает ошибка 3021 (текущая запись).</span><span class="sxs-lookup"><span data-stu-id="2f747-126">If there is no current record when you use the **GetChunk** method on a **Field** object, error 3021 (no current record) occurs.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2f747-127">Метод <STRONG>GetChunk</STRONG> не работают с объектами <STRONG>поля</STRONG> объект <A href="record-object-ado.md">записи</A> .</span><span class="sxs-lookup"><span data-stu-id="2f747-127">The <STRONG>GetChunk</STRONG> method does not operate on <STRONG>Field</STRONG> objects of a <A href="record-object-ado.md">Record</A> object.</span></span> <span data-ttu-id="2f747-128">Он не выполнять любые операции и приведет к ошибке времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="2f747-128">It does not perform any operation and will produce a run-time error.</span></span></P>



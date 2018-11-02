---
title: Метод GetChunk (ADO)
TOCTitle: GetChunk method (ADO)
ms:assetid: 1ef1c37a-8453-8d3b-251a-d16e0d519fd7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248979(v=office.15)
ms:contentKeyID: 48543629
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a61130db9bd4564523688adc4e045f665e7310e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919012"
---
# <a name="getchunk-method-ado"></a><span data-ttu-id="df7cd-102">Метод GetChunk (ADO)</span><span class="sxs-lookup"><span data-stu-id="df7cd-102">GetChunk method (ADO)</span></span>


<span data-ttu-id="df7cd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="df7cd-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="df7cd-104">Возвращает все или часть содержимого большого текстового или объекта [поля](field-object-ado.md) двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="df7cd-104">Returns all, or a portion, of the contents of a large text or binary data [Field](field-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="df7cd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df7cd-105">Syntax</span></span>

<span data-ttu-id="df7cd-106">*переменная* = *поля*. Методы GetChunk (*размер* )</span><span class="sxs-lookup"><span data-stu-id="df7cd-106">*variable* = *field*.GetChunk(*Size* )</span></span>

## <a name="return-value"></a><span data-ttu-id="df7cd-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df7cd-107">Return value</span></span>

<span data-ttu-id="df7cd-108">Возвращает значение **типа Variant**.</span><span class="sxs-lookup"><span data-stu-id="df7cd-108">Returns a **Variant**.</span></span>

## <a name="parameters"></a><span data-ttu-id="df7cd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="df7cd-109">Parameters</span></span>

  - <span data-ttu-id="df7cd-110">*Размер*</span><span class="sxs-lookup"><span data-stu-id="df7cd-110">*Size*</span></span>

  - <span data-ttu-id="df7cd-111">**Длинные** выражения, равный число байтов или символов, которые необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="df7cd-111">A **Long** expression that is equal to the number of bytes or characters that you want to retrieve.</span></span>

## <a name="remarks"></a><span data-ttu-id="df7cd-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="df7cd-112">Remarks</span></span>

<span data-ttu-id="df7cd-113">Используйте метод **GetChunk** для объекта **поля** для извлечения или часть ее длинные двоичный или данных символов.</span><span class="sxs-lookup"><span data-stu-id="df7cd-113">Use the **GetChunk** method on a **Field** object to retrieve part or all of its long binary or character data.</span></span> <span data-ttu-id="df7cd-114">В случаях, когда системной памяти ограниченный можно использовать метод **GetChunk** для работы с длинные значения в частях, а не полностью.</span><span class="sxs-lookup"><span data-stu-id="df7cd-114">In situations where system memory is limited, you can use the **GetChunk** method to manipulate long values in portions, rather than in their entirety.</span></span>

<span data-ttu-id="df7cd-115">Данные, вызов **GetChunk** возвращает назначается *переменной*.</span><span class="sxs-lookup"><span data-stu-id="df7cd-115">The data that a **GetChunk** call returns is assigned to *variable*.</span></span> <span data-ttu-id="df7cd-116">Если *размер* больше, чем остальные данные, метод **GetChunk** возвращает только оставшихся данных без заполнения *переменной* пробелами.</span><span class="sxs-lookup"><span data-stu-id="df7cd-116">If *Size* is greater than the remaining data, the **GetChunk** method returns only the remaining data without padding *variable* with empty spaces.</span></span> <span data-ttu-id="df7cd-117">Если поле не заполнено, метод **GetChunk** возвращает значение null.</span><span class="sxs-lookup"><span data-stu-id="df7cd-117">If the field is empty, the **GetChunk** method returns a null value.</span></span>

<span data-ttu-id="df7cd-118">Каждый последующий вызов **GetChunk** возвращает данные, начиная с предыдущего звонка **GetChunk** же места.</span><span class="sxs-lookup"><span data-stu-id="df7cd-118">Each subsequent **GetChunk** call retrieves data starting from where the previous **GetChunk** call left off.</span></span> <span data-ttu-id="df7cd-119">Тем не менее если необходимо извлечь данные из одного поля, а затем можно устанавливать или читать значение другого поля в текущей записи, ADO предполагается, что завершения извлечения данных из первого поля.</span><span class="sxs-lookup"><span data-stu-id="df7cd-119">However, if you are retrieving data from one field and then you set or read the value of another field in the current record, ADO assumes you have finished retrieving data from the first field.</span></span> <span data-ttu-id="df7cd-120">При вызове метода **GetChunk** в первом поле еще раз, ADO интерпретирует звонок как операции создания **GetChunk** и запускает чтения с самого начала данных.</span><span class="sxs-lookup"><span data-stu-id="df7cd-120">If you call the **GetChunk** method on the first field again, ADO interprets the call as a new **GetChunk** operation and starts reading from the beginning of the data.</span></span> <span data-ttu-id="df7cd-121">Доступ к полей в другие объекты [набора записей](recordset-object-ado.md) , которые не копирует первый объект **набора записей** не нарушить **GetChunk** операций.</span><span class="sxs-lookup"><span data-stu-id="df7cd-121">Accessing fields in other [Recordset](recordset-object-ado.md) objects that are not clones of the first **Recordset** object will not disrupt **GetChunk** operations.</span></span>

<span data-ttu-id="df7cd-122">Если бит **adFldLong** в свойство [Attributes](attributes-property-ado.md) объекта **поля** задано значение **True**, можно использовать метод **GetChunk** для этого поля.</span><span class="sxs-lookup"><span data-stu-id="df7cd-122">If the **adFldLong** bit in the [Attributes](attributes-property-ado.md) property of a **Field** object is set to **True**, you can use the **GetChunk** method for that field.</span></span>

<span data-ttu-id="df7cd-123">Если при использовании метода **GetChunk** для объекта **поля** нет текущей записи, возникает ошибка 3021 (текущая запись).</span><span class="sxs-lookup"><span data-stu-id="df7cd-123">If there is no current record when you use the **GetChunk** method on a **Field** object, error 3021 (no current record) occurs.</span></span>


> [!NOTE]
> <P><span data-ttu-id="df7cd-124">Метод <STRONG>GetChunk</STRONG> не работают с объектами <STRONG>поля</STRONG> объект <A href="record-object-ado.md">записи</A> .</span><span class="sxs-lookup"><span data-stu-id="df7cd-124">The <STRONG>GetChunk</STRONG> method does not operate on <STRONG>Field</STRONG> objects of a <A href="record-object-ado.md">Record</A> object.</span></span> <span data-ttu-id="df7cd-125">Он не выполнять любые операции и приведет к ошибке времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="df7cd-125">It does not perform any operation and will produce a run-time error.</span></span></P>



---
title: Метод - Read ActiveX Data Objects (ADO)
TOCTitle: Read Method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e32de818dc88c2bca14a4fefb5eac59abcc91caf
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604705"
---
# <a name="read-method-ado"></a><span data-ttu-id="6d30f-102">Read Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="6d30f-102">Read Method (ADO)</span></span>


<span data-ttu-id="6d30f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d30f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6d30f-104">Считывает указанное число байтов из двоичного объекта [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="6d30f-104">Reads a specified number of bytes from a binary [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d30f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d30f-105">Syntax</span></span>

<span data-ttu-id="6d30f-106">*Variant* = *потока*. Чтение (*NumBytes* )</span><span class="sxs-lookup"><span data-stu-id="6d30f-106">*Variant* = *Stream*.Read (*NumBytes* )</span></span>

## <a name="parameters"></a><span data-ttu-id="6d30f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d30f-107">Parameters</span></span>

  - <span data-ttu-id="6d30f-108">*NumBytes*</span><span class="sxs-lookup"><span data-stu-id="6d30f-108">*NumBytes*</span></span>

  - <span data-ttu-id="6d30f-109">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6d30f-109">Optional.</span></span> <span data-ttu-id="6d30f-110">Значение типа **Long** , указывающее число байтов для чтения из файла или значение [StreamReadEnum](streamreadenum.md) **adReadAll**, который используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6d30f-110">A **Long** value that specifies the number of bytes to read from the file or the [StreamReadEnum](streamreadenum.md) value **adReadAll**, which is the default.</span></span>

<span data-ttu-id="6d30f-111"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="6d30f-111"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="6d30f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d30f-112">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="6d30f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d30f-113">Return value</span></span>
>>>>>>> <span data-ttu-id="6d30f-114">master</span><span class="sxs-lookup"><span data-stu-id="6d30f-114">master</span></span>

<span data-ttu-id="6d30f-115">Метод **Read** считывает указанное число байтов или потока всей из объекта **потока** и возвращает результирующую данных как **Variant**.</span><span class="sxs-lookup"><span data-stu-id="6d30f-115">The **Read** method reads a specified number of bytes or the entire stream from a **Stream** object and returns the resulting data as a **Variant**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d30f-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="6d30f-116">Remarks</span></span>

<span data-ttu-id="6d30f-117">Если *NumBytes* больше, чем количество байтов, оставшихся в **потоке**, возвращаются только остаток байтов.</span><span class="sxs-lookup"><span data-stu-id="6d30f-117">If *NumBytes* is more than the number of bytes left in the **Stream**, only the bytes remaining are returned.</span></span> <span data-ttu-id="6d30f-118">Данные, прочитанные не дополняется в соответствии с *NumBytes*заданной длины.</span><span class="sxs-lookup"><span data-stu-id="6d30f-118">The data read is not padded to match the length specified by *NumBytes*.</span></span> <span data-ttu-id="6d30f-119">Если нет байт для чтения, возвращается значение variant нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="6d30f-119">If there are no bytes left to read, a variant with a null value is returned.</span></span> <span data-ttu-id="6d30f-120">**Чтение** не может использоваться для чтения в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="6d30f-120">**Read** cannot be used to read backwards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6d30f-121"><EM>NumBytes</EM> всегда меры в байтах.</span><span class="sxs-lookup"><span data-stu-id="6d30f-121"><EM>NumBytes</EM> always measures bytes.</span></span> <span data-ttu-id="6d30f-122">Для текста <STRONG>поток</STRONG> объектов (<A href="type-property-ado-stream.md">Тип</A> — <STRONG>adTypeText</STRONG>), используйте <A href="readtext-method-ado.md">ReadText</A>.</span><span class="sxs-lookup"><span data-stu-id="6d30f-122">For text <STRONG>Stream</STRONG> objects (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>), use <A href="readtext-method-ado.md">ReadText</A>.</span></span></P>



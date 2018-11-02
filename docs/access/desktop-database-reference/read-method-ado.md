---
title: Метод - Read ActiveX Data Objects (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d6de4ea8a8dd64ff4c0562111f6e42ed089754f3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919460"
---
# <a name="read-method-ado"></a><span data-ttu-id="860da-102">Метод Read (ADO)</span><span class="sxs-lookup"><span data-stu-id="860da-102">Read method (ADO)</span></span>


<span data-ttu-id="860da-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="860da-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="860da-104">Считывает указанное число байтов из двоичного объекта [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="860da-104">Reads a specified number of bytes from a binary [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="860da-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="860da-105">Syntax</span></span>

<span data-ttu-id="860da-106">*Variant* = *потока*. Чтение (*NumBytes* )</span><span class="sxs-lookup"><span data-stu-id="860da-106">*Variant* = *Stream*.Read (*NumBytes* )</span></span>

## <a name="parameters"></a><span data-ttu-id="860da-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="860da-107">Parameters</span></span>

  - <span data-ttu-id="860da-108">*NumBytes*</span><span class="sxs-lookup"><span data-stu-id="860da-108">*NumBytes*</span></span>

  - <span data-ttu-id="860da-109">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="860da-109">Optional.</span></span> <span data-ttu-id="860da-110">Значение типа **Long** , указывающее число байтов для чтения из файла или значение [StreamReadEnum](streamreadenum.md) **adReadAll**, который используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="860da-110">A **Long** value that specifies the number of bytes to read from the file or the [StreamReadEnum](streamreadenum.md) value **adReadAll**, which is the default.</span></span>

## <a name="return-value"></a><span data-ttu-id="860da-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="860da-111">Return value</span></span>

<span data-ttu-id="860da-112">Метод **Read** считывает указанное число байтов или потока всей из объекта **потока** и возвращает результирующую данных как **Variant**.</span><span class="sxs-lookup"><span data-stu-id="860da-112">The **Read** method reads a specified number of bytes or the entire stream from a **Stream** object and returns the resulting data as a **Variant**.</span></span>

## <a name="remarks"></a><span data-ttu-id="860da-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="860da-113">Remarks</span></span>

<span data-ttu-id="860da-114">Если *NumBytes* больше, чем количество байтов, оставшихся в **потоке**, возвращаются только остаток байтов.</span><span class="sxs-lookup"><span data-stu-id="860da-114">If *NumBytes* is more than the number of bytes left in the **Stream**, only the bytes remaining are returned.</span></span> <span data-ttu-id="860da-115">Данные, прочитанные не дополняется в соответствии с *NumBytes*заданной длины.</span><span class="sxs-lookup"><span data-stu-id="860da-115">The data read is not padded to match the length specified by *NumBytes*.</span></span> <span data-ttu-id="860da-116">Если нет байт для чтения, возвращается значение variant нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="860da-116">If there are no bytes left to read, a variant with a null value is returned.</span></span> <span data-ttu-id="860da-117">**Чтение** не может использоваться для чтения в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="860da-117">**Read** cannot be used to read backwards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="860da-118"><EM>NumBytes</EM> всегда меры в байтах.</span><span class="sxs-lookup"><span data-stu-id="860da-118"><EM>NumBytes</EM> always measures bytes.</span></span> <span data-ttu-id="860da-119">Для текста <STRONG>поток</STRONG> объектов (<A href="type-property-ado-stream.md">Тип</A> — <STRONG>adTypeText</STRONG>), используйте <A href="readtext-method-ado.md">ReadText</A>.</span><span class="sxs-lookup"><span data-stu-id="860da-119">For text <STRONG>Stream</STRONG> objects (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>), use <A href="readtext-method-ado.md">ReadText</A>.</span></span></P>



---
title: Метод - Read ActiveX Data Objects (ADO)
TOCTitle: Read Method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4fcc4c3039e1e55bb6bd33078542faa880d27ded
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480937"
---
# <a name="read-method-ado"></a><span data-ttu-id="0dc18-102">Read Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="0dc18-102">Read Method (ADO)</span></span>


<span data-ttu-id="0dc18-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0dc18-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0dc18-104">Считывает указанное число байтов из двоичного объекта [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="0dc18-104">Reads a specified number of bytes from a binary [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dc18-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0dc18-105">Syntax</span></span>

<span data-ttu-id="0dc18-106">*Variant* = *потока*. Чтение (*NumBytes* )</span><span class="sxs-lookup"><span data-stu-id="0dc18-106">*Variant* = *Stream*.Read (*NumBytes* )</span></span>

## <a name="parameters"></a><span data-ttu-id="0dc18-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0dc18-107">Parameters</span></span>

  - <span data-ttu-id="0dc18-108">*NumBytes*</span><span class="sxs-lookup"><span data-stu-id="0dc18-108">*NumBytes*</span></span>

  - <span data-ttu-id="0dc18-109">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="0dc18-109">Optional.</span></span> <span data-ttu-id="0dc18-110">Значение типа **Long** , указывающее число байтов для чтения из файла или значение [StreamReadEnum](streamreadenum.md) **adReadAll**, который используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0dc18-110">A **Long** value that specifies the number of bytes to read from the file or the [StreamReadEnum](streamreadenum.md) value **adReadAll**, which is the default.</span></span>

## <a name="return-value"></a><span data-ttu-id="0dc18-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0dc18-111">Return Value</span></span>

<span data-ttu-id="0dc18-112">Метод **Read** считывает указанное число байтов или потока всей из объекта **потока** и возвращает результирующую данных как **Variant**.</span><span class="sxs-lookup"><span data-stu-id="0dc18-112">The **Read** method reads a specified number of bytes or the entire stream from a **Stream** object and returns the resulting data as a **Variant**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dc18-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="0dc18-113">Remarks</span></span>

<span data-ttu-id="0dc18-114">Если *NumBytes* больше, чем количество байтов, оставшихся в **потоке**, возвращаются только остаток байтов.</span><span class="sxs-lookup"><span data-stu-id="0dc18-114">If *NumBytes* is more than the number of bytes left in the **Stream**, only the bytes remaining are returned.</span></span> <span data-ttu-id="0dc18-115">Данные, прочитанные не дополняется в соответствии с *NumBytes*заданной длины.</span><span class="sxs-lookup"><span data-stu-id="0dc18-115">The data read is not padded to match the length specified by *NumBytes*.</span></span> <span data-ttu-id="0dc18-116">Если нет байт для чтения, возвращается значение variant нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="0dc18-116">If there are no bytes left to read, a variant with a null value is returned.</span></span> <span data-ttu-id="0dc18-117">**Чтение** не может использоваться для чтения в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="0dc18-117">**Read** cannot be used to read backwards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0dc18-118"><EM>NumBytes</EM> всегда меры в байтах.</span><span class="sxs-lookup"><span data-stu-id="0dc18-118"><EM>NumBytes</EM> always measures bytes.</span></span> <span data-ttu-id="0dc18-119">Для текста <STRONG>поток</STRONG> объектов (<A href="type-property-ado-stream.md">Тип</A> — <STRONG>adTypeText</STRONG>), используйте <A href="readtext-method-ado.md">ReadText</A>.</span><span class="sxs-lookup"><span data-stu-id="0dc18-119">For text <STRONG>Stream</STRONG> objects (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>), use <A href="readtext-method-ado.md">ReadText</A>.</span></span></P>



---
title: Метод ReadText (ADO)
TOCTitle: ReadText Method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e4bc9febb76f71068517d2d83cddbdf4edee53b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891137"
---
# <a name="readtext-method-ado"></a><span data-ttu-id="c9288-102">Метод ReadText (ADO)</span><span class="sxs-lookup"><span data-stu-id="c9288-102">ReadText Method (ADO)</span></span>


<span data-ttu-id="c9288-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9288-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9288-104">Число операций чтения указанное число символов из объекта [потока](stream-object-ado.md) текста.</span><span class="sxs-lookup"><span data-stu-id="c9288-104">Reads specified number of characters from a text [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9288-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9288-105">Syntax</span></span>

<span data-ttu-id="c9288-106">*Строка* = *потока*. ReadText (*NumChars*)</span><span class="sxs-lookup"><span data-stu-id="c9288-106">*String* = *Stream*.ReadText (*NumChars*)</span></span>

## <a name="parameters"></a><span data-ttu-id="c9288-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9288-107">Parameters</span></span>

  - <span data-ttu-id="c9288-108">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="c9288-108">*NumChars*</span></span>

  - <span data-ttu-id="c9288-109">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="c9288-109">Optional.</span></span> <span data-ttu-id="c9288-110">**Длинное целое** значение, задающее число символов для чтения из файла, или значение [StreamReadEnum](streamreadenum.md) .</span><span class="sxs-lookup"><span data-stu-id="c9288-110">A **Long** value that specifies the number of characters to read from the file, or a [StreamReadEnum](streamreadenum.md) value.</span></span> <span data-ttu-id="c9288-111">Значение по умолчанию — **adReadAll**.</span><span class="sxs-lookup"><span data-stu-id="c9288-111">The default value is **adReadAll**.</span></span>

## <a name="return-value"></a><span data-ttu-id="c9288-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9288-112">Return value</span></span>

<span data-ttu-id="c9288-113">Метод **ReadText** считывает указанное число символов, строку целиком или всей потока из объекта **потока** и возвращает результирующую строку.</span><span class="sxs-lookup"><span data-stu-id="c9288-113">The **ReadText** method reads a specified number of characters, an entire line, or the entire stream from a **Stream** object and returns the resulting string.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9288-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c9288-114">Remarks</span></span>

<span data-ttu-id="c9288-115">Если *NumChar* больше, чем количество символов в потоке, возвращаются только оставшиеся символы.</span><span class="sxs-lookup"><span data-stu-id="c9288-115">If *NumChar* is more than the number of characters left in the stream, only the characters remaining are returned.</span></span> <span data-ttu-id="c9288-116">Чтение строки не дополняется в соответствии с *NumChar*заданной длины.</span><span class="sxs-lookup"><span data-stu-id="c9288-116">The string read is not padded to match the length specified by *NumChar*.</span></span> <span data-ttu-id="c9288-117">Если не используются никакие символы для чтения, возвращается значение типа variant, значение которого равно null.</span><span class="sxs-lookup"><span data-stu-id="c9288-117">If there are no characters left to read, a variant whose value is null is returned.</span></span> <span data-ttu-id="c9288-118">**ReadText** не может использоваться для чтения в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="c9288-118">**ReadText** cannot be used to read backwards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c9288-119">Метод <STRONG>ReadText</STRONG> используется с потоками текст (<A href="type-property-ado-stream.md">Тип</A> — <STRONG>adTypeText</STRONG>).</span><span class="sxs-lookup"><span data-stu-id="c9288-119">The <STRONG>ReadText</STRONG> method is used with text streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>).</span></span> <span data-ttu-id="c9288-120">Для двоичного файла потоков (<STRONG>Тип</STRONG> — <STRONG>adTypeBinary</STRONG>), используйте <A href="read-method-ado.md">чтения</A>.</span><span class="sxs-lookup"><span data-stu-id="c9288-120">For binary streams (<STRONG>Type</STRONG> is <STRONG>adTypeBinary</STRONG>), use <A href="read-method-ado.md">Read</A>.</span></span></P>



---
title: Метод ReadText (ADO)
TOCTitle: ReadText method (ADO)
ms:assetid: 08f5bac4-dccd-696c-09a7-e1ba0cb38d79
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248826(v=office.15)
ms:contentKeyID: 48543108
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 883f74c06da83a46f9ffd1c30861d796c04b5c74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300800"
---
# <a name="readtext-method-ado"></a><span data-ttu-id="5f7a6-102">Метод ReadText (ADO)</span><span class="sxs-lookup"><span data-stu-id="5f7a6-102">ReadText method (ADO)</span></span>

<span data-ttu-id="5f7a6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f7a6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5f7a6-104">Считывает указанное число символов из текстового объекта [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="5f7a6-104">Reads specified number of characters from a text [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f7a6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5f7a6-105">Syntax</span></span>

<span data-ttu-id="5f7a6-106">*Строковый* = *поток*. ReadText (*нумчарс*)</span><span class="sxs-lookup"><span data-stu-id="5f7a6-106">*String* = *Stream*.ReadText (*NumChars*)</span></span>

## <a name="parameters"></a><span data-ttu-id="5f7a6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f7a6-107">Parameters</span></span>

|<span data-ttu-id="5f7a6-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="5f7a6-108">Parameter</span></span>|<span data-ttu-id="5f7a6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5f7a6-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5f7a6-110">*нумчарс*</span><span class="sxs-lookup"><span data-stu-id="5f7a6-110">*NumChars*</span></span> |<span data-ttu-id="5f7a6-111">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="5f7a6-111">Optional.</span></span> <span data-ttu-id="5f7a6-112">**Длинное** значение, задающее количество символов, считываемых из файла, или значение [стреамреаденум](streamreadenum.md) .</span><span class="sxs-lookup"><span data-stu-id="5f7a6-112">A **Long** value that specifies the number of characters to read from the file, or a [StreamReadEnum](streamreadenum.md) value.</span></span> <span data-ttu-id="5f7a6-113">Значение по умолчанию — **адреадалл**.</span><span class="sxs-lookup"><span data-stu-id="5f7a6-113">The default value is **adReadAll**.</span></span>|

## <a name="return-value"></a><span data-ttu-id="5f7a6-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5f7a6-114">Return value</span></span>

<span data-ttu-id="5f7a6-115">Метод **ReadText** считывает указанное число символов, всю строку или весь поток из объекта **Stream** и возвращает результирующую строку.</span><span class="sxs-lookup"><span data-stu-id="5f7a6-115">The **ReadText** method reads a specified number of characters, an entire line, or the entire stream from a **Stream** object and returns the resulting string.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f7a6-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="5f7a6-116">Remarks</span></span>

<span data-ttu-id="5f7a6-117">Если *нумчар* превышает количество символов в потоке, возвращаются только оставшиеся символы.</span><span class="sxs-lookup"><span data-stu-id="5f7a6-117">If *NumChar* is more than the number of characters left in the stream, only the characters remaining are returned.</span></span> <span data-ttu-id="5f7a6-118">Прочитанная строка не заполняется в соответствии с длиной, указанной в параметре *нумчар*.</span><span class="sxs-lookup"><span data-stu-id="5f7a6-118">The string read is not padded to match the length specified by *NumChar*.</span></span> <span data-ttu-id="5f7a6-119">Если не осталось символов для чтения, возвращается Variant со значением NULL.</span><span class="sxs-lookup"><span data-stu-id="5f7a6-119">If there are no characters left to read, a variant whose value is null is returned.</span></span> <span data-ttu-id="5f7a6-120">Не удается использовать **ReadText** для чтения в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="5f7a6-120">**ReadText** cannot be used to read backwards.</span></span>

> [!NOTE]
> <span data-ttu-id="5f7a6-121">Метод **ReadText** используется с текстовыми потоками ([Type](type-property-ado-stream.md) — **адтипетекст**).</span><span class="sxs-lookup"><span data-stu-id="5f7a6-121">The **ReadText** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span> <span data-ttu-id="5f7a6-122">Для двоичных потоков (**Type** — **Адтипебинари**) используйте [Read](read-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5f7a6-122">For binary streams (**Type** is **adTypeBinary**), use [Read](read-method-ado.md).</span></span>


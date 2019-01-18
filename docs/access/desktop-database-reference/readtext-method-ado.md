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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699935"
---
# <a name="readtext-method-ado"></a><span data-ttu-id="95087-102">Метод ReadText (ADO)</span><span class="sxs-lookup"><span data-stu-id="95087-102">ReadText method (ADO)</span></span>

<span data-ttu-id="95087-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="95087-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95087-104">Число операций чтения указанное число символов из объекта [потока](stream-object-ado.md) текста.</span><span class="sxs-lookup"><span data-stu-id="95087-104">Reads specified number of characters from a text [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="95087-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95087-105">Syntax</span></span>

<span data-ttu-id="95087-106">*Строка* = *потока*. ReadText (*NumChars*)</span><span class="sxs-lookup"><span data-stu-id="95087-106">*String* = *Stream*.ReadText (*NumChars*)</span></span>

## <a name="parameters"></a><span data-ttu-id="95087-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="95087-107">Parameters</span></span>

|<span data-ttu-id="95087-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="95087-108">Parameter</span></span>|<span data-ttu-id="95087-109">Описание</span><span class="sxs-lookup"><span data-stu-id="95087-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="95087-110">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="95087-110">*NumChars*</span></span> |<span data-ttu-id="95087-111">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="95087-111">Optional.</span></span> <span data-ttu-id="95087-112">**Длинное целое** значение, задающее число символов для чтения из файла, или значение [StreamReadEnum](streamreadenum.md) .</span><span class="sxs-lookup"><span data-stu-id="95087-112">A **Long** value that specifies the number of characters to read from the file, or a [StreamReadEnum](streamreadenum.md) value.</span></span> <span data-ttu-id="95087-113">Значение по умолчанию — **adReadAll**.</span><span class="sxs-lookup"><span data-stu-id="95087-113">The default value is **adReadAll**.</span></span>|

## <a name="return-value"></a><span data-ttu-id="95087-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95087-114">Return value</span></span>

<span data-ttu-id="95087-115">Метод **ReadText** считывает указанное число символов, строку целиком или всей потока из объекта **потока** и возвращает результирующую строку.</span><span class="sxs-lookup"><span data-stu-id="95087-115">The **ReadText** method reads a specified number of characters, an entire line, or the entire stream from a **Stream** object and returns the resulting string.</span></span>

## <a name="remarks"></a><span data-ttu-id="95087-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="95087-116">Remarks</span></span>

<span data-ttu-id="95087-117">Если *NumChar* больше, чем количество символов в потоке, возвращаются только оставшиеся символы.</span><span class="sxs-lookup"><span data-stu-id="95087-117">If *NumChar* is more than the number of characters left in the stream, only the characters remaining are returned.</span></span> <span data-ttu-id="95087-118">Чтение строки не дополняется в соответствии с *NumChar*заданной длины.</span><span class="sxs-lookup"><span data-stu-id="95087-118">The string read is not padded to match the length specified by *NumChar*.</span></span> <span data-ttu-id="95087-119">Если не используются никакие символы для чтения, возвращается значение типа variant, значение которого равно null.</span><span class="sxs-lookup"><span data-stu-id="95087-119">If there are no characters left to read, a variant whose value is null is returned.</span></span> <span data-ttu-id="95087-120">**ReadText** не может использоваться для чтения в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="95087-120">**ReadText** cannot be used to read backwards.</span></span>

> [!NOTE]
> <span data-ttu-id="95087-121">Метод **ReadText** используется с потоками текст ([Тип](type-property-ado-stream.md) — **adTypeText**).</span><span class="sxs-lookup"><span data-stu-id="95087-121">The **ReadText** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span> <span data-ttu-id="95087-122">Для двоичного файла потоков (**Тип** — **adTypeBinary**), используйте [чтения](read-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="95087-122">For binary streams (**Type** is **adTypeBinary**), use [Read](read-method-ado.md).</span></span>


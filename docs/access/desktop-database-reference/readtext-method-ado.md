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
# <a name="readtext-method-ado"></a><span data-ttu-id="50cfa-102">Метод ReadText (ADO)</span><span class="sxs-lookup"><span data-stu-id="50cfa-102">ReadText method (ADO)</span></span>

<span data-ttu-id="50cfa-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50cfa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50cfa-104">Считывая указанное количество символов из объекта [Text Stream.](stream-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="50cfa-104">Reads specified number of characters from a text [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="50cfa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50cfa-105">Syntax</span></span>

<span data-ttu-id="50cfa-106">*Строка*  =  *Stream*. ReadText (*NumChars*)</span><span class="sxs-lookup"><span data-stu-id="50cfa-106">*String* = *Stream*.ReadText (*NumChars*)</span></span>

## <a name="parameters"></a><span data-ttu-id="50cfa-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="50cfa-107">Parameters</span></span>

|<span data-ttu-id="50cfa-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="50cfa-108">Parameter</span></span>|<span data-ttu-id="50cfa-109">Описание</span><span class="sxs-lookup"><span data-stu-id="50cfa-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="50cfa-110">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="50cfa-110">*NumChars*</span></span> |<span data-ttu-id="50cfa-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="50cfa-111">Optional.</span></span> <span data-ttu-id="50cfa-112">**Длинное** значение, которое указывает количество символов для чтения из файла или значение [StreamReadEnum.](streamreadenum.md)</span><span class="sxs-lookup"><span data-stu-id="50cfa-112">A **Long** value that specifies the number of characters to read from the file, or a [StreamReadEnum](streamreadenum.md) value.</span></span> <span data-ttu-id="50cfa-113">Значение по умолчанию **— adReadAll.**</span><span class="sxs-lookup"><span data-stu-id="50cfa-113">The default value is **adReadAll**.</span></span>|

## <a name="return-value"></a><span data-ttu-id="50cfa-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50cfa-114">Return value</span></span>

<span data-ttu-id="50cfa-115">Метод **ReadText** считыет указанное количество символов, всю строку или весь поток из объекта **Stream** и возвращает итоговую строку.</span><span class="sxs-lookup"><span data-stu-id="50cfa-115">The **ReadText** method reads a specified number of characters, an entire line, or the entire stream from a **Stream** object and returns the resulting string.</span></span>

## <a name="remarks"></a><span data-ttu-id="50cfa-116">Заметки</span><span class="sxs-lookup"><span data-stu-id="50cfa-116">Remarks</span></span>

<span data-ttu-id="50cfa-117">Если *NumChar* больше количества символов, оставшихся в потоке, возвращаются только оставшиеся символы.</span><span class="sxs-lookup"><span data-stu-id="50cfa-117">If *NumChar* is more than the number of characters left in the stream, only the characters remaining are returned.</span></span> <span data-ttu-id="50cfa-118">Строка чтения не заполнена в соответствие с длиной, указанной *NumChar.*</span><span class="sxs-lookup"><span data-stu-id="50cfa-118">The string read is not padded to match the length specified by *NumChar*.</span></span> <span data-ttu-id="50cfa-119">Если для чтения не осталось символов, возвращается вариант, значение которого null.</span><span class="sxs-lookup"><span data-stu-id="50cfa-119">If there are no characters left to read, a variant whose value is null is returned.</span></span> <span data-ttu-id="50cfa-120">**ReadText** нельзя использовать для чтения в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="50cfa-120">**ReadText** cannot be used to read backwards.</span></span>

> [!NOTE]
> <span data-ttu-id="50cfa-121">Метод **ReadText** используется с текстовыми потоками [(тип](type-property-ado-stream.md) **adTypeText).**</span><span class="sxs-lookup"><span data-stu-id="50cfa-121">The **ReadText** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span> <span data-ttu-id="50cfa-122">Для двоичных потоков (**Тип** **adTypeBinary),** используйте [чтение](read-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="50cfa-122">For binary streams (**Type** is **adTypeBinary**), use [Read](read-method-ado.md).</span></span>


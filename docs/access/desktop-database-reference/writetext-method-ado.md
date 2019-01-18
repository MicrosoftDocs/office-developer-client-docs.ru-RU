---
title: Метод WriteText (ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 92983163a909e72c3da142ebcf63b7e0723e96af
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726248"
---
# <a name="writetext-method-ado"></a><span data-ttu-id="149de-102">Метод WriteText (ADO)</span><span class="sxs-lookup"><span data-stu-id="149de-102">WriteText method (ADO)</span></span>

<span data-ttu-id="149de-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="149de-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="149de-104">Записывает строку, указанный текст в объект [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="149de-104">Writes a specified text string to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="149de-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="149de-105">Syntax</span></span>

<span data-ttu-id="149de-106">*Поток*. WriteText*данных*, *Параметры*</span><span class="sxs-lookup"><span data-stu-id="149de-106">*Stream*.WriteText*Data*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="149de-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="149de-107">Parameters</span></span>

|<span data-ttu-id="149de-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="149de-108">Parameter</span></span>|<span data-ttu-id="149de-109">Описание</span><span class="sxs-lookup"><span data-stu-id="149de-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="149de-110">*Данные*</span><span class="sxs-lookup"><span data-stu-id="149de-110">*Data*</span></span> |<span data-ttu-id="149de-111">**Строковое** значение, содержащее текст в символов для записи.</span><span class="sxs-lookup"><span data-stu-id="149de-111">A **String** value that contains the text in characters to be written.</span></span>|
|<span data-ttu-id="149de-112">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="149de-112">*Options*</span></span> |<span data-ttu-id="149de-113">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="149de-113">Optional.</span></span> <span data-ttu-id="149de-114">[StreamWriteEnum](streamwriteenum.md) значение, указывающее, является ли знака разделителя строки должны быть записаны в конце указанной строки.</span><span class="sxs-lookup"><span data-stu-id="149de-114">A [StreamWriteEnum](streamwriteenum.md) value that specifies whether a line separator character must be written at the end of the specified string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="149de-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="149de-115">Remarks</span></span>

<span data-ttu-id="149de-116">Объект **потока** без промежуточных пробелов и знаков между каждую строку, записывается заданных строк.</span><span class="sxs-lookup"><span data-stu-id="149de-116">Specified strings are written to the **Stream** object without any intervening spaces or characters between each string.</span></span>

<span data-ttu-id="149de-117">Символ, следующий записываемые данные имеет значение текущей [позиции](position-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="149de-117">The current [Position](position-property-ado.md) is set to the character following the written data.</span></span> <span data-ttu-id="149de-118">Метод **WriteText** не усекать остальную часть данных в поток.</span><span class="sxs-lookup"><span data-stu-id="149de-118">The **WriteText** method does not truncate the rest of the data in a stream.</span></span> <span data-ttu-id="149de-119">Если вы хотите усекать эти символы, вызовите [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="149de-119">If you want to truncate these characters, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="149de-120">Если записать за текущую позицию [EOS](eos-property-ado.md) будет увеличить [размер](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) **потока** , содержит новые символы и **EOS** будут перемещаться до нового получения последнего байта в **поток**.</span><span class="sxs-lookup"><span data-stu-id="149de-120">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) of the **Stream** will be increased to contain any new characters, and **EOS** will move to the new last byte in the **Stream**.</span></span>

> [!NOTE]
> <span data-ttu-id="149de-121">Метод **WriteText** используется с потоками текст ([Тип](type-property-ado-stream.md) — **adTypeText**).</span><span class="sxs-lookup"><span data-stu-id="149de-121">The **WriteText** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span> <span data-ttu-id="149de-122">Для двоичного файла потоков (**Тип** — **adTypeBinary**), используйте [запись](write-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="149de-122">For binary streams (**Type** is **adTypeBinary**), use [Write](write-method-ado.md).</span></span>



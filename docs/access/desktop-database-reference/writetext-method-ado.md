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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308269"
---
# <a name="writetext-method-ado"></a><span data-ttu-id="cc304-102">Метод WriteText (ADO)</span><span class="sxs-lookup"><span data-stu-id="cc304-102">WriteText method (ADO)</span></span>

<span data-ttu-id="cc304-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc304-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc304-104">Записывает указанную текстовую строку на [объект Stream.](stream-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="cc304-104">Writes a specified text string to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc304-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc304-105">Syntax</span></span>

<span data-ttu-id="cc304-106">*Stream*. WriteText *Data*, *Options*</span><span class="sxs-lookup"><span data-stu-id="cc304-106">*Stream*.WriteText *Data*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="cc304-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc304-107">Parameters</span></span>

|<span data-ttu-id="cc304-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="cc304-108">Parameter</span></span>|<span data-ttu-id="cc304-109">Описание</span><span class="sxs-lookup"><span data-stu-id="cc304-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="cc304-110">*Data*</span><span class="sxs-lookup"><span data-stu-id="cc304-110">*Data*</span></span> |<span data-ttu-id="cc304-111">**Строковое** значение, содержа которое содержит текст в символах, которые будут написаны.</span><span class="sxs-lookup"><span data-stu-id="cc304-111">A **String** value that contains the text in characters to be written.</span></span>|
|<span data-ttu-id="cc304-112">*Options*</span><span class="sxs-lookup"><span data-stu-id="cc304-112">*Options*</span></span> |<span data-ttu-id="cc304-113">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="cc304-113">Optional.</span></span> <span data-ttu-id="cc304-114">Значение [StreamWriteEnum,](streamwriteenum.md) которое указывает, должен ли символ сепаратора строки быть написан в конце указанной строки.</span><span class="sxs-lookup"><span data-stu-id="cc304-114">A [StreamWriteEnum](streamwriteenum.md) value that specifies whether a line separator character must be written at the end of the specified string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="cc304-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="cc304-115">Remarks</span></span>

<span data-ttu-id="cc304-116">Указанные строки пишутся в объект **Stream** без каких-либо пересекающихся пространств или символов между каждой строкой.</span><span class="sxs-lookup"><span data-stu-id="cc304-116">Specified strings are written to the **Stream** object without any intervening spaces or characters between each string.</span></span>

<span data-ttu-id="cc304-117">Текущая [позиция](position-property-ado.md) устанавливается для символа, следующего за письменными данными.</span><span class="sxs-lookup"><span data-stu-id="cc304-117">The current [Position](position-property-ado.md) is set to the character following the written data.</span></span> <span data-ttu-id="cc304-118">Метод **WriteText** не усечен остальных данных в потоке.</span><span class="sxs-lookup"><span data-stu-id="cc304-118">The **WriteText** method does not truncate the rest of the data in a stream.</span></span> <span data-ttu-id="cc304-119">Если вы хотите усечение этих символов, позвоните [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cc304-119">If you want to truncate these characters, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="cc304-120">Если вы напишете текущую [](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) позицию  [EOS,](eos-property-ado.md) размер потока будет увеличен, чтобы содержать новые символы, и **EOS** перейдет к новому последнему byte в **потоке**.</span><span class="sxs-lookup"><span data-stu-id="cc304-120">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) of the **Stream** will be increased to contain any new characters, and **EOS** will move to the new last byte in the **Stream**.</span></span>

> [!NOTE]
> <span data-ttu-id="cc304-121">Метод **WriteText** используется с текстовыми потоками [(Type](type-property-ado-stream.md) **is adTypeText).**</span><span class="sxs-lookup"><span data-stu-id="cc304-121">The **WriteText** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span> <span data-ttu-id="cc304-122">Для двоичных потоков **(Type** **is adTypeBinary),** используйте [Write](write-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cc304-122">For binary streams (**Type** is **adTypeBinary**), use [Write](write-method-ado.md).</span></span>



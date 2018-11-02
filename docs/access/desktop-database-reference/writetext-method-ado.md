---
title: Метод WriteText (ADO)
TOCTitle: WriteText method (ADO)
ms:assetid: 1ca2d9d5-11f4-d088-6fc3-53240208bb09
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248963(v=office.15)
ms:contentKeyID: 48543574
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c0c4668141c0da6e5faddee009d2548f1ee2c53
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926999"
---
# <a name="writetext-method-ado"></a><span data-ttu-id="4a6c3-102">Метод WriteText (ADO)</span><span class="sxs-lookup"><span data-stu-id="4a6c3-102">WriteText method (ADO)</span></span>


<span data-ttu-id="4a6c3-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a6c3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a6c3-104">Записывает строку, указанный текст в объект [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="4a6c3-104">Writes a specified text string to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a6c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a6c3-105">Syntax</span></span>

<span data-ttu-id="4a6c3-106">*Поток*. WriteText*данных*, *Параметры*</span><span class="sxs-lookup"><span data-stu-id="4a6c3-106">*Stream*.WriteText*Data*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="4a6c3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4a6c3-107">Parameters</span></span>

  - <span data-ttu-id="4a6c3-108">*Данные*</span><span class="sxs-lookup"><span data-stu-id="4a6c3-108">*Data*</span></span>

  - <span data-ttu-id="4a6c3-109">**Строковое** значение, содержащее текст в символов для записи.</span><span class="sxs-lookup"><span data-stu-id="4a6c3-109">A **String** value that contains the text in characters to be written.</span></span>

  - <span data-ttu-id="4a6c3-110">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="4a6c3-110">*Options*</span></span>

  - <span data-ttu-id="4a6c3-111">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="4a6c3-111">Optional.</span></span> <span data-ttu-id="4a6c3-112">[StreamWriteEnum](streamwriteenum.md) значение, указывающее, является ли знака разделителя строки должны быть записаны в конце указанной строки.</span><span class="sxs-lookup"><span data-stu-id="4a6c3-112">A [StreamWriteEnum](streamwriteenum.md) value that specifies whether a line separator character must be written at the end of the specified string.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a6c3-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a6c3-113">Remarks</span></span>

<span data-ttu-id="4a6c3-114">Объект **потока** без промежуточных пробелов и знаков между каждую строку, записывается заданных строк.</span><span class="sxs-lookup"><span data-stu-id="4a6c3-114">Specified strings are written to the **Stream** object without any intervening spaces or characters between each string.</span></span>

<span data-ttu-id="4a6c3-115">Символ, следующий записываемые данные имеет значение текущей [позиции](position-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="4a6c3-115">The current [Position](position-property-ado.md) is set to the character following the written data.</span></span> <span data-ttu-id="4a6c3-116">Метод **WriteText** не усекать остальную часть данных в поток.</span><span class="sxs-lookup"><span data-stu-id="4a6c3-116">The **WriteText** method does not truncate the rest of the data in a stream.</span></span> <span data-ttu-id="4a6c3-117">Если вы хотите усекать эти символы, вызовите [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="4a6c3-117">If you want to truncate these characters, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="4a6c3-118">Если записать за текущую позицию [EOS](eos-property-ado.md) будет увеличить [размер](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) **потока** , содержит новые символы и **EOS** будут перемещаться до нового получения последнего байта в **поток**.</span><span class="sxs-lookup"><span data-stu-id="4a6c3-118">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new characters, and **EOS** will move to the new last byte in the **Stream**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4a6c3-119">Метод <STRONG>WriteText</STRONG> используется с потоками текст (<A href="type-property-ado-stream.md">Тип</A> — <STRONG>adTypeText</STRONG>).</span><span class="sxs-lookup"><span data-stu-id="4a6c3-119">The <STRONG>WriteText</STRONG> method is used with text streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>).</span></span> <span data-ttu-id="4a6c3-120">Для двоичного файла потоков (<STRONG>Тип</STRONG> — <STRONG>adTypeBinary</STRONG>), используйте <A href="write-method-ado.md">запись</A>.</span><span class="sxs-lookup"><span data-stu-id="4a6c3-120">For binary streams (<STRONG>Type</STRONG> is <STRONG>adTypeBinary</STRONG>), use <A href="write-method-ado.md">Write</A>.</span></span></P>



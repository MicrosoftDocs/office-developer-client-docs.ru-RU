---
title: Метод - Read ActiveX Data Objects (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ce545b1a6b036cae9f92d7e1ab7ba7479e4e252
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710890"
---
# <a name="read-method-ado"></a><span data-ttu-id="b3349-102">Метод Read (ADO)</span><span class="sxs-lookup"><span data-stu-id="b3349-102">Read method (ADO)</span></span>

<span data-ttu-id="b3349-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3349-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3349-104">Считывает указанное число байтов из двоичного объекта [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b3349-104">Reads a specified number of bytes from a binary [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3349-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3349-105">Syntax</span></span>

<span data-ttu-id="b3349-106">*Variant* = *потока*. Чтение (*NumBytes* )</span><span class="sxs-lookup"><span data-stu-id="b3349-106">*Variant* = *Stream*.Read (*NumBytes* )</span></span>

## <a name="parameters"></a><span data-ttu-id="b3349-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="b3349-107">Parameters</span></span>

|<span data-ttu-id="b3349-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="b3349-108">Parameter</span></span>|<span data-ttu-id="b3349-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b3349-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b3349-110">*NumBytes*</span><span class="sxs-lookup"><span data-stu-id="b3349-110">*NumBytes*</span></span> |<span data-ttu-id="b3349-111">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="b3349-111">Optional.</span></span> <span data-ttu-id="b3349-112">Значение типа **Long** , указывающее число байтов для чтения из файла или значение [StreamReadEnum](streamreadenum.md) **adReadAll**, который используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b3349-112">A **Long** value that specifies the number of bytes to read from the file or the [StreamReadEnum](streamreadenum.md) value **adReadAll**, which is the default.</span></span>|

## <a name="return-value"></a><span data-ttu-id="b3349-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3349-113">Return value</span></span>

<span data-ttu-id="b3349-114">Метод **Read** считывает указанное число байтов или потока всей из объекта **потока** и возвращает результирующую данных как **Variant**.</span><span class="sxs-lookup"><span data-stu-id="b3349-114">The **Read** method reads a specified number of bytes or the entire stream from a **Stream** object and returns the resulting data as a **Variant**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3349-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="b3349-115">Remarks</span></span>

<span data-ttu-id="b3349-116">Если *NumBytes* больше, чем количество байтов, оставшихся в **потоке**, возвращаются только остаток байтов.</span><span class="sxs-lookup"><span data-stu-id="b3349-116">If *NumBytes* is more than the number of bytes left in the **Stream**, only the bytes remaining are returned.</span></span> <span data-ttu-id="b3349-117">Данные, прочитанные не дополняется в соответствии с *NumBytes*заданной длины.</span><span class="sxs-lookup"><span data-stu-id="b3349-117">The data read is not padded to match the length specified by *NumBytes*.</span></span> <span data-ttu-id="b3349-118">Если нет байт для чтения, возвращается значение variant нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="b3349-118">If there are no bytes left to read, a variant with a null value is returned.</span></span> <span data-ttu-id="b3349-119">**Чтение** не может использоваться для чтения в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="b3349-119">**Read** cannot be used to read backwards.</span></span>

> [!NOTE]
> <span data-ttu-id="b3349-120">*NumBytes* всегда меры в байтах.</span><span class="sxs-lookup"><span data-stu-id="b3349-120">*NumBytes* always measures bytes.</span></span> <span data-ttu-id="b3349-121">Для текста **поток** объектов ([Тип](type-property-ado-stream.md) — **adTypeText**), используйте [ReadText](readtext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b3349-121">For text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**), use [ReadText](readtext-method-ado.md).</span></span>



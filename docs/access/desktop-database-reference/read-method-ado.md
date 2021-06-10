---
title: Метод чтения — ActiveX объектов данных (ADO)
TOCTitle: Read method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7ce545b1a6b036cae9f92d7e1ab7ba7479e4e252
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307674"
---
# <a name="read-method-ado"></a><span data-ttu-id="3d2d9-102">Метод чтения (ADO)</span><span class="sxs-lookup"><span data-stu-id="3d2d9-102">Read method (ADO)</span></span>

<span data-ttu-id="3d2d9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d2d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d2d9-104">Считывает определенное количество bytes из двоичного объекта [Stream.](stream-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="3d2d9-104">Reads a specified number of bytes from a binary [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d2d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d2d9-105">Syntax</span></span>

<span data-ttu-id="3d2d9-106">*Variant*  =  *Stream*. Read *(NumBytes)*</span><span class="sxs-lookup"><span data-stu-id="3d2d9-106">*Variant* = *Stream*.Read (*NumBytes* )</span></span>

## <a name="parameters"></a><span data-ttu-id="3d2d9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d2d9-107">Parameters</span></span>

|<span data-ttu-id="3d2d9-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="3d2d9-108">Parameter</span></span>|<span data-ttu-id="3d2d9-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3d2d9-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="3d2d9-110">*NumBytes*</span><span class="sxs-lookup"><span data-stu-id="3d2d9-110">*NumBytes*</span></span> |<span data-ttu-id="3d2d9-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="3d2d9-111">Optional.</span></span> <span data-ttu-id="3d2d9-112">**Длинное** значение, которое указывает количество байтов для чтения из файла или значение [StreamReadEnum](streamreadenum.md) **adReadAll**, которое является по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3d2d9-112">A **Long** value that specifies the number of bytes to read from the file or the [StreamReadEnum](streamreadenum.md) value **adReadAll**, which is the default.</span></span>|

## <a name="return-value"></a><span data-ttu-id="3d2d9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d2d9-113">Return value</span></span>

<span data-ttu-id="3d2d9-114">Метод **Read** считывает определенное количество bytes или весь поток с объекта **Stream** и возвращает полученные данные в качестве **варианта**.</span><span class="sxs-lookup"><span data-stu-id="3d2d9-114">The **Read** method reads a specified number of bytes or the entire stream from a **Stream** object and returns the resulting data as a **Variant**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d2d9-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="3d2d9-115">Remarks</span></span>

<span data-ttu-id="3d2d9-116">Если *numBytes* превышает количество оставленных в потоке bytes, возвращаются только оставшиеся bytes.</span><span class="sxs-lookup"><span data-stu-id="3d2d9-116">If *NumBytes* is more than the number of bytes left in the **Stream**, only the bytes remaining are returned.</span></span> <span data-ttu-id="3d2d9-117">Считываемая информация не соответствует длине, указанной *NumBytes.*</span><span class="sxs-lookup"><span data-stu-id="3d2d9-117">The data read is not padded to match the length specified by *NumBytes*.</span></span> <span data-ttu-id="3d2d9-118">Если для чтения не осталось bytes, возвращается вариант со значением null.</span><span class="sxs-lookup"><span data-stu-id="3d2d9-118">If there are no bytes left to read, a variant with a null value is returned.</span></span> <span data-ttu-id="3d2d9-119">**Чтение** не может использоваться для чтения в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="3d2d9-119">**Read** cannot be used to read backwards.</span></span>

> [!NOTE]
> <span data-ttu-id="3d2d9-120">*NumBytes всегда* измеряет bytes.</span><span class="sxs-lookup"><span data-stu-id="3d2d9-120">*NumBytes* always measures bytes.</span></span> <span data-ttu-id="3d2d9-121">Для объектов **text Stream** [(Type](type-property-ado-stream.md) is **adTypeText),** используйте [ReadText](readtext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="3d2d9-121">For text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**), use [ReadText](readtext-method-ado.md).</span></span>



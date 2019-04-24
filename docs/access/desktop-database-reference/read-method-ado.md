---
title: Метод Read — объекты данных ActiveX (ADO)
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
# <a name="read-method-ado"></a><span data-ttu-id="a4fa4-102">Метод Read (ADO)</span><span class="sxs-lookup"><span data-stu-id="a4fa4-102">Read method (ADO)</span></span>

<span data-ttu-id="a4fa4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a4fa4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a4fa4-104">Считывает указанное число байтов из двоичного объекта [Stream](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a4fa4-104">Reads a specified number of bytes from a binary [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4fa4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4fa4-105">Syntax</span></span>

<span data-ttu-id="a4fa4-106">\*\* = *Поток*Variant. Read (*нумбитес* )</span><span class="sxs-lookup"><span data-stu-id="a4fa4-106">*Variant* = *Stream*.Read (*NumBytes* )</span></span>

## <a name="parameters"></a><span data-ttu-id="a4fa4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4fa4-107">Parameters</span></span>

|<span data-ttu-id="a4fa4-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="a4fa4-108">Parameter</span></span>|<span data-ttu-id="a4fa4-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a4fa4-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a4fa4-110">*Нумбитес*</span><span class="sxs-lookup"><span data-stu-id="a4fa4-110">*NumBytes*</span></span> |<span data-ttu-id="a4fa4-111">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="a4fa4-111">Optional.</span></span> <span data-ttu-id="a4fa4-112">**Длинное** значение, задающее количество байтов для чтения из файла или значение [стреамреаденум](streamreadenum.md) **адреадалл**, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a4fa4-112">A **Long** value that specifies the number of bytes to read from the file or the [StreamReadEnum](streamreadenum.md) value **adReadAll**, which is the default.</span></span>|

## <a name="return-value"></a><span data-ttu-id="a4fa4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4fa4-113">Return value</span></span>

<span data-ttu-id="a4fa4-114">Метод **Read** считывает указанное число байтов или весь поток из объекта **Stream** и возвращает полученные данные в виде **Variant**.</span><span class="sxs-lookup"><span data-stu-id="a4fa4-114">The **Read** method reads a specified number of bytes or the entire stream from a **Stream** object and returns the resulting data as a **Variant**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4fa4-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="a4fa4-115">Remarks</span></span>

<span data-ttu-id="a4fa4-116">Если *нумбитес* больше, чем число байтов, оставшихся в **потоке**, возвращаются только оставшиеся байты.</span><span class="sxs-lookup"><span data-stu-id="a4fa4-116">If *NumBytes* is more than the number of bytes left in the **Stream**, only the bytes remaining are returned.</span></span> <span data-ttu-id="a4fa4-117">Прочитанные данные не дополняются в соответствии с длиной, указанной в параметре *нумбитес*.</span><span class="sxs-lookup"><span data-stu-id="a4fa4-117">The data read is not padded to match the length specified by *NumBytes*.</span></span> <span data-ttu-id="a4fa4-118">Если не осталось байтов для чтения, возвращается Variant со значением NULL.</span><span class="sxs-lookup"><span data-stu-id="a4fa4-118">If there are no bytes left to read, a variant with a null value is returned.</span></span> <span data-ttu-id="a4fa4-119">**Read** не может использоваться для чтения в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="a4fa4-119">**Read** cannot be used to read backwards.</span></span>

> [!NOTE]
> <span data-ttu-id="a4fa4-120">*Нумбитес* всегда измеряется в байтах.</span><span class="sxs-lookup"><span data-stu-id="a4fa4-120">*NumBytes* always measures bytes.</span></span> <span data-ttu-id="a4fa4-121">Для объектов текстовых **потоков** ([Type](type-property-ado-stream.md) — **адтипетекст**) используйте [ReadText](readtext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="a4fa4-121">For text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**), use [ReadText](readtext-method-ado.md).</span></span>



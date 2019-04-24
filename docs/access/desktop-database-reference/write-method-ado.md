---
title: Метод Write — объекты данных ActiveX (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c6f4bba55ec3a32d206d3a7bfd001e96cd94923e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302466"
---
# <a name="write-method-ado"></a><span data-ttu-id="fd4fd-102">Метод Write (ADO)</span><span class="sxs-lookup"><span data-stu-id="fd4fd-102">Write method (ADO)</span></span>

<span data-ttu-id="fd4fd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fd4fd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fd4fd-104">ЗаПисывает двоичные данные в объект [Stream](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="fd4fd-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd4fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd4fd-105">Syntax</span></span>

<span data-ttu-id="fd4fd-106">*Stream*. *Буфер* записи</span><span class="sxs-lookup"><span data-stu-id="fd4fd-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="fd4fd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd4fd-107">Parameters</span></span>

|<span data-ttu-id="fd4fd-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="fd4fd-108">Parameter</span></span>|<span data-ttu-id="fd4fd-109">Описание</span><span class="sxs-lookup"><span data-stu-id="fd4fd-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="fd4fd-110">*Буферизовать*</span><span class="sxs-lookup"><span data-stu-id="fd4fd-110">*Buffer*</span></span> |<span data-ttu-id="fd4fd-111">**Переменная типа Variant** , содержащая массив байтов для записи.</span><span class="sxs-lookup"><span data-stu-id="fd4fd-111">A **Variant** that contains an array of bytes to be written.</span></span>|

## <a name="remarks"></a><span data-ttu-id="fd4fd-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="fd4fd-112">Remarks</span></span>

<span data-ttu-id="fd4fd-113">Указанные байты записываются в объект **Stream** без промежуточных пробелов между ними.</span><span class="sxs-lookup"><span data-stu-id="fd4fd-113">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="fd4fd-114">Текущая [позиция](position-property-ado.md) равна байту после записанных данных.</span><span class="sxs-lookup"><span data-stu-id="fd4fd-114">The current [Position](position-property-ado.md) is set to the byte following the written data.</span></span> <span data-ttu-id="fd4fd-115">Метод **Write** не усекает остальные данные в потоке.</span><span class="sxs-lookup"><span data-stu-id="fd4fd-115">The **Write** method does not truncate the rest of the data in a stream.</span></span> <span data-ttu-id="fd4fd-116">Если вы хотите усечь эти байты, вызовите [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="fd4fd-116">If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="fd4fd-117">Если вы пишете за пределами текущей позиции [](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) [EOS](eos-property-ado.md) , размер **потока** увеличится до того, как будут содержаться новые байты, а **EOS** перейдет к новому последнему байту в **потоке**.</span><span class="sxs-lookup"><span data-stu-id="fd4fd-117">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>

> [!NOTE]
> <span data-ttu-id="fd4fd-118">Метод **Write** используется с двоичными потоками ([Type](type-property-ado-stream.md) — **адтипебинари**).</span><span class="sxs-lookup"><span data-stu-id="fd4fd-118">The **Write** method is used with binary streams ([Type](type-property-ado-stream.md) is **adTypeBinary**).</span></span> <span data-ttu-id="fd4fd-119">Для текстовых потоков (**Type** — **Адтипетекст**) используйте [WriteText](writetext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="fd4fd-119">For text streams (**Type** is **adTypeText**), use [WriteText](writetext-method-ado.md).</span></span>


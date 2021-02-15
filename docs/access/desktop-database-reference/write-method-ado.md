---
title: Метод Write — ActiveX Data Objects (ADO)
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
# <a name="write-method-ado"></a><span data-ttu-id="8860b-102">Метод Write (ADO)</span><span class="sxs-lookup"><span data-stu-id="8860b-102">Write method (ADO)</span></span>

<span data-ttu-id="8860b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8860b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8860b-104">Записывает двоичные данные в [объект Stream.](stream-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="8860b-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8860b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8860b-105">Syntax</span></span>

<span data-ttu-id="8860b-106">*Stream*. Буфер *записи*</span><span class="sxs-lookup"><span data-stu-id="8860b-106">*Stream*.Write *Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="8860b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8860b-107">Parameters</span></span>

|<span data-ttu-id="8860b-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="8860b-108">Parameter</span></span>|<span data-ttu-id="8860b-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8860b-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="8860b-110">*Буфер*</span><span class="sxs-lookup"><span data-stu-id="8860b-110">*Buffer*</span></span> |<span data-ttu-id="8860b-111">**Вариант,** содержащий массив данных, которые необходимо написать.</span><span class="sxs-lookup"><span data-stu-id="8860b-111">A **Variant** that contains an array of bytes to be written.</span></span>|

## <a name="remarks"></a><span data-ttu-id="8860b-112">Заметки</span><span class="sxs-lookup"><span data-stu-id="8860b-112">Remarks</span></span>

<span data-ttu-id="8860b-113">Указанные bytes are written to the **Stream** object without any intervening spaces between each byte.</span><span class="sxs-lookup"><span data-stu-id="8860b-113">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="8860b-114">Текущее [положение](position-property-ado.md) устанавливается в соответствии с письменными данными в соответствии с данными.</span><span class="sxs-lookup"><span data-stu-id="8860b-114">The current [Position](position-property-ado.md) is set to the byte following the written data.</span></span> <span data-ttu-id="8860b-115">Метод **Write** не усечен остальных данных в потоке.</span><span class="sxs-lookup"><span data-stu-id="8860b-115">The **Write** method does not truncate the rest of the data in a stream.</span></span> <span data-ttu-id="8860b-116">Если вы хотите усечение этих данных, вызовите [SetEOS.](seteos-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="8860b-116">If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="8860b-117">Если вы напишете после текущей [](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) позиции  [EOS,](eos-property-ado.md) размер потока будет увеличен, чтобы содержать любые новые bytes, и **EOS** перейдет к новому последнему byte в **Stream**.</span><span class="sxs-lookup"><span data-stu-id="8860b-117">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>

> [!NOTE]
> <span data-ttu-id="8860b-118">Метод **Write** используется с двоичными потоками [(тип](type-property-ado-stream.md) **adTypeBinary).**</span><span class="sxs-lookup"><span data-stu-id="8860b-118">The **Write** method is used with binary streams ([Type](type-property-ado-stream.md) is **adTypeBinary**).</span></span> <span data-ttu-id="8860b-119">Для текстовых потоков **(тип** **adTypeText),** используйте [WriteText](writetext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="8860b-119">For text streams (**Type** is **adTypeText**), use [WriteText](writetext-method-ado.md).</span></span>


---
title: Создание метода - ActiveX Data Objects (ADO)
TOCTitle: Write Method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98af810c9a24d38a6b2b32db31f9a650c2d6f70a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482525"
---
# <a name="write-method-ado"></a><span data-ttu-id="63a2d-102">Write Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="63a2d-102">Write Method (ADO)</span></span>


<span data-ttu-id="63a2d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="63a2d-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="63a2d-104">Записывает двоичные данные в объект [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="63a2d-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="63a2d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63a2d-105">Syntax</span></span>

<span data-ttu-id="63a2d-106">*Поток*. Запись*буфера*</span><span class="sxs-lookup"><span data-stu-id="63a2d-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="63a2d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="63a2d-107">Parameters</span></span>

  - <span data-ttu-id="63a2d-108">*Буфера*</span><span class="sxs-lookup"><span data-stu-id="63a2d-108">*Buffer*</span></span>

  - <span data-ttu-id="63a2d-109">**Variant** , содержащее массив байтов для записи.</span><span class="sxs-lookup"><span data-stu-id="63a2d-109">A **Variant** that contains an array of bytes to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="63a2d-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="63a2d-110">Remarks</span></span>

<span data-ttu-id="63a2d-111">Объект **потока** без пробелов промежуточных между каждый байт записывается указанный байт.</span><span class="sxs-lookup"><span data-stu-id="63a2d-111">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="63a2d-112">Текущей [позиции](position-property-ado.md) задано значение байт следующие записываемые данные.</span><span class="sxs-lookup"><span data-stu-id="63a2d-112">The current [Position](position-property-ado.md) is set to the byte following the written data.</span></span> <span data-ttu-id="63a2d-113">Метод **Write** не усекать остальную часть данных в поток.</span><span class="sxs-lookup"><span data-stu-id="63a2d-113">The **Write** method does not truncate the rest of the data in a stream.</span></span> <span data-ttu-id="63a2d-114">Если вы хотите усечение этих байт, вызовите [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="63a2d-114">If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="63a2d-115">Если записать за текущую позицию [EOS](eos-property-ado.md) будет увеличить [размер](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) **потока** , содержать любые новые байт и **EOS** будут перемещаться до нового получения последнего байта в **поток**.</span><span class="sxs-lookup"><span data-stu-id="63a2d-115">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="63a2d-116">Метод <STRONG>Write</STRONG> используется с двоичных потоков (<A href="type-property-ado-stream.md">Тип</A> — <STRONG>adTypeBinary</STRONG>).</span><span class="sxs-lookup"><span data-stu-id="63a2d-116">The <STRONG>Write</STRONG> method is used with binary streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeBinary</STRONG>).</span></span> <span data-ttu-id="63a2d-117">Для текста потоков (<STRONG>Тип</STRONG> — <STRONG>adTypeText</STRONG>) используйте <A href="writetext-method-ado.md">WriteText</A>.</span><span class="sxs-lookup"><span data-stu-id="63a2d-117">For text streams (<STRONG>Type</STRONG> is <STRONG>adTypeText</STRONG>), use <A href="writetext-method-ado.md">WriteText</A>.</span></span></P>



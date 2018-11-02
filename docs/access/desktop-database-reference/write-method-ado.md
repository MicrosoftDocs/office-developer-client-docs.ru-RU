---
title: Создание метода - ActiveX Data Objects (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a04825a59f19b6b54fbb10652a1bba2fd0479588
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920965"
---
# <a name="write-method-ado"></a><span data-ttu-id="f53a1-102">Метод Write (ADO)</span><span class="sxs-lookup"><span data-stu-id="f53a1-102">Write method (ADO)</span></span>


<span data-ttu-id="f53a1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f53a1-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="f53a1-104">Записывает двоичные данные в объект [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="f53a1-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f53a1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f53a1-105">Syntax</span></span>

<span data-ttu-id="f53a1-106">*Поток*. Запись*буфера*</span><span class="sxs-lookup"><span data-stu-id="f53a1-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="f53a1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f53a1-107">Parameters</span></span>

  - <span data-ttu-id="f53a1-108">*Буфера*</span><span class="sxs-lookup"><span data-stu-id="f53a1-108">*Buffer*</span></span>

  - <span data-ttu-id="f53a1-109">**Variant** , содержащее массив байтов для записи.</span><span class="sxs-lookup"><span data-stu-id="f53a1-109">A **Variant** that contains an array of bytes to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="f53a1-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="f53a1-110">Remarks</span></span>

<span data-ttu-id="f53a1-111">Объект **потока** без пробелов промежуточных между каждый байт записывается указанный байт.</span><span class="sxs-lookup"><span data-stu-id="f53a1-111">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="f53a1-112">Текущей [позиции](position-property-ado.md) задано значение байт следующие записываемые данные.</span><span class="sxs-lookup"><span data-stu-id="f53a1-112">The current [Position](position-property-ado.md) is set to the byte following the written data.</span></span> <span data-ttu-id="f53a1-113">Метод **Write** не усекать остальную часть данных в поток.</span><span class="sxs-lookup"><span data-stu-id="f53a1-113">The **Write** method does not truncate the rest of the data in a stream.</span></span> <span data-ttu-id="f53a1-114">Если вы хотите усечение этих байт, вызовите [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f53a1-114">If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="f53a1-115">Если записать за текущую позицию [EOS](eos-property-ado.md) будет увеличить [размер](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) **потока** , содержать любые новые байт и **EOS** будут перемещаться до нового получения последнего байта в **поток**.</span><span class="sxs-lookup"><span data-stu-id="f53a1-115">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="f53a1-116">Метод <STRONG>Write</STRONG> используется с двоичных потоков (<A href="type-property-ado-stream.md">Тип</A> — <STRONG>adTypeBinary</STRONG>).</span><span class="sxs-lookup"><span data-stu-id="f53a1-116">The <STRONG>Write</STRONG> method is used with binary streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeBinary</STRONG>).</span></span> <span data-ttu-id="f53a1-117">Для текста потоков (<STRONG>Тип</STRONG> — <STRONG>adTypeText</STRONG>) используйте <A href="writetext-method-ado.md">WriteText</A>.</span><span class="sxs-lookup"><span data-stu-id="f53a1-117">For text streams (<STRONG>Type</STRONG> is <STRONG>adTypeText</STRONG>), use <A href="writetext-method-ado.md">WriteText</A>.</span></span></P>



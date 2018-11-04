---
title: Создание метода - ActiveX Data Objects (ADO)
TOCTitle: Write method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 93336294380ffa207f47adbcad630be3fdd1a8b8
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950218"
---
# <a name="write-method-ado"></a><span data-ttu-id="cff64-102">Метод Write (ADO)</span><span class="sxs-lookup"><span data-stu-id="cff64-102">Write method (ADO)</span></span>

<span data-ttu-id="cff64-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cff64-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cff64-104">Записывает двоичные данные в объект [потока](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="cff64-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cff64-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cff64-105">Syntax</span></span>

<span data-ttu-id="cff64-106">*Поток*. Запись*буфера*</span><span class="sxs-lookup"><span data-stu-id="cff64-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="cff64-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cff64-107">Parameters</span></span>

|<span data-ttu-id="cff64-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="cff64-108">Parameter</span></span>|<span data-ttu-id="cff64-109">Описание</span><span class="sxs-lookup"><span data-stu-id="cff64-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="cff64-110">*Буфера*</span><span class="sxs-lookup"><span data-stu-id="cff64-110">*Buffer*</span></span> |<span data-ttu-id="cff64-111">**Variant** , содержащее массив байтов для записи.</span><span class="sxs-lookup"><span data-stu-id="cff64-111">A **Variant** that contains an array of bytes to be written.</span></span>|

## <a name="remarks"></a><span data-ttu-id="cff64-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="cff64-112">Remarks</span></span>

<span data-ttu-id="cff64-113">Объект **потока** без пробелов промежуточных между каждый байт записывается указанный байт.</span><span class="sxs-lookup"><span data-stu-id="cff64-113">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="cff64-114">Текущей [позиции](position-property-ado.md) задано значение байт следующие записываемые данные.</span><span class="sxs-lookup"><span data-stu-id="cff64-114">The current [Position](position-property-ado.md) is set to the byte following the written data.</span></span> <span data-ttu-id="cff64-115">Метод **Write** не усекать остальную часть данных в поток.</span><span class="sxs-lookup"><span data-stu-id="cff64-115">The **Write** method does not truncate the rest of the data in a stream.</span></span> <span data-ttu-id="cff64-116">Если вы хотите усечение этих байт, вызовите [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cff64-116">If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="cff64-117">Если записать за текущую позицию [EOS](eos-property-ado.md) будет увеличить [размер](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) **потока** , содержать любые новые байт и **EOS** будут перемещаться до нового получения последнего байта в **поток**.</span><span class="sxs-lookup"><span data-stu-id="cff64-117">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>

> [!NOTE]
> <span data-ttu-id="cff64-118">Метод **Write** используется с двоичных потоков ([Тип](type-property-ado-stream.md) — **adTypeBinary**).</span><span class="sxs-lookup"><span data-stu-id="cff64-118">The **Write** method is used with binary streams ([Type](type-property-ado-stream.md) is **adTypeBinary**).</span></span> <span data-ttu-id="cff64-119">Для текста потоков (**Тип** — **adTypeText**) используйте [WriteText](writetext-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cff64-119">For text streams (**Type** is **adTypeText**), use [WriteText](writetext-method-ado.md).</span></span>


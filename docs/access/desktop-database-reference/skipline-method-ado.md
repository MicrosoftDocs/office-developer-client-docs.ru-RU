---
title: Метод SkipLine (ADO)
TOCTitle: SkipLine method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d22aca01c468813f280472281719822a7d884988
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923926"
---
# <a name="skipline-method-ado"></a><span data-ttu-id="b1121-102">Метод SkipLine (ADO)</span><span class="sxs-lookup"><span data-stu-id="b1121-102">SkipLine method (ADO)</span></span>


<span data-ttu-id="b1121-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1121-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b1121-104">Пропускает одну всю строку при чтении текстовый поток.</span><span class="sxs-lookup"><span data-stu-id="b1121-104">Skips one entire line when reading a text stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1121-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1121-105">Syntax</span></span>

<span data-ttu-id="b1121-106">*Поток*. SkipLine</span><span class="sxs-lookup"><span data-stu-id="b1121-106">*Stream*.SkipLine</span></span>

## <a name="remarks"></a><span data-ttu-id="b1121-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="b1121-107">Remarks</span></span>

<span data-ttu-id="b1121-108">Все символы, включая Далее разделителя строки, пропускаются.</span><span class="sxs-lookup"><span data-stu-id="b1121-108">All characters up to, and including the next line separator, are skipped.</span></span> <span data-ttu-id="b1121-109">По умолчанию [LineSeparator](lineseparator-property-ado.md) — **adCRLF**.</span><span class="sxs-lookup"><span data-stu-id="b1121-109">By default, the [LineSeparator](lineseparator-property-ado.md) is **adCRLF**.</span></span> <span data-ttu-id="b1121-110">При попытке пропустить [EOS](eos-property-ado.md)текущей позиции просто останется на **EOS**.</span><span class="sxs-lookup"><span data-stu-id="b1121-110">If you attempt to skip past [EOS](eos-property-ado.md), the current position will simply remain at **EOS**.</span></span>

<span data-ttu-id="b1121-111">Метод **SkipLine** используется с потоками текст ([Тип](type-property-ado-stream.md) — **adTypeText**).</span><span class="sxs-lookup"><span data-stu-id="b1121-111">The **SkipLine** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span>


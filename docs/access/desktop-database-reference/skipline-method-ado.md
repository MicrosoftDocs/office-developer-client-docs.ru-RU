---
title: Метод SkipLine (ADO)
TOCTitle: SkipLine method (ADO)
ms:assetid: 419c24c3-6b84-eed0-5884-f2dcd485dc3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249187(v=office.15)
ms:contentKeyID: 48544456
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5e49b8379f078ad698a4a0040de0eb2e4429fd34
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314562"
---
# <a name="skipline-method-ado"></a><span data-ttu-id="46d8d-102">Метод SkipLine (ADO)</span><span class="sxs-lookup"><span data-stu-id="46d8d-102">SkipLine method (ADO)</span></span>


<span data-ttu-id="46d8d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="46d8d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="46d8d-104">ПроПускает одну строку целиком при чтении текстового потока.</span><span class="sxs-lookup"><span data-stu-id="46d8d-104">Skips one entire line when reading a text stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="46d8d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46d8d-105">Syntax</span></span>

<span data-ttu-id="46d8d-106">*Stream*. SkipLine</span><span class="sxs-lookup"><span data-stu-id="46d8d-106">*Stream*.SkipLine</span></span>

## <a name="remarks"></a><span data-ttu-id="46d8d-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="46d8d-107">Remarks</span></span>

<span data-ttu-id="46d8d-108">Все символы до и включительно разделитель в следующую строку будут пропущены.</span><span class="sxs-lookup"><span data-stu-id="46d8d-108">All characters up to, and including the next line separator, are skipped.</span></span> <span data-ttu-id="46d8d-109">По умолчанию [LineSeparator](lineseparator-property-ado.md) — **адкрлф**.</span><span class="sxs-lookup"><span data-stu-id="46d8d-109">By default, the [LineSeparator](lineseparator-property-ado.md) is **adCRLF**.</span></span> <span data-ttu-id="46d8d-110">Если вы попытаетесь пропустить прошедший [EOS](eos-property-ado.md), текущее положение просто останется в **EOS**.</span><span class="sxs-lookup"><span data-stu-id="46d8d-110">If you attempt to skip past [EOS](eos-property-ado.md), the current position will simply remain at **EOS**.</span></span>

<span data-ttu-id="46d8d-111">Метод **SkipLine** используется с текстовыми потоками ([Type](type-property-ado-stream.md) — **адтипетекст**).</span><span class="sxs-lookup"><span data-stu-id="46d8d-111">The **SkipLine** method is used with text streams ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span>


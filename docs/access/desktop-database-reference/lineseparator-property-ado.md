---
title: Свойство LineSeparator (ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4e941339ad1c8622d1c87ada848a44fa82a9ef2d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289951"
---
# <a name="lineseparator-property-ado"></a><span data-ttu-id="db9c0-102">Свойство LineSeparator (ADO)</span><span class="sxs-lookup"><span data-stu-id="db9c0-102">LineSeparator property (ADO)</span></span>


<span data-ttu-id="db9c0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="db9c0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="db9c0-104">Указывает двоичный символ, который будет использоваться в качестве сепаратора строки в текстовых [объектах Stream.](stream-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="db9c0-104">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="db9c0-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="db9c0-105">Settings and return values</span></span>

<span data-ttu-id="db9c0-106">Задает или возвращает [значение LineSeparatorsEnum,](lineseparatorsenum.md) которое указывает на символ сепаратора строки, используемый в **потоке.**</span><span class="sxs-lookup"><span data-stu-id="db9c0-106">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**.</span></span> <span data-ttu-id="db9c0-107">По умолчанию значение **adCRLF**.</span><span class="sxs-lookup"><span data-stu-id="db9c0-107">The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="db9c0-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="db9c0-108">Remarks</span></span>

<span data-ttu-id="db9c0-109">**LineSeparator** используется для интерпретации строк при чтении контента текстового **потока.**</span><span class="sxs-lookup"><span data-stu-id="db9c0-109">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**.</span></span> <span data-ttu-id="db9c0-110">Строки можно пропустить с помощью метода [SkipLine.](skipline-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="db9c0-110">Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="db9c0-111">**LineSeparator** используется только с текстовыми объектами **Stream** [(Type](type-property-ado-stream.md) **is adTypeText).**</span><span class="sxs-lookup"><span data-stu-id="db9c0-111">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span> <span data-ttu-id="db9c0-112">Это свойство игнорируется, **если Type** **является adTypeBinary.**</span><span class="sxs-lookup"><span data-stu-id="db9c0-112">This property is ignored if **Type** is **adTypeBinary**.</span></span>


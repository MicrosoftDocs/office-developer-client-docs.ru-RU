---
title: Свойство LineSeparator (ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 831b6377ade43b3be04ed21add20fbd10e48ac2f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882506"
---
# <a name="lineseparator-property-ado"></a><span data-ttu-id="e1752-102">Свойство LineSeparator (ADO)</span><span class="sxs-lookup"><span data-stu-id="e1752-102">LineSeparator property (ADO)</span></span>


<span data-ttu-id="e1752-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e1752-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e1752-104">Указывает двоичных символов для использования в качестве разделителя строки в объектах [потока](stream-object-ado.md) текста.</span><span class="sxs-lookup"><span data-stu-id="e1752-104">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e1752-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="e1752-105">Settings and return values</span></span>

<span data-ttu-id="e1752-106">Задает или возвращает [LineSeparatorsEnum](lineseparatorsenum.md) значение, указывающее знак разделителя строки, используемые в **поток**.</span><span class="sxs-lookup"><span data-stu-id="e1752-106">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**.</span></span> <span data-ttu-id="e1752-107">Значение по умолчанию — **adCRLF**.</span><span class="sxs-lookup"><span data-stu-id="e1752-107">The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1752-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="e1752-108">Remarks</span></span>

<span data-ttu-id="e1752-109">**LineSeparator** используется для интерпретации строки при чтении содержимое текста **потока**.</span><span class="sxs-lookup"><span data-stu-id="e1752-109">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**.</span></span> <span data-ttu-id="e1752-110">С помощью метода [SkipLine](skipline-method-ado.md) можно пропустить строки.</span><span class="sxs-lookup"><span data-stu-id="e1752-110">Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="e1752-111">**LineSeparator** используется только с объектами **потока** текста ([Тип](type-property-ado-stream.md) — **adTypeText**).</span><span class="sxs-lookup"><span data-stu-id="e1752-111">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span> <span data-ttu-id="e1752-112">Это свойство игнорируется, если **Тип** — **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="e1752-112">This property is ignored if **Type** is **adTypeBinary**.</span></span>


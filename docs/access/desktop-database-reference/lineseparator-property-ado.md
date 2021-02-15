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
# <a name="lineseparator-property-ado"></a><span data-ttu-id="50c55-102">Свойство LineSeparator (ADO)</span><span class="sxs-lookup"><span data-stu-id="50c55-102">LineSeparator property (ADO)</span></span>


<span data-ttu-id="50c55-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50c55-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50c55-104">Указывает двоичный символ, который будет использоваться в качестве различиватора линии в текстовых [объектах Stream.](stream-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="50c55-104">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="50c55-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="50c55-105">Settings and return values</span></span>

<span data-ttu-id="50c55-106">Задает или возвращает [значение LineSeparatorsEnum,](lineseparatorsenum.md) которое указывает знак разлиения строки, используемый в **Stream.**</span><span class="sxs-lookup"><span data-stu-id="50c55-106">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**.</span></span> <span data-ttu-id="50c55-107">Значение по умолчанию **— adCRLF.**</span><span class="sxs-lookup"><span data-stu-id="50c55-107">The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="50c55-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="50c55-108">Remarks</span></span>

<span data-ttu-id="50c55-109">**LineSeparator** используется для интерпретации строк при чтении содержимого текстового **потока.**</span><span class="sxs-lookup"><span data-stu-id="50c55-109">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**.</span></span> <span data-ttu-id="50c55-110">Строки можно пропустить с помощью метода [SkipLine.](skipline-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="50c55-110">Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="50c55-111">**LineSeparator** используется только с текстовыми объектами **Stream** ([Тип](type-property-ado-stream.md) **adTypeText).**</span><span class="sxs-lookup"><span data-stu-id="50c55-111">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span> <span data-ttu-id="50c55-112">Это свойство игнорируется, **если type** **— adTypeBinary.**</span><span class="sxs-lookup"><span data-stu-id="50c55-112">This property is ignored if **Type** is **adTypeBinary**.</span></span>


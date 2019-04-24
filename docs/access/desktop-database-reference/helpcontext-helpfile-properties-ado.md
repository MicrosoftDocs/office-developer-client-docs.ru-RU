---
title: Свойства HelpContext, HelpFile (ADO)
TOCTitle: HelpContext, HelpFile properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c90fee6b8525ab13c8a294f9b39c52c20f580a62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291994"
---
# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="27606-102">Свойства HelpContext, HelpFile (ADO)</span><span class="sxs-lookup"><span data-stu-id="27606-102">HelpContext, HelpFile properties (ADO)</span></span>

<span data-ttu-id="27606-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="27606-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="27606-104">Указывает файл справки и раздел, связанный с объектом [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="27606-104">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

## <a name="return-values"></a><span data-ttu-id="27606-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="27606-105">Return values</span></span>

- <span data-ttu-id="27606-106">**HelpContextID** — возвращает идентификатор контекста в виде длинного \*\*\*\* значения для раздела в файле справки.</span><span class="sxs-lookup"><span data-stu-id="27606-106">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

- <span data-ttu-id="27606-107">**HelpFile** — возвращает **строковое** значение, которое оценивается как полностью разрешенный путь к файлу справки.</span><span class="sxs-lookup"><span data-stu-id="27606-107">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>

## <a name="remarks"></a><span data-ttu-id="27606-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="27606-108">Remarks</span></span>

<span data-ttu-id="27606-109">Если в свойстве **HelpFile** указан файл справки, свойство **HelpContext** используется для автоматического отображения раздела справки, который он идентифицирует.</span><span class="sxs-lookup"><span data-stu-id="27606-109">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies.</span></span> <span data-ttu-id="27606-110">Если подходящий раздел справки отсутствует, свойство **HelpContext** возвращает ноль, а свойство **HelpFile** возвращает строку нулевой длины ("").</span><span class="sxs-lookup"><span data-stu-id="27606-110">If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>


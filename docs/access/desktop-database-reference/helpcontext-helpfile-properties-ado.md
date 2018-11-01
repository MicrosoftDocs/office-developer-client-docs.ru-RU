---
title: Свойства HelpContext, HelpFile (ADO)
TOCTitle: HelpContext, HelpFile properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: a9ad8c700b0b0ae293683f7b79062a0edf7775f9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881372"
---
# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="92e3e-102">Свойства HelpContext, HelpFile (ADO)</span><span class="sxs-lookup"><span data-stu-id="92e3e-102">HelpContext, HelpFile properties (ADO)</span></span>

<span data-ttu-id="92e3e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="92e3e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="92e3e-104">Указывает файл справки и раздел, связанный с объектом [Ошибка](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="92e3e-104">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

## <a name="return-values"></a><span data-ttu-id="92e3e-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="92e3e-105">Return values</span></span>

- <span data-ttu-id="92e3e-106">**HelpContextID** — возвращает идентификатор контекста, как **длинное целое** значение, для раздела в файле справки.</span><span class="sxs-lookup"><span data-stu-id="92e3e-106">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

- <span data-ttu-id="92e3e-107">**Файл справки** — возвращает **строковое** значение, которое оценивается как полностью разрешенный путь к файлу справки.</span><span class="sxs-lookup"><span data-stu-id="92e3e-107">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>

## <a name="remarks"></a><span data-ttu-id="92e3e-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="92e3e-108">Remarks</span></span>

<span data-ttu-id="92e3e-109">Если в свойство **HelpFile** указан файл справки, свойство **HelpContext** используется для отображения раздела справки, он определяет автоматически.</span><span class="sxs-lookup"><span data-stu-id="92e3e-109">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies.</span></span> <span data-ttu-id="92e3e-110">Если нет ни один соответствующий раздел справки, свойство **HelpContext** возвращает нуль и свойство **HelpFile** возвращает строку нулевой длины (»»).</span><span class="sxs-lookup"><span data-stu-id="92e3e-110">If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>


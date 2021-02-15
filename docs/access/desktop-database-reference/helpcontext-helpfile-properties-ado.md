---
title: Свойства HelpContext и HelpFile (ADO)
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
# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="04342-102">Свойства HelpContext и HelpFile (ADO)</span><span class="sxs-lookup"><span data-stu-id="04342-102">HelpContext, HelpFile properties (ADO)</span></span>

<span data-ttu-id="04342-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04342-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04342-104">Указывает файл справки и раздел, связанный с [объектом Error.](error-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="04342-104">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

## <a name="return-values"></a><span data-ttu-id="04342-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="04342-105">Return values</span></span>

- <span data-ttu-id="04342-106">**HelpContextID** — возвращает контекстный ИД в качестве значения **Long** для раздела в файле справки.</span><span class="sxs-lookup"><span data-stu-id="04342-106">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

- <span data-ttu-id="04342-107">**HelpFile** — возвращает **строку,** которая оценивается в полностью разрешенный путь к файлу справки.</span><span class="sxs-lookup"><span data-stu-id="04342-107">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>

## <a name="remarks"></a><span data-ttu-id="04342-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="04342-108">Remarks</span></span>

<span data-ttu-id="04342-109">Если файл справки указан в свойстве **HelpFile,** свойство **HelpContext** используется для автоматического отображения идентифицируемого раздела справки.</span><span class="sxs-lookup"><span data-stu-id="04342-109">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies.</span></span> <span data-ttu-id="04342-110">Если соответствующий раздел справки не доступен, свойство **HelpContext** возвращает ноль, а **свойство HelpFile** возвращает строку нулевой длины ("").</span><span class="sxs-lookup"><span data-stu-id="04342-110">If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>


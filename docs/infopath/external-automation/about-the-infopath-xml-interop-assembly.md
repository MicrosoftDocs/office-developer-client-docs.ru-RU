---
title: Сведения о сборке XML-межсоедомения InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- msxml interop [infopath 2007],InfoPath 2007, XML primary interop assembly,InfoPath XML interop assembly
localization_priority: Normal
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: Сборка взаимодействия XML InfoPath предоставляется для обеспечения поддержки взаимодействия между управляемым кодом и COM-сервером, предоставляемым MSXML (MSXML) из внешних приложений, которые автоматизуют InfoPath.
ms.openlocfilehash: 8d47fb58c5133fa14ac78aa8fb29278b70c26abb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303782"
---
# <a name="about-the-infopath-xml-interop-assembly"></a><span data-ttu-id="b93c4-104">Сведения о сборке XML-межсоедомения InfoPath</span><span class="sxs-lookup"><span data-stu-id="b93c4-104">About the InfoPath XML interop assembly</span></span>

<span data-ttu-id="b93c4-105">Сборка взаимодействия XML InfoPath предоставляется для обеспечения поддержки взаимодействия между управляемым кодом и COM-сервером, предоставляемым MSXML (MSXML) из внешних приложений, которые автоматизуют InfoPath.</span><span class="sxs-lookup"><span data-stu-id="b93c4-105">The InfoPath XML interop assembly is provided to allow support for interoperability between managed code and the COM server exposed by Microsoft XML Core Services (MSXML) from external applications that automate InfoPath.</span></span>

<span data-ttu-id="b93c4-106">Параметр **поддержки программируемости .NET** в программе установки InfoPath устанавливает три сборки межпрограммного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="b93c4-106">The **.NET Programmability Support** option in the InfoPath setup program installs three interop assemblies.</span></span> <span data-ttu-id="b93c4-107">Сборки взаимодействия представляют собой сборки .NET, которые служат "мостом" между управляемым и неуправляемым кодами, сопоставляя элементы COM-объекта эквивалентным управляемым элементам .NET.</span><span class="sxs-lookup"><span data-stu-id="b93c4-107">Interop assemblies are .NET assemblies that act as a bridge between managed and unmanaged code, mapping COM object members to equivalent .NET managed members.</span></span> <span data-ttu-id="b93c4-108">Одна из этих сборок, Microsoft.Office.Interop.InfoPath.Xml.dll, предоставляет члены пространства имен [Microsoft.Office.Interop.InfoPath.Xml, ](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external) которое используется для работы с членами, которые предоставляет com-сервер для MSXML (MSXML) из внешних приложений, которые автоматизуют InfoPath с помощью управляемого кода.</span><span class="sxs-lookup"><span data-stu-id="b93c4-108">One of those assemblies, Microsoft.Office.Interop.InfoPath.Xml.dll, provides the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external) namespace, which is used to work with members exposed by the COM server for Microsoft XML Core Services (MSXML) from external applications that automate InfoPath using managed code.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b93c4-109">Ссылки на сборки Microsoft.Office.Interop.InfoPath.dll и Microsoft.Office.Interop.InfoPath.Xml.dll, необходимые для внешних проектов автоматизации InfoPath, необходимо установить вручную.</span><span class="sxs-lookup"><span data-stu-id="b93c4-109">The references to the Microsoft.Office.Interop.InfoPath.dll and Microsoft.Office.Interop.InfoPath.Xml.dll interop assemblies that are required for InfoPath external automation projects must be established manually.</span></span> <span data-ttu-id="b93c4-110">Дополнительные сведения о внешней автоматизации см. в примерах и сценариях внешней [автоматизации.](external-automation-scenarios-and-examples.md)</span><span class="sxs-lookup"><span data-stu-id="b93c4-110">For more information on external automation, see [External Automation Scenarios and Examples](external-automation-scenarios-and-examples.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b93c4-111">См. также</span><span class="sxs-lookup"><span data-stu-id="b93c4-111">See also</span></span>

- [<span data-ttu-id="b93c4-112">Работа с MSXML и System.Xml с использованием объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="b93c4-112">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)


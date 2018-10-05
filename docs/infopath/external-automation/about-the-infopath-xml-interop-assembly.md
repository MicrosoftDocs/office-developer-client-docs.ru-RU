---
title: О сборке взаимодействия InfoPath XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- MSXML взаимодействия [infopath 2007] InfoPath 2007, основной сборки взаимодействия XML, сборки взаимодействия InfoPath XML
localization_priority: Normal
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: Сборки взаимодействия InfoPath XML предоставляется для поддержки для взаимодействия между управляемым кодом и сервером COM, предоставляемые с Microsoft XML Core Services (MSXML) из внешних приложений, которые автоматизируют InfoPath.
ms.openlocfilehash: 8d47fb58c5133fa14ac78aa8fb29278b70c26abb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386826"
---
# <a name="about-the-infopath-xml-interop-assembly"></a><span data-ttu-id="12a7b-104">О сборке взаимодействия InfoPath XML</span><span class="sxs-lookup"><span data-stu-id="12a7b-104">About the InfoPath XML interop assembly</span></span>

<span data-ttu-id="12a7b-105">Сборки взаимодействия InfoPath XML предоставляется для поддержки для взаимодействия между управляемым кодом и сервером COM, предоставляемые с Microsoft XML Core Services (MSXML) из внешних приложений, которые автоматизируют InfoPath.</span><span class="sxs-lookup"><span data-stu-id="12a7b-105">The InfoPath XML interop assembly is provided to allow support for interoperability between managed code and the COM server exposed by Microsoft XML Core Services (MSXML) from external applications that automate InfoPath.</span></span>

<span data-ttu-id="12a7b-106">Параметр **Поддержка программирования .NET** в программе установки InfoPath устанавливает трех сборок взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="12a7b-106">The **.NET Programmability Support** option in the InfoPath setup program installs three interop assemblies.</span></span> <span data-ttu-id="12a7b-107">Сборки взаимодействия представляют собой сборки .NET, которые служат "мостом" между управляемым и неуправляемым кодами, сопоставляя элементы COM-объекта эквивалентным управляемым элементам .NET.</span><span class="sxs-lookup"><span data-stu-id="12a7b-107">Interop assemblies are .NET assemblies that act as a bridge between managed and unmanaged code, mapping COM object members to equivalent .NET managed members.</span></span> <span data-ttu-id="12a7b-108">Один из этих сборок Microsoft.Office.Interop.InfoPath.Xml.dll, предоставляет члены пространства имен [Microsoft.Office.Interop.InfoPath.Xml](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external) , который используется для работы с члены, предоставляемые сервером COM для Microsoft XML Core Services (MSXML) из внешних приложений, который автоматизации InfoPath с помощью управляемого кода.</span><span class="sxs-lookup"><span data-stu-id="12a7b-108">One of those assemblies, Microsoft.Office.Interop.InfoPath.Xml.dll, provides the members of the [Microsoft.Office.Interop.InfoPath.Xml](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external) namespace, which is used to work with members exposed by the COM server for Microsoft XML Core Services (MSXML) from external applications that automate InfoPath using managed code.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="12a7b-109">Ссылки на Microsoft.Office.Interop.InfoPath.dll и Microsoft.Office.Interop.InfoPath.Xml.dll сборки взаимодействия, которые необходимы для внешней автоматизации InfoPath проектов необходимо установить вручную.</span><span class="sxs-lookup"><span data-stu-id="12a7b-109">The references to the Microsoft.Office.Interop.InfoPath.dll and Microsoft.Office.Interop.InfoPath.Xml.dll interop assemblies that are required for InfoPath external automation projects must be established manually.</span></span> <span data-ttu-id="12a7b-110">Дополнительные сведения о внешней автоматизации видеть [внешней автоматизации сценарии и примеры](external-automation-scenarios-and-examples.md).</span><span class="sxs-lookup"><span data-stu-id="12a7b-110">For more information on external automation, see [External Automation Scenarios and Examples](external-automation-scenarios-and-examples.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="12a7b-111">См. также</span><span class="sxs-lookup"><span data-stu-id="12a7b-111">See also</span></span>

- [<span data-ttu-id="12a7b-112">Работа с MSXML и System.Xml с использованием объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="12a7b-112">Working with MSXML and System.Xml Using the InfoPath 2003 Object Model</span></span>](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)


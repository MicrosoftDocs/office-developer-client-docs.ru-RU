---
title: Об сборке интероп-сборки XML InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- msxml interop [infopath 2007], InfoPath 2007, XML основная сборка интеропов, сборка интероп-сборки XML InfoPath
localization_priority: Normal
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: Сборка интеропопов InfoPath XML предоставляется для обеспечения поддержки взаимодействия между управляемым кодом и сервером COM, MSXML (MSXML) от внешних приложений, которые автоматизуют InfoPath.
ms.openlocfilehash: 8d47fb58c5133fa14ac78aa8fb29278b70c26abb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303782"
---
# <a name="about-the-infopath-xml-interop-assembly"></a>Об сборке интероп-сборки XML InfoPath

Сборка интеропопов InfoPath XML предоставляется для обеспечения поддержки взаимодействия между управляемым кодом и сервером COM, MSXML (MSXML) от внешних приложений, которые автоматизуют InfoPath.

Параметр **.NET Programmability Support** в программе установки InfoPath устанавливает три сборки межоперативов. Сборки взаимодействия представляют собой сборки .NET, которые служат "мостом" между управляемым и неуправляемым кодами, сопоставляя элементы COM-объекта эквивалентным управляемым элементам .NET. Одна из этих сборк, Microsoft.Office.Interop.InfoPath.Xml.dll, предоставляет членам [пространства именMicrosoft.Office.Interop.InfoPath.Xml,](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external) которое используется для работы с участниками, подвергшимися воздействию com-сервера для MSXML (MSXML) из внешних приложений, которые автоматизуют InfoPath с помощью управляемого кода. 
  
> [!NOTE]
> Ссылки на сборки Microsoft.Office.Interop.InfoPath.dll Microsoft.Office.Interop.InfoPath.Xml.dll, необходимые для проектов внешней автоматизации InfoPath, необходимо установить вручную. Дополнительные сведения о внешней автоматизации см. в [статьи Внешние сценарии автоматизации и примеры.](external-automation-scenarios-and-examples.md) 
  
## <a name="see-also"></a>См. также

- [Работа с MSXML и System.Xml с использованием объектной модели InfoPath 2003](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)


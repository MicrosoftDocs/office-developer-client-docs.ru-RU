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
# <a name="about-the-infopath-xml-interop-assembly"></a>О сборке взаимодействия InfoPath XML

Сборки взаимодействия InfoPath XML предоставляется для поддержки для взаимодействия между управляемым кодом и сервером COM, предоставляемые с Microsoft XML Core Services (MSXML) из внешних приложений, которые автоматизируют InfoPath.

Параметр **Поддержка программирования .NET** в программе установки InfoPath устанавливает трех сборок взаимодействия. Сборки взаимодействия представляют собой сборки .NET, которые служат "мостом" между управляемым и неуправляемым кодами, сопоставляя элементы COM-объекта эквивалентным управляемым элементам .NET. Один из этих сборок Microsoft.Office.Interop.InfoPath.Xml.dll, предоставляет члены пространства имен [Microsoft.Office.Interop.InfoPath.Xml](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external) , который используется для работы с члены, предоставляемые сервером COM для Microsoft XML Core Services (MSXML) из внешних приложений, который автоматизации InfoPath с помощью управляемого кода. 
  
> [!NOTE]
> Ссылки на Microsoft.Office.Interop.InfoPath.dll и Microsoft.Office.Interop.InfoPath.Xml.dll сборки взаимодействия, которые необходимы для внешней автоматизации InfoPath проектов необходимо установить вручную. Дополнительные сведения о внешней автоматизации видеть [внешней автоматизации сценарии и примеры](external-automation-scenarios-and-examples.md). 
  
## <a name="see-also"></a>См. также

- [Работа с MSXML и System.Xml с использованием объектной модели InfoPath 2003](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)


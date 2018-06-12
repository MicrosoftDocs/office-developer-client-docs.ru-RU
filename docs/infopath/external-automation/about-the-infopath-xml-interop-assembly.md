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
ms.openlocfilehash: 8d3fb1c1de141fe23c655e82b77d83a8e2b11abd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807368"
---
# <a name="about-the-infopath-xml-interop-assembly"></a>О сборке взаимодействия InfoPath XML

Сборки взаимодействия InfoPath XML предоставляется для поддержки для взаимодействия между управляемым кодом и сервером COM, предоставляемые с Microsoft XML Core Services (MSXML) из внешних приложений, которые автоматизируют InfoPath.

Параметр **Поддержка программирования .NET** в программе установки InfoPath устанавливает трех сборок взаимодействия. Сборки взаимодействия представляют собой сборки .NET, которые служат "мостом" между управляемым и неуправляемым кодами, сопоставляя элементы COM-объекта эквивалентным управляемым элементам .NET. Один из этих сборок Microsoft.Office.Interop.InfoPath.Xml.dll, предоставляет члены пространства имен [Microsoft.Office.Interop.InfoPath.Xml](https://msdn.microsoft.com/en-us/library/microsoft.office.interop.infopath.xml) , который используется для работы с члены, предоставляемые сервером COM для Microsoft XML Core Services (MSXML) из внешних приложений, который автоматизации InfoPath с помощью управляемого кода. 
  
> [!NOTE]
> Ссылки на Microsoft.Office.Interop.InfoPath.dll и Microsoft.Office.Interop.InfoPath.Xml.dll сборки взаимодействия, которые необходимы для внешней автоматизации InfoPath проектов необходимо установить вручную. Дополнительные сведения о внешней автоматизации видеть [внешней автоматизации сценарии и примеры](external-automation-scenarios-and-examples.md). 
  
## <a name="see-also"></a>См. также

- [Работа с MSXML и System.Xml с использованием объектной модели InfoPath 2003](http://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)


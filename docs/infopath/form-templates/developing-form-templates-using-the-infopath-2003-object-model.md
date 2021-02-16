---
title: Разработка шаблонов форм с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- form templates [infopath 2007], using infopath 2003 object model,InfoPath 2003-compatible form templates,InfoPath 2007, developing form templates using InfoPath 2003 object model,object models [InfoPath 2003], developing managed code form templates
localization_priority: Normal
ms.assetid: c74cbcd0-4fe6-4eb7-a05c-f61e1868c42b
description: Приложение Microsoft InfoPath по-прежнему поддерживает проекты шаблонов форм, созданные с помощью набора инструментов Microsoft Office InfoPath 2003 для Visual Studio .NET или с помощью набора инструментов Visual Studio 2005 для системы Microsoft Office, использующих бизнес-логику, написанную с применением элементов пространства имен Microsoft.Office.Interop.InfoPath.SemiTrust . В темах этого раздела типы и члены этого пространства имен упоминаются как объектная модель, совместимая с InfoPath 2003, или просто объектная модель InfoPath 2003. InfoPath также поддерживает проекты шаблонов форм, созданные с помощью Microsoft Office InfoPath 2007 с использованием объектной модели, совместимой с InfoPath 2003. Кроме того, InfoPath можно использовать для создания новых проектов шаблонов форм с применением объектной модели, совместимой с InfoPath 2003, чтобы сохранить обратную совместимость для пользователей Office InfoPath 2007. Все темы этого раздела посвящены созданию и разработке шаблонов форм, работающих с объектной моделью, совместимой с InfoPath 2003 и предоставляемой пространством имен Microsoft.Office.Interop.InfoPath.SemiTrust .
ms.openlocfilehash: a39f921f6c7465dbcf469062b866c808fa222851
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300366"
---
# <a name="developing-form-templates-using-the-infopath-2003-object-model"></a>Разработка шаблонов форм с помощью объектной модели InfoPath 2003

Приложение Microsoft InfoPath по-прежнему поддерживает проекты шаблонов форм, созданные с помощью набора инструментов Microsoft Office InfoPath 2003 для Visual Studio .NET или с помощью набора инструментов Visual Studio 2005 для системы Microsoft Office, использующих бизнес-логику, написанную с применением элементов пространства имен [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . В темах этого раздела типы и члены этого пространства имен упоминаются как объектная модель, совместимая с InfoPath 2003, или просто объектная модель InfoPath 2003. InfoPath также поддерживает проекты шаблонов форм, созданные с помощью Microsoft Office InfoPath 2007 с использованием объектной модели, совместимой с InfoPath 2003. Кроме того, InfoPath можно использовать для создания новых проектов шаблонов форм с применением объектной модели, совместимой с InfoPath 2003, чтобы сохранить обратную совместимость для пользователей Office InfoPath 2007. Все темы этого раздела посвящены созданию и разработке шаблонов форм, работающих с объектной моделью, совместимой с InfoPath 2003 и предоставляемой пространством имен [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) . 
  
> [!IMPORTANT]
> [!Важно!] Хотя создание бизнес-логики с помощью объектной модели с управляемым кодом, предоставляемой пространством имен [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) , по-прежнему поддерживается в InfoPath, бизнес-логика, написанная с применением этой объектной модели, не поддерживается для шаблонов форм с поддержкой веб-браузера, развернутых в Microsoft SharePoint Server 2010 с InfoPath Forms Services. Шаблоны форм с поддержкой веб-браузера должны использовать новую объектную модель InfoPath с управляемым кодом, которая предоставляется элементами пространства имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) для настраиваемой бизнес-логики. Дополнительные сведения по созданию шаблонов форм с бизнес-логикой, написанной с применением элементов пространства имен [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , см. в статье [Разработка шаблонов форм InfoPath с кодом](developing-infopath-form-templates-with-code.md). > Кроме того, обратите внимание на то, что для пользователей шаблонов форм, скомпилированных с помощью набора Visual Studio 2012, необходимо наличие установленной платформы Microsoft .NET Framework 2.0 или более поздней версии. Для пользователей шаблонов форм, скомпилированных с помощью Visual Studio .NET 2003, требуется только платформа Microsoft .NET Framework. 1.1. 
  
## <a name="in-this-section"></a>В этом разделе:

[Начало разработки шаблонов форм с помощью объектной модели InfoPath 2003](get-started-developing-form-templates-using-infopath-object-model.md)
  
> Предоставляются общие сведения о создании шаблонов форм с управляемым кодом, которые работают с объектной моделью, совместимой с InfoPath 2003.
    
[Создание шаблонов форм с помощью объектной модели InfoPath 2003](creating-form-templates-using-the-infopath-2003-object-model.md)
  
> Описывается инициализация и очистка кода, добавление обработчиков событий, отладка и развертывание шаблонов форм с управляемым кодом, поддержка потоков и работа со службами MSXML из решений InfoPath с управляемым кодом.
    
[Безопасность шаблонов форм InfoPath с кодом](security-in-infopath-form-templates-with-code.md)
  
> Описывается модель безопасности для шаблонов форм InfoPath, использующих управляемый код, отладка шаблонов форм InfoPath с полным доверием, а также соответствующие процедуры безопасности.
    
[Ознакомление с объектной моделью InfoPath 2003](understanding-the-infopath-2003-object-model.md)
  
> Описывается объектная модель, совместимая с InfoPath 2003, и типичные задачи программирования для шаблонов форм с управляемым кодом, работающих с этой объектной моделью.
    
[Устранение неполадок шаблонов форм, которые используют объектную модель InfoPath 2003](troubleshoot-form-templates-that-use-infopath-object-model.md)
  
> Представляет советы по решению типичных проблем, которые могут обнаружиться при создании шаблонов форм с управляемым кодом, работающих с объектной моделью, совместимой с InfoPath 2003.
    
## <a name="related-sections"></a>Связанные разделы

[Портал разработчиков InfoPath](https://go.microsoft.com/fwlink?LinkID=11689)
  
> Содержит ссылки на технические статьи, примеры кода, загрузки, поддержку и другую документацию MSDN по построению настраиваемых решений InfoPath.
    
[Центр разработчика Microsoft Office](https://go.microsoft.com/fwlink?LinkID=27128)
  
> Содержит ссылки на технические статьи, примеры кода, загрузки, поддержку и другую документацию MSDN по построению настраиваемых решений Office.
    


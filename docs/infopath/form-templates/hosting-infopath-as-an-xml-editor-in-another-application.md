---
title: Размещение InfoPath как редактора XML в другом приложении
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: Среда редактирования форм Microsoft InfoPath может быть настроена в пользовательском приложении для Windows, что позволяет разработчикам интегрировать среду редактирования форм InfoPath в бизнес-приложения.
ms.openlocfilehash: b85e47d506b17982bb883c9d56ea13131807d1cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422581"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a>Размещение InfoPath как редактора XML в другом приложении

Среда редактирования форм Microsoft InfoPath может быть настроена в пользовательском приложении для Windows. Эта функция позволяет разработчикам интегрировать среду редактирования форм InfoPath в бизнес-приложения. Разработчики, записывающие традиционные приложения на основе COM, могут использовать объект **InfoPathEditorObject,** доступный с помощью ссылки на IPEDITOR.DLL, и разработчики, написав Корпорацию Майкрософт. Приложения на основе NET могут использовать сборку **Microsoft.Office.InfoPath.FormControl,** которая предоставляет управляемые типы на основе интерфейса COM. Сборки IPEDITOR.DLL **Microsoft.Office.InfoPath.FormControl** установлены вместе с InfoPath в папке C:\Program Files\Microsoft Office\Office15 или C:\Program Files (x86)\Microsoft Office\Office15. 
  
Статья MSDN, в которой размещена среда редактирования форм InfoPath 2007 в настраиваемом приложении формы Windows, посвящена **объекту FormControl** и его включению в настраиваемый . Приложения на основе NET. В загружаемом файле, связанным с данной статьей, содержится настраиваемое приложение с функциями технологии .NET по замене среды изменения форм InfoPath за счет использования **IOleCommandTargets** COM.
  


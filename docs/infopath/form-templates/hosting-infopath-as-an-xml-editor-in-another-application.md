---
title: Размещение InfoPath как редактора XML в другом приложении
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: Среды редактирования форм Microsoft InfoPath могут размещаться в пользовательском приложении Windows позволяет разработчикам интегрировать редактора в бизнес приложениях форм InfoPath.
ms.openlocfilehash: dd87cba7219b5647bd2b20dd67c6eb0f1811cc59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807480"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a>Размещение InfoPath как редактора XML в другом приложении

Среды редактирования форм Microsoft InfoPath могут размещаться в пользовательском приложении Windows. Эта функция позволяет разработчикам интегрировать редактора в бизнес приложениях форм InfoPath. Разработчики традиционных приложений на базе COM можно использовать объект **InfoPathEditorObject** , который доступен с учетом IPEDITOR. DLL-Библиотека, а разработчики Майкрософт. NET-приложений можно использовать сборку **Microsoft.Office.InfoPath.FormControl** , которая предоставляет управляемых типов, на основе интерфейса COM. IPEDITOR. DLL-Библиотеку и сборки **Microsoft.Office.InfoPath.FormControl** устанавливаются вместе с InfoPath в C:\Program Files\Microsoft Office\Office15 или папка C:\Program Files (x86) \Microsoft Office\Office15. 
  
Статья MSDN, размещение среды редактирования форм InfoPath 2007 в пользовательском приложении формы Windows, в центре внимания объект **FormControl** и как включить в пользовательских. NET-приложениях. В загружаемом файле, связанным с данной статьей, содержится настраиваемое приложение с функциями технологии .NET по замене среды изменения форм InfoPath за счет использования **IOleCommandTargets** COM.
  


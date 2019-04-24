---
title: Размещение InfoPath как редактора XML в другом приложении
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ae24b317-f486-763a-7009-e32c5cb85b59
description: Среда редактирования форм Microsoft InfoPath может быть размещена в пользовательском приложении Windows, что позволяет разработчикам интегрировать среду редактирования форм InfoPath в бизнес-приложения.
ms.openlocfilehash: b85e47d506b17982bb883c9d56ea13131807d1cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303691"
---
# <a name="hosting-infopath-as-an-xml-editor-in-another-application"></a>Размещение InfoPath как редактора XML в другом приложении

Среда редактирования форм Microsoft InfoPath может быть размещена в пользовательском приложении Windows. Эта функция позволяет разработчикам интегрировать среду редактирования форм InfoPath в бизнес-приложения. Разработчики традиционных приложений на основе COM могут использовать объект **инфопаседиторобжект** , который можно использовать для создания ссылки на ипедитор. DLL и разработчики, пишущие Майкрософт. NET-приложения могут использовать сборку **Microsoft. Office. InfoPath. формконтрол** , которая предоставляет управляемые типы на основе интерфейса COM. ИПЕДИТОР. Сборки DLL и **Microsoft. Office. InfoPath. формконтрол** устанавливаются вместе с InfoPath в папке C:\Program Files\Microsoft Office\Office15 или C:\Program Files (x86) \Microsoft Office\Office15. 
  
Статья MSDN, в которой разМещается среда редактирования форм InfoPath 2007 в пользовательском приложении Windows Form, фокусируется на объекте **формконтрол** и о том, как внедрить его в свой собственный. СЕТЕВЫЕ приложения. В загружаемом файле, связанным с данной статьей, содержится настраиваемое приложение с функциями технологии .NET по замене среды изменения форм InfoPath за счет использования **IOleCommandTargets** COM.
  


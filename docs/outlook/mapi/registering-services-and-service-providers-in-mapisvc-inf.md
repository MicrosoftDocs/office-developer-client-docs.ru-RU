---
title: Регистрация служб и поставщиков услуг в MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Last modified: July 18, 2013'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328373"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>Регистрация служб и поставщиков услуг в MapiSvc.inf

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Чтобы установить нового поставщика в системе, необходимо обновить файл MapiSvc.inf, чтобы он был указать на нового поставщика. Стандартные свойства, заданная во время настройки, в том числе следующие, сообщают MAPI, где найти библиотеку динамической компоновки поставщика (DLL):
  
- Этот **PR_SERVICE_DLL_NAME** указан в разделе **[Служба сообщений].** 
    
- Этот **PR_PROVIDER_DLL_NAME** указан в разделе **[Поставщик услуг].** 
    
> [!NOTE]
> Ожидается, что вы установите имя DLL поставщика (без суффикса "32"). Затем MAPI загружает поставщика, ищет его по пути. 
  
## <a name="putting-a-path-in-mapisvcinf"></a>Размещение пути в mapiSvc.inf

Большинство приложений устанавливаются в папке Program Files, что требует обновления переменной пути, чтобы разрешить работу поставщиков MAPI. С помощью нескольких ограничений Microsoft Outlook 2010, русская версия Outlook 2013 могут использовать полные пути к поставщикам MAPI.
  
При регистрации поставщика в MapiSvc.inf можно уложить полный путь к поставщику в свойствах MAPI PR_SERVICE_DLL_NAME и **PR_PROVIDER_DLL_NAME.** 
  
В обоих свойствах полный путь должен быть без суффикса "32", так как MAPI продолжает прикрепить его к имени файла перед поиском файла. Это означает, что если вы зарегистрируете путь "c:\mypath\myprovider.dll", MAPI попытается загрузить "c:\mypath\myprovider32.dll".
  
Так как MAPI Outlook изначально не был разработан для размещения полных путей, для этого вставляется суффикс "32", который ищет первый период в строке, что означает, что пути, содержащие другие точки, не могут работать, поэтому нельзя использовать такие пути, как "c:\my.path\myprovider.dll" или "c:\mypath\my.provider.dll".
  
Иногда в поставщике магазина идентификаторы записей создаются с помощью функции **WrapStoreEntryID,** которая принимает в качестве параметра имя поставщика. 
  
> [!IMPORTANT]
> При использовании полных путей в MapiSvc.inf необходимо использовать тот же путь во всех вызовах **WrapStoreEntryID.** 
  
Кроме того, путь, который вы используете, может быть преобразован в Юникод и из него, используя кодовую страницу, предоставленную функцией [GetACP.](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) 
  
> [!CAUTION]
> Если выбрать путь, содержащий символы, которые не могут выдержать такую прокрутку с помощью функций [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) и [WideCharToMultiByte,](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) будет сбой. 
  
Для демонстрации этой функциональности был изменен пример упакованного [PST-сайта](https://github.com/stephenegriffin/Outlook2010CodeSamples) на GitHub. Эта функциональная возможность находится в **MergeWithMapiSvc** и **GenerateProviderPath.**
  


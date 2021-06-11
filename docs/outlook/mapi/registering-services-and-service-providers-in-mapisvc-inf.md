---
title: Регистрация служб и поставщиков услуг в MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Последнее изменение: 18 июля 2013 г.'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328373"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>Регистрация служб и поставщиков услуг в MapiSvc.inf

 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Установка нового поставщика в системе требует обновления файла MapiSvc.inf, чтобы указать на нового поставщика. Стандартные свойства, заданная во время настройки, включая следующие, информируют MAPI, где найти библиотеку динамических ссылок поставщика (.dll):
  
- Этот **PR_SERVICE_DLL_NAME** указан в разделе **[Служба сообщений].** 
    
- Этот **PR_PROVIDER_DLL_NAME** указан в разделе **[Поставщик услуг].** 
    
> [!NOTE]
> Ожидается, что вы установите имя .dll поставщика (без суффикса "32"). ПОСЛЕ этого MAPI загружает поставщика, ищем его на пути. 
  
## <a name="putting-a-path-in-mapisvcinf"></a>Ввод пути в MapiSvc.inf

Большинство приложений устанавливаются в программных файлах, что требует обновления переменной пути, чтобы разрешить работу поставщиков MAPI. С несколькими ограничениями Microsoft Outlook 2010, русская версия и Outlook 2013 может вместить полные пути к поставщикам MAPI.
  
При регистрации поставщика в MapiSvc.inf можно ввести полный путь к поставщику в свойствах MAPI PR_SERVICE_DLL_NAME **и PR_PROVIDER_DLL_NAME**. 
  
В любом свойстве полный путь должен быть без суффикса "32", так как MAPI продолжает прикрепить его к имени файла перед поиском файла. Это означает, что если вы зарегистрируете путь "c:\mypath\myprovider.dll", MAPI попытается загрузить "c:\mypath\myprovider32.dll".
  
Поскольку mapI Outlook изначально не был разработан для размещения полных путей, он выполняет эту вставку суффикса "32", ища первый период в строке, что означает, что пути, содержащие другие периоды, не могут работать, поэтому вы не можете использовать пути, такие как "c:\my.path\myprovider.dll" или "c:\mypath\my.provider.dll".
  
Иногда в поставщике магазинов вы создаете идентификаторы записей с помощью функции **WrapStoreEntryID,** которая принимает в качестве параметра имя поставщика. 
  
> [!IMPORTANT]
> Если вы используете полные пути в MapiSvc.inf, необходимо использовать тот же путь в любых вызовах **в WrapStoreEntryID.** 
  
Кроме того, путь, который вы используете, может быть преобразован в Юникод и из него с помощью страницы кода, предоставленной функцией [GetACP.](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) 
  
> [!CAUTION]
> При выборе пути, который содержит символы, которые не могут выдержать такой кругооборот с помощью функций [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) и [WideCharToMultiByte,](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) вы испытаете сбой. 
  
Для демонстрации этой функции был пересмотрен пример упакованного [PST](https://github.com/stephenegriffin/Outlook2010CodeSamples) на GitHub - в **MergeWithMapiSvc** и **GenerateProviderPath**.
  


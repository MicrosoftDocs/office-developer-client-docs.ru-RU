---
title: Регистрация служб и поставщиков служб в MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Последнее изменение: 18 июля 2013 г.'
ms.openlocfilehash: 2eb7f1b496e0732b157ea4f9105a0e067329c52f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812113"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>Регистрация служб и поставщиков служб в MapiSvc.inf

 
  
**Относится к**: Outlook 
  
Для установки нового поставщика в системе требуется обновление файла MapiSvc.inf для указания на новый поставщик. Стандартные свойства, установленные во время настройки, которые включают следующие информирование MAPI расположение библиотеки поставщика динамической компоновки (DLL):
  
- **PR_SERVICE_DLL_NAME** , указанного в разделе **[Службы сообщений]** . 
    
- **PR_PROVIDER_DLL_NAME** , указанного в разделе **[Поставщика услуг]** . 
    
> [!NOTE]
> Ожидается, что значение имя вашего поставщика .dll (без суффикс «32»). MAPI загружает ваш поставщик, выполнив поиск по пути. 
  
## <a name="putting-a-path-in-mapisvcinf"></a>Выравнивание пути в MapiSvc.inf

В папке Program Files, обновления в переменную path, чтобы разрешить поставщики MAPI для работы требует установки большинства приложений. С некоторыми ограничениями Microsoft Outlook 2010 и Outlook 2013 позволяет разместить полные пути к поставщики MAPI.
  
При регистрации у поставщика в MapiSvc.inf, можно поместить полный путь к поставщику в разделе свойства MAPI, **PR_SERVICE_DLL_NAME** и **PR_PROVIDER_DLL_NAME**.
  
В любом свойство полный путь должен быть без суффикса «32», так как MAPI по-прежнему производится, добавьте к имени файла перед нужны для файла. Это означает, что при регистрации путь «c:\mypath\myprovider.dll» MAPI попытается загрузить «c:\mypath\myprovider32.dll».
  
Поскольку Outlook MAPI изначально не предназначен для учета полные пути, выполнив поиск первого периода, в строке, которая означает, что пути, содержащие другие периоды не могут работать, поэтому нельзя использовать пути, такие как выполнить этот вставки суффикс «32» «c:\my.path\myprovider.dll» или «c:\mypath\my.provider.dll».
  
В некоторых случаях в хранилище поставщика будет создана идентификаторы записей с помощью функции **WrapStoreEntryID** , который принимает в качестве параметра имя вашего поставщика. 
  
> [!IMPORTANT]
> При использовании полные пути в MapiSvc.inf необходимо использовать тот же путь в вызове **WrapStoreEntryID**. 
  
Кроме того пути, который использован может быть преобразован в Юникод с использованием кодовой страницы, предоставленные функции [GetACP](http://msdn.microsoft.com/en-us/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) и обратно. 
  
> [!CAUTION]
> При выборе пути, который содержит символы, которые не могут выдержать обмен через функции [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) и [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) могут возникнуть сбой. 
  
Для демонстрации эту функцию был обновлен [Пример оболочку PST -файлов](http://ol2010mapisamples.codeplex.com/) на сайте CodePlex - соответствующие функциональные возможности в **MergeWithMapiSvc** и **GenerateProviderPath**.
  


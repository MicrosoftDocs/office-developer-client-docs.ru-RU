---
title: Запуск сеанса MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7935ebed-f252-482c-ad8c-757aa2d8501d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d88ce382b6a6b5f98ec5f88c4deb1565d3b60151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336346"
---
# <a name="starting-a-mapi-session"></a>Запуск сеанса MAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Хотя во время запуска сеанса выполняется значительный объем работы, необходимые задачи минимальны. Большая часть этой работы делается при обработке MAPI вызовов [MAPIInitialize](mapiinitialize.md) и [MAPILogonEx.](mapilogonex.md) Обе эти функции принимают флаги в качестве входных параметров для управления аспектами сеанса, такими как обработка уведомлений и пользовательский интерфейс. Важно понимать последствия установки каждого из этих флагов при вызове **MAPIInitialize** для инициализации библиотек MAPI и **MAPILogonEx** для входа в подсистему MAPI. 
  
 **Запуск сеанса MAPI**
  
1. Вызовите **MAPIInitialize,** чтобы инициализировать стандартный набор библиотек MAPI. 
    
2. Если необходимо использовать библиотеки OLE, вызовите функцию [OLE OleInitialize.](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx)
    
3. Если необходимо использовать библиотеку-сучретарь MAPI, вызовите [ScInitMapiUtil.](scinitmapiutil.md)
    
4. Вызовите **MAPILogonEx** с допустимым профилем, чтобы войти в подсистему MAPI. **MAPILogonEx** проверяет конфигурацию каждого поставщика услуг в службах сообщений, включенных в профиль, и при необходимости запросит у пользователя дополнительные сведения. После **завершения mapILogonEx** настроенные поставщики служб готовы к обслуживанию. 
    
## <a name="in-this-section"></a>В этом разделе:

[Инициализация MAPI](initializing-mapi.md)
  
> Описывается инициализация MAPI для сеанса.
    
[Инициализация OLE для MAPI](initializing-ole-for-mapi.md)
  
> Описывает вызовы, которые необходимо инициализировать OLE для использования с MAPI.
    
[Инициализация utilities MAPI](initializing-the-mapi-utilities.md)
  
> Описывается инициализация utilities MAPI.
    
[Вход в MAPI](logging-on-to-mapi.md)
  
> Описание входа клиентских приложений в подсистему MAPI.
    


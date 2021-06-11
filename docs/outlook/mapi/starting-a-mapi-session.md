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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Несмотря на то, что во время запуска сеанса выполняется значительный объем работы, необходимые задачи минимальны. Большая часть этой работы делается в обработке MAPI вызовов [MAPIInitialize](mapiinitialize.md) и [MAPILogonEx.](mapilogonex.md) Обе эти функции принимают флаги в качестве параметров ввода для управления аспектами сеанса, такими как обработка уведомлений и пользовательский интерфейс. Важно понимать последствия установки каждого из этих флагов при вызове **MAPIInitialize** для инициализации библиотек MAPI и **MAPILogonEx** для входа в подсистему MAPI. 
  
 **Запуск сеанса MAPI**
  
1. Вызов **MAPIInitialize,** чтобы инициализировать стандартный набор библиотек MAPI. 
    
2. Если вам нужно использовать библиотеки OLE, позвоните в OLE-функцию [OleInitialize.](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx)
    
3. Если вам нужно использовать библиотеку утилиты MAPI, позвоните [в ScInitMapiUtil](scinitmapiutil.md).
    
4. Вызов **MAPILogonEx с** допустимым профилем для входа в подсистему MAPI. **MAPILogonEx** проверяет конфигурацию каждого из поставщиков услуг в службах сообщений, включенных в профиль, и, при необходимости, запросит у пользователя дополнительные сведения. После **завершения MAPILogonEx** настроенные поставщики услуг готовы к обслуживанию. 
    
## <a name="in-this-section"></a>В этом разделе

[Инициализация MAPI](initializing-mapi.md)
  
> Описывает инициализацию MAPI для сеанса.
    
[Инициализация OLE для MAPI](initializing-ole-for-mapi.md)
  
> Описывает вызовы, которые необходимо сделать для инициализации OLE для использования с MAPI.
    
[Инициализация утилит MAPI](initializing-the-mapi-utilities.md)
  
> Описывает инициализацию утилит MAPI.
    
[Вход в MAPI](logging-on-to-mapi.md)
  
> Описывает, как клиентские приложения войдите в подсистему MAPI.
    


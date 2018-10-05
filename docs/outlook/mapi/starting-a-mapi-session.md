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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382591"
---
# <a name="starting-a-mapi-session"></a>Запуск сеанса MAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Хотя значительное выполненных во время сеанса запуска работ, необходимых задач минимальны. Большая часть этой работы выполняется в MAPI обработки вызовов [MAPIInitialize](mapiinitialize.md) и [MAPILogonEx](mapilogonex.md) . Обе эти функции принимать флаги в качестве входных параметров для управления аспектов сеанса, таких как обработки уведомлений и пользовательский интерфейс. Важно понять последствия настройки каждой из этих флагов при вызове **MAPIInitialize** для инициализации библиотеки MAPI и **MAPILogonEx** войдите в систему в подсистеме MAPI. 
  
 **Начало сеанса MAPI**
  
1. Вызов **MAPIInitialize** для инициализации стандартный набор библиотек MAPI. 
    
2. Если необходимо использовать библиотек OLE, вызовите функцию OLE [OleInitialize](https://msdn.microsoft.com/library/9a13e7a0-f2e2-466b-98f5-38d5972fa391%28Office.15%29.aspx).
    
3. Если требуется использовать библиотеку служебной программы MAPI, вызовите [ScInitMapiUtil](scinitmapiutil.md).
    
4. Вызов **MAPILogonEx** с допустимого профиля войдите в систему в подсистеме MAPI. **MAPILogonEx** проверяет конфигурацию каждый из поставщиков услуг в службах сообщения, включенные в профиль, запросом для получения дополнительных сведений, если необходимо и возможные. По завершении **MAPILogonEx** поставщиков услуг настроенного готовы для службы. 
    
## <a name="in-this-section"></a>В этой статье

[Инициализация MAPI](initializing-mapi.md)
  
> Описание способов инициализации MAPI для сеанса.
    
[Инициализация OLE для MAPI](initializing-ole-for-mapi.md)
  
> Описание вызовов для выполнения инициализировать OLE для использования с MAPI.
    
[Инициализация служебных программ MAPI](initializing-the-mapi-utilities.md)
  
> Описание способов инициализации MAPI служебных программ.
    
[Вход в MAPI](logging-on-to-mapi.md)
  
> Описывает, как клиентские приложения выполните вход в систему sub MAPI.
    


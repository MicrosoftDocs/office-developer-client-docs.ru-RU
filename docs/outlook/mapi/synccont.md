---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: afba7fa718a35d33966d45289461313e349ef2e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349576"
---
# <a name="synccont"></a>SYNCCONT

**Область применения**: Outlook 2013 | Outlook 2016 
  
Сведения для синхронизации содержимого указанных папок в локальном хранилище с сервером во время [состояния "Синхронизация содержимого](synchronize-contents-state.md)". Это включает только отправку или полную синхронизацию, включающую отправку, а затем загрузку.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct SYNCCONT 
{ 
   ULONG   ulFlags; 
   UINT   iEnt; 
   UINT   cEnt; 
   LPVOID    pvReserved; 
   LPSPropTagArray   ptagaReserved; 
   LPSSortOrderSet   psosReserved; 
};
```

## <a name="members"></a>Элементы

_ulFlags_
  
> возврата Флаги для определения соответствующего поведения во время синхронизации.
    
  - UPC_OK
    
  - возврата Отправка или полная синхронизация выполнена успешно. Клиент устанавливает это после синхронизации информации с сервером.
    
_Иент_
  
> вышли Индекс для отслеживания синхронизации содержимого в количестве папок, заданных с помощью _цента_.
    
_Центов_
  
> вышли Количество реплицируемых папок.
    
_Пвресервед_
  
> Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается. 
    
_Птагаресервед_
  
> Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается. 
    
_Псосресервед_
  
> Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается. 
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [Константы MAPI](mapi-constants.md)


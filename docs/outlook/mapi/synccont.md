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
ms.openlocfilehash: b1ab1bd4eb6badc75065ce54d009e034f0fc2b29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584676"
---
# <a name="synccont"></a>SYNCCONT

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Сведения о синхронизации содержимое указанных папках в локальном хранилище с сервером во время [синхронизации состояние содержимого](synchronize-contents-state.md). Это включает в себя только что отправку пользователями или полную синхронизацию, передаваемых и выберите файл для загрузки.
  
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

## <a name="members"></a>Members

_ulFlags_
  
> [in] Флаги для определения соответствующего поведения при синхронизации.
    
  - UPC_OK
    
  - [in] Отправка или полная синхронизация прошла успешно. Клиент устанавливает это после синхронизация данных с сервером.
    
_iEnt_
  
> [out] Индекс для отслеживания синхронизацию содержимого в поле число папок, указанного идентификатором _централизованной_.
    
_централизованной_
  
> [out] Число папок, которые следует реплицировать.
    
_pvReserved_
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_ptagaReserved_
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_psosReserved_
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [��������� MAPI](mapi-constants.md)


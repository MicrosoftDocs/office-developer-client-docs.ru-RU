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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430408"
---
# <a name="synccont"></a>SYNCCONT

**Относится к**: Outlook 2013 | Outlook 2016 
  
Сведения о синхронизации содержимого указанных папок в локальном хранилище с сервером во время синхронизации [состояния содержимого.](synchronize-contents-state.md) Это включает только отправку или полную синхронизацию с отправкой, а затем скачиванием.
  
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
  
> [in] Флаги для определения соответствующего поведения во время синхронизации.
    
  - UPC_OK
    
  - [in] Отправка или полная синхронизация прошла успешно. Клиент устанавливает это после синхронизации данных с сервером.
    
_iEnt_
  
> [out] Индекс для отслеживания синхронизации содержимого в количестве папок, указанных _cEnt._
    
_cEnt_
  
> [out] Количество реплицируемых папок.
    
_pvReserved_
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_ptagaReserved_
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
_psosReserved_
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [Константы MAPI](mapi-constants.md)


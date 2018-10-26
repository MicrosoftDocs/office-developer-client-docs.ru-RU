---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a1ec71d7120eab220ee3b11d2a751fba51cee48e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592096"
---
# <a name="uphier"></a>UPHIER
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сведения о синхронизации иерархии папок во время [загрузки иерархия состояний](upload-hierarchy-state.md).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a>Элементы

_ulFlags_
  
> [in] Флаги для изменения поведения при синхронизации иерархии папок.
    
  - UPH_OK
    
    - [in] Отправка прошла успешно. Клиент устанавливает это после успешной отправки информации на сервер. После просмотра этот флаг, Outlook удаляет все сведения о внутренней регистрации, который сообщил, что требуется обновление иерархии папок. 
    
    - Клиент передает значение HRESULT, если передача не удалась.
    
_pstmReserved_
  
> [out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.
    
_iEnt_
  
> [out] Индекс для отслеживания синхронизация число папок, указанного идентификатором *централизованной* . 
    
_централизованной_
  
> [out] Число папок, которые не синхронизированы.
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [Константы MAPI](mapi-constants.md)


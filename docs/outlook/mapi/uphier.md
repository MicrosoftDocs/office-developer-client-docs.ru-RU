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
ms.openlocfilehash: 45ef7ce9291376ac020035f0bde6172caf6cc01b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414923"
---
# <a name="uphier"></a>UPHIER
 
**Относится к**: Outlook 2013 | Outlook 2016 
  
Сведения о синхронизации иерархии папок во время состояния [иерархии отправки.](upload-hierarchy-state.md)
  
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
    
    - [in] Отправка прошла успешно. Клиент устанавливает это после успешной отправки сведений на сервер. После просмотра этого флага Outlook очищает все внутренние сведения регистрации, которые указывали на необходимость обновления иерархии папок. 
    
    - Клиент передает HRESULT, если отправка не была успешной.
    
_pstmReserved_
  
> [out] Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.
    
_iEnt_
  
> [out] Индекс для отслеживания синхронизации количества папок, указанных *в cEnt.* 
    
_cEnt_
  
> [out] Количество не синхронизированных папок.
    
## <a name="see-also"></a>См. также

- [Сведения об API репликации](about-the-replication-api.md)
- [Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
- [Константы MAPI](mapi-constants.md)


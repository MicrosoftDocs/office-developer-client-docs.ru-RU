---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3cb110fdcbbd88e494c44ba2ed73cc26674638ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420026"
---
# <a name="mapiofflineadviseinfo"></a>MAPIOFFLINE_ADVISEINFO
 
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет сведения для **[имапиоффлинемгр:: Advise](imapiofflinemgr-advise.md)** для регистрации обратного вызова для автономного объекта. 
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу **имапиоффлинемгр:: Advise**. 
  
```cpp
typedef struct 
{ 
      ULONG                   ulSize; 
      ULONG                   ulClientToken; 
      MAPIOFFLINE_CALLBACK_TYPE     CallbackType; 
      IUnknown*               pCallback; 
      ULONG                   ulAdviseTypes; 
      ULONG                   ulStateMask; 
} MAPIOFFLINE_ADVISEINFO;
```

## <a name="members"></a>Members

_улсизе_: размер **мапиоффлине_адвисеинфо**. 
    
_улклиенттокен_: маркер, определяемый клиентом для обратного вызова. Это член *улклиенттокен* структуры **[мапиоффлине_нотифи](mapioffline_notify.md)** , переданный в **[имапиоффлиненотифи:: notify](imapiofflinenotify-notify.md)**. 
    
_Каллбакктипе_: тип обратного вызова, который требуется выполнить.
    
   -  МАПИОФФЛИНЕ_КАЛЛБАКК_ТИПЕ_НОТИФИ 
    
   - Тип обратного вызова — уведомление. Это единственный поддерживаемый тип обратного вызова.  *пкаллбакк* должен указывать на интерфейс **[имапиоффлиненотифи](imapiofflinenotifyiunknown.md)**. 
    
_пкаллбакк_: интерфейс, используемый для обратного вызова. Это реализация **[имапиоффлиненотифи](imapiofflinenotifyiunknown.md)** клиентом. 
    
_уладвисетипес_: типы уведомлений, определяемые условием для рекомендации. Единственный поддерживаемый тип — МАПИОФФЛИНЕ_АДВИСЕ_ТИПЕ_СТАТЕЧАНЖЕ.
    
_улстатемаск_: единственное поддерживаемое состояние — мапиоффлине_стате_алл.
    
## <a name="see-also"></a>См. также

- [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)
- [Об API автономного режима](about-the-offline-state-api.md) 
- [��������� MAPI](mapi-constants.md) 
- [MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)


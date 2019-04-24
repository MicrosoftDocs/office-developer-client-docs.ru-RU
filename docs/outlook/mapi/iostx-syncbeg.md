---
title: Иосткссинкбег
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncBeg
api_type:
- COM
ms.assetid: 4a935df3-98c4-2742-206e-4e16eda7b9bc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ae4497295328155780fc5208d1699169698e02d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317173"
---
# <a name="iostxsyncbeg"></a>IOSTX::SyncBeg

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
ПодГотавливает локальное хранилище к синхронизации в определенном состоянии и получает сведения, необходимые для репликации.
  
```cpp
HRESULT SyncBeg( 
    UINT uiSync, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Параметры

 _Уисинк_
  
>  возврата Состояние, которое будет вводить локальное хранилище. Ниже приведен список состояний идентиферс: 
    
ЛР_СИНК_ИДЛЕ
  
> 
    
ЛР_СИНК
  
> 
    
ЛР_СИНК_УПЛОАД_ХИЕРАРЧИ
  
> 
    
ЛР_СИНК_УПЛОАД_ФОЛДЕР
  
> 
    
ЛР_СИНК_КОНТЕНТС
  
> 
    
ЛР_СИНК_УПЛОАД_ТАБЛЕ
  
> 
    
ЛР_СИНК_УПЛОАД_МЕССАЖЕ
  
> 
    
ЛР_СИНК_УПЛОАД_МЕССАЖЕ_РЕАД
  
> 
    
ЛР_СИНК_УПЛОАД_МЕССАЖЕ_ДЕЛ
  
> 
    
ЛР_СИНК_ДОВНЛОАД_ХИЕРАРЧИ
  
> 
    
ЛР_СИНК_ДОВНЛОАД_ТАБЛЕ
  
> 
    
 _ППВ_
  
>  [in]/[out] указатель на структуру данных, соответствующую состоянию, которое необходимо ввести. 
    
[DNHIER](dnhier.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[DNTBL](dntbl.md)
  
> 
    
[Синхр](sync.md)
  
> 
    
[SYNCCONT](synccont.md)
  
> 
    
[UPDEL](updel.md)
  
> 
    
[UPDELE](updele.md)
  
> 
    
[UPFLD](upfld.md)
  
> 
    
[UPHIER](uphier.md)
  
> 
    
[UPMOV](upmov.md)
  
> 
    
[UPMSG](upmsg.md)
  
> 
    
[UPREAD](upread.md)
  
> 
    
[UPREADE](upreade.md)
  
> 
    
[UPTBL](uptbl.md)
  
> 
    
[UPTBLE](uptble.md)
  
> 
    
## <a name="remarks"></a>Замечания

Клиент вызывает **[иосткс:: сетсинкресулт](iostx-setsyncresult.md)** , чтобы задать результат синхронизации, а затем вызывает **[Иосткс:: синценд](iostx-syncend.md)** , чтобы завершить это состояние. Клиент должен вызвать **[иосткс:: синценд](iostx-syncend.md)** для каждого вызова **Иосткс:: синкбег** для определения успешности репликации состояния. После того как это будет определено, Outlook может начать очистку своего внутреннего состояния. 
  
Большая часть этих структур содержит сведения [out]/[in], позволяя Outlook передавать информацию клиенту, а клиент — передавать информацию в Outlook. Когда клиент вызывает **иосткс:: синкбег**, Outlook выделяет структуру данных для определенного состояния и инициализирует ее информацией для этого состояния. Сведения о [выходе]. НаХодясь в состоянии, клиент обновляет соответствующую структуру данных для этого состояния. Это сведения о [in]. 
  
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Константы MAPI](mapi-constants.md)


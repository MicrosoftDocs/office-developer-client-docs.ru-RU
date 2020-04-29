---
title: иосткссинчдрбег
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SyncHdrBeg
api_type:
- COM
ms.assetid: 7f8ca7cf-ac0b-9b77-c1dd-9f1d0871d603
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 49ef9862d5156a1bed242652df32baab9a0123fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405095"
---
# <a name="iostxsynchdrbeg"></a>IOSTX::SyncHdrBeg

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Запускает синхронизацию для заголовка сообщения.
  
```cpp
HRESULT SyncHdrBeg( 
    ULONG cbeid, 
    LPENTRYID lpeid, 
    LPVOID *ppv 
);
```

## <a name="parameters"></a>Параметры

 _кбеид_
  
> возврата Число байтов в ИДЕНТИФИКАТОРе записи сообщения.
    
 _лпеид_
  
> возврата Идентификатор элемента сообщения.
    
 _ппв_
  
>  [in]/[out] указатель на структуру **[хдрсинк](hdrsync.md)** для заголовка сообщения. 
    
## <a name="remarks"></a>Примечания

После **иосткс:: синчдрбег**локальное хранилище переходит в [состояние загрузка заголовка сообщения](download-message-header-state.md). Outlook инициализирует клиентскую структуру **хдрсинк** с текущим представлением заголовка сообщения в хранилище и родительской папке. После этого клиент должен скачать полный элемент сообщения (как *пмсгфулл* в **хдрсинк** ). В случае успешного выполнения клиент также устанавливает *ulFlags* в **хдрсинк** как **HSF_OK**. После **[иосткс:: синчдренд](iostx-synchdrend.md)** Outlook проверяет результат в **хдрсинк** и использует информацию в **хдрсинк** для обновления заголовка локального сообщения. 
  
## <a name="see-also"></a>См. также



[IOSTX::GetLastError](iostx-getlasterror.md)
  
[IOSTX::InitSync](iostx-initsync.md)
  
[IOSTX::SetSyncResult](iostx-setsyncresult.md)
  
[IOSTX::SyncBeg](iostx-syncbeg.md)
  
[IOSTX::SyncEnd](iostx-syncend.md)
  
[IOSTX::SyncHdrEnd](iostx-synchdrend.md)
  
[IOSTX : IUnknown](iostxiunknown.md)


[Константы MAPI](mapi-constants.md)


---
title: RTFSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RTFSync
api_type:
- HeaderDef
ms.assetid: 627f95e9-39ac-4d43-8f02-687783b09785
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dfdf1068caaab3894b1b489d53ccc8debe1b3a29
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436211"
---
# <a name="rtfsync"></a>RTFSync

**Относится к**: Outlook 2013 | Outlook 2016 
  
Убедитесь, что текст сообщения в формате RTF соответствует обычной текстовой версии. Необходимо вызвать эту функцию перед чтением версии RTF и после изменения версии RTF. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения с RTF и поставщики store сообщений  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a>Параметры

_lpMessage_
  
> [in] Указатель на сообщение, которое необходимо обновить.
    
_ulFlags_
  
> [in] Битоваяmas флагов, используемых для сообщения в виде RTF или обычного текста, была изменена. Можно установить следующие флаги:
    
  - RTF_SYNC_BODY_CHANGED: текстовая версия сообщения изменена.
      
  - RTF_SYNC_RTF_CHANGED: версия сообщения в RTF изменена.
    
  Все остальные биты в параметре  _ulFlags_ зарезервированы для будущего использования. 
    
_lpfMessageUpdated_
  
> [out] Указатель на переменную, указывающее, есть ли обновленное сообщение. TRUE, если есть обновленное сообщение, в противном случае FALSE.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Если свойство **PR_RTF_IN_SYNC** ([PidTagRtfInSync)](pidtagrtfinsync-canonical-property.md)отсутствует или имеет false, перед чтением свойства **PR_RTF_COMPRESSED** ([PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)функцию **RTFSync** следует назвать с установленным флагом RTF_SYNC_BODY_CHANGED. 
  
Если флаг STORE_RTF_OK не установлен в свойстве **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask),](pidtagstoresupportmask-canonical-property.md)эту функцию следует использовать с флагом RTF_SYNC_RTF_CHANGED, установленным после изменения **PR_RTF_COMPRESSED.** 
  
Если оба **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) **и PR_RTF_COMPRESSED** были изменены, следует создать функцию **RTFSync** с обоими установленными флагами. 
  
Если для параметра _lpfMessageUpdated_ задано значение TRUE, для сообщения должен быть вызван метод [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Если **saveChanges** не вызван, изменения не будут сохранены в сообщении. 
  
Поставщики rtFSync могут использовать **RTFSync** для синхронизации PR_BODY и **PR_RTF_COMPRESSED** свойств.  
  
Дополнительные сведения см. в документе [Supporting RTF Text for Message Store Providers.](supporting-rtf-text-for-message-store-providers.md) 
  
## <a name="see-also"></a>См. также

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)


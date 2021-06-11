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

**Область применения**: Outlook 2013 | Outlook 2016 
  
Убедитесь, что текст сообщения Rich Text Format (RTF) совпадает с обычной текстовой версией. Необходимо вызвать эту функцию перед чтением версии RTF и после изменения версии RTF. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики магазинов сообщений, осведомленные о RTF  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a>Parameters

_lpMessage_
  
> [in] Указатель на обновленное сообщение.
    
_ulFlags_
  
> [in] Изменена битмаска флагов, используемых для указать RTF или обычную текстовую версию сообщения. Можно установить следующие флаги:
    
  - RTF_SYNC_BODY_CHANGED: обычная текстовая версия сообщения изменилась.
      
  - RTF_SYNC_RTF_CHANGED. Версия сообщения RTF изменилась.
    
  Все остальные биты в параметре  _ulFlags_ зарезервированы для использования в будущем. 
    
_lpfMessageUpdated_
  
> [вышел] Указатель на переменную, указывающее, есть ли обновленное сообщение. TRUE, если есть обновленное сообщение, FALSE в противном случае.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Если **свойство PR_RTF_IN_SYNC** [(PidTagRtfInSync)](pidtagrtfinsync-canonical-property.md)отсутствует или является FALSE, перед чтением свойства **PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)функция **RTFSync** должна быть вызвана с набором флага RTF_SYNC_BODY_CHANGED. 
  
Если флаг STORE_RTF_OK не установлен в **свойстве PR_STORE_SUPPORT_MASK** [(PidTagStoreSupportMask),](pidtagstoresupportmask-canonical-property.md)эта функция должна быть вызвана с набором флага RTF_SYNC_RTF_CHANGED после изменения **PR_RTF_COMPRESSED**. 
  
Если **изменены PR_BODY** [(PidTagBody)](pidtagbody-canonical-property.md)и **PR_RTF_COMPRESSED,** функция **RTFSync** должна быть вызвана с набором флагов. 
  
Если значение параметра _lpfMessageUpdated_ задано значение TRUE, для сообщения должен быть вызван метод [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Если **SaveChanges** не называется, изменения не будут сохранены в сообщении. 
  
Поставщики магазинов сообщений могут использовать **RTFSync** для синхронизации свойств PR_BODY и **PR_RTF_COMPRESSED.**  
  
Дополнительные сведения см. [в документе Поддержка текста RTF для поставщиков магазинов сообщений.](supporting-rtf-text-for-message-store-providers.md) 
  
## <a name="see-also"></a>См. также

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)


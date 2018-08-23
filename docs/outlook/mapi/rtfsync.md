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
ms.openlocfilehash: 706c628241e519642209a271dce62d21b16938e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565741"
---
# <a name="rtfsync"></a>RTFSync

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Следит за тем, что текста сообщения форматированный текст (RTF) соответствует версии обычного текста. Это необходимо для вызова этой функции перед чтением версии RTF и после изменения версии RTF. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Поставщики удаленного хранилища принять во внимание RTF клиентских приложений и сообщения  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a>Параметры

_lpMessage_
  
> [in] Указатель на сообщение, который требуется обновить.
    
_ulFlags_
  
> [in] Битовая маска флагов служит для указания RTF или текстовая версия сообщения, была изменена. Можно задать следующие флажки:
    
  - RTF_SYNC_BODY_CHANGED: Версия обычного текста сообщения, была изменена.
      
  - RTF_SYNC_RTF_CHANGED: Версия RTF сообщения, была изменена.
    
  Все другие биты с помощью параметра _ulFlags_ зарезервированы для использования в будущем. 
    
_lpfMessageUpdated_
  
> [out] Указатель на переменную, указывающее, существует ли обновленные сообщения. Значение TRUE, если сообщение обновленные значение FALSE в противном случае.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Если свойство **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) отсутствует или имеет значение FALSE, перед чтением свойства **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) функция **RTFSync** вызывается с RTF_SYNC_BODY_ ИЗМЕНЕН флаг. 
  
Если флаг STORE_RTF_OK не установлен в свойстве **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), эта функция должна вызываться с флаг RTF_SYNC_RTF_CHANGED после изменения **PR_RTF_COMPRESSED**. 
  
При изменении **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) и **PR_RTF_COMPRESSED** **RTFSync** функция должна вызываться с оба набора флаги. 
  
Если параметр _lpfMessageUpdated_ имеет значение TRUE, метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) должен быть вызван для сообщения. Если **SaveChanges** не вызван, изменения не будут сохранены в сообщении. 
  
Поставщики хранилища сообщений можно использовать **RTFSync** для хранения синхронизацию свойств **PR_BODY** и **PR_RTF_COMPRESSED** . 
  
Для получения дополнительных сведений см [Поддержка текст RTF для поставщиков хранилища сообщений](supporting-rtf-text-for-message-store-providers.md). 
  
## <a name="see-also"></a>См. также

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)


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
  
Убедитесь, что текст сообщения в формате RTF соответствует версии обычного текста. Перед считыванием версии RTF и изменением версии RTF необходимо вызвать эту функцию. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики хранилищ сообщений с поддержкой RTF  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a>Параметры

_лпмессаже_
  
> возврата Указатель на сообщение, которое требуется обновить.
    
_ulFlags_
  
> возврата Битовая маска флагов, используемых для обозначения измененной версии сообщения в формате RTF или обычного текста. Можно задать следующие флаги:
    
  - RTF_SYNC_BODY_CHANGED: изменена текстовая версия сообщения.
      
  - RTF_SYNC_RTF_CHANGED: изменена версия сообщения в формате RTF.
    
  Все остальные биты в параметре _ulFlags_ зарезервированы для последующего использования. 
    
_лпфмессажеупдатед_
  
> вышли Указатель на переменную, указывающую наличие обновленного сообщения. Значение TRUE, если имеется обновленное сообщение, в противном случае — FALSE.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Если свойство **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) отсутствует или имеет значение false, перед чтением свойства **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) необходимо вызвать функцию **ртфсинк** с установленным флагом RTF_SYNC_BODY_CHANGED. 
  
Если флаг STORE_RTF_OK не задан в свойстве **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), эту функцию необходимо вызвать с установленным флагом RTF_SYNC_RTF_CHANGED после изменения **PR_RTF_COMPRESSED**. 
  
Если были изменены как **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), так и **PR_RTF_COMPRESSED** , функция **ртфсинк** должна вызываться с установленными обоими флагами. 
  
Если для параметра _лпфмессажеупдатед_ задано значение true, то для сообщения должен вызываться метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Если параметр **SaveChanges** не вызывается, изменения не будут сохранены в сообщении. 
  
Поставщики хранилищ сообщений могут использовать **ртфсинк** для синхронизации свойств **PR_BODY** и **PR_RTF_COMPRESSED** . 
  
Дополнительную информацию можно узнать в статье [поддержка текста в формате RTF для поставщиков хранилищ сообщений](supporting-rtf-text-for-message-store-providers.md). 
  
## <a name="see-also"></a>См. также

- [WrapCompressedRTFStream](wrapcompressedrtfstream.md)


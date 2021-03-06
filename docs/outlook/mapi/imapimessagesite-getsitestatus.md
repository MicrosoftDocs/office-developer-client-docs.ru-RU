---
title: IMAPIMessageSiteGetSiteStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSiteStatus
api_type:
- COM
ms.assetid: 02718898-7857-4e43-8f46-622269f812e6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ab4a06a20c71943f9b649d8f22377f59223e9717
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430128"
---
# <a name="imapimessagesitegetsitestatus"></a>IMAPIMessageSite::GetSiteStatus

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает сведения с объекта сайта сообщений о возможностях веб-сайта сообщений для текущего сообщения.
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parameters

 _lpulStatus_
  
> [вышел] Указатель на битмаску флагов, которая предоставляет сведения о состоянии сообщения. Можно установить следующие флаги:
    
VCSTATUS_COPY 
  
> Сообщение можно скопировать. 
    
VCSTATUS_DELETE 
  
> Сообщение можно удалить.
    
VCSTATUS_DELETE_IS_MOVE 
  
> При удалении сообщение перемещается в папку **"Удаленные** элементы" в хранилище сообщений вместо немедленного удаления из ее магазина сообщений. 
    
VCSTATUS_MOVE 
  
> Сообщение может быть перемещено.
    
VCSTATUS_NEW_MESSAGE 
  
> Можно создать новое сообщение.
    
VCSTATUS_SAVE 
  
> Сообщение можно сохранить.
    
VCSTATUS_SUBMIT 
  
> Сообщение может быть отправлено.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Объекты формы называют **метод IMAPIMessageSite::GetSiteStatus,** чтобы получить возможности объекта сайта сообщений для текущего сообщения. Флаги, возвращенные в  _параметре lpulStatus,_ предоставляют сведения о сайте сообщения. Как правило, форма включает или отключает команды меню в зависимости от сведений, которые предоставляют флаги о возможностях реализации сайта сообщений. Если новое сообщение загружается в форму методом [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) или методом [IPersistMessage::Load,](ipersistmessage-load.md) необходимо проверить флаги состояния. Некоторые объекты сайта сообщений, особенно объекты только для чтения, не позволяют сохранить или удалить сообщения. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Метод **IMAPIMessageSite::GetSiteStatus** может потребовать от клиентского приложения выполнения некоторых вычислений, чтобы определить, какие операции можно или не могут выполнять в текущем сообщении. Как правило, это включает просмотр строки состояния для поставщика магазина сообщений текущего сообщения или запрос поставщика магазина, чтобы определить, какие действия клиентская заявка может выполнять с помощью магазина сообщений. Например, чтобы определить, следует ли возвращать флаг MAPI_DELETE_IS_MOVE, проверьте свойство  PR_IPM_WASTEBASKET_ENTRYID объекта магазина сообщений[(PidTagIpIpmWastebasketEntryId),](pidtagipmwastebasketentryid-canonical-property.md)  чтобы узнать, есть ли папка удаленных элементов в хранилище сообщений. 
  
Список интерфейсов, связанных с серверами форм, см. в [перечне интерфейсов форм MAPI.](mapi-form-interfaces.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSiteStatus  <br/> |MFCMAPI использует **метод IMAPIMessageSite::GetSiteStatus** для получения состояния указанного сайта. Он может возвращать VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE или VCSTATUS_SUBMIT.  <br/> |
   
## <a name="see-also"></a>См. также



[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[Каноническое свойство PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)


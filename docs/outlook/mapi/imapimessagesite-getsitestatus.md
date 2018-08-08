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
ms.openlocfilehash: 7d81533b13f4f44a0644215e009dc3477717e9a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808969"
---
# <a name="imapimessagesitegetsitestatus"></a>IMAPIMessageSite::GetSiteStatus

  
  
**Относится к**: Outlook 
  
Возвращает сведения из объекта сайта сообщения о сообщении возможности веб-узла для текущего сообщения.
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Параметры

 _lpulStatus_
  
> [out] Указатель на битовую маску флагов, который предоставляет сведения о состоянии сообщения. Можно задать следующие флажки:
    
VCSTATUS_COPY 
  
> Можно скопировать сообщение. 
    
VCSTATUS_DELETE 
  
> Можно удалить сообщение.
    
VCSTATUS_DELETE_IS_MOVE 
  
> При удалении сообщения перемещаются в папку **Удаленных элементов** в хранилище сообщения вместо немедленно удаляется из его хранилища сообщений. 
    
VCSTATUS_MOVE 
  
> Можно перемещать сообщения.
    
VCSTATUS_NEW_MESSAGE 
  
> Можно создать новое сообщение.
    
VCSTATUS_SAVE 
  
> Сообщения могут быть сохранены.
    
VCSTATUS_SUBMIT 
  
> Можно отправить сообщение.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Объекты формы вызовите метод **IMAPIMessageSite::GetSiteStatus** , чтобы получить возможность объект сайта message для текущего сообщения. Флажки, возвращаемые в параметре _lpulStatus_ содержатся сведения о сайте сообщения. Как правило формы включает или отключает команды меню, в зависимости от сведений, флаги обеспечивают возможности реализации сайта сообщения. Если новое сообщение загружается в форме, метод [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) или [IPersistMessage::Load](ipersistmessage-load.md) , проверяется состояние флаги. Некоторые объекты сайта сообщения, особенно только для чтения, объектов, не разрешать сообщения, чтобы быть сохранены или удалены. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Метод **IMAPIMessageSite::GetSiteStatus** может потребоваться клиентское приложение для выполнения некоторых вычислений, чтобы определить, какие операции может или не может быть выполнена для текущего сообщения. Как правило, который включает в себя посмотрев в строке состояния для поставщика хранилища сообщений текущего сообщения или запросы поставщика хранилища, чтобы определить, какие действия в клиентском приложении можно выполнять с помощью хранилища сообщений. Например, чтобы определить, нужно ли возвращать флаг MAPI_DELETE_IS_MOVE, проверьте свойство **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) объектов хранилища сообщений ли папки " **Удаленные** " в хранение сообщений. 
  
Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSiteStatus  <br/> |Mfcmapi (en) использует метод **IMAPIMessageSite::GetSiteStatus** , чтобы получить сведения о состоянии указанного сайта. Он может вернуть VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE или VCSTATUS_SUBMIT.  <br/> |
   
## <a name="see-also"></a>См. также



[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[Каноническое свойство PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Интерфейсы форм MAPI](mapi-form-interfaces.md)


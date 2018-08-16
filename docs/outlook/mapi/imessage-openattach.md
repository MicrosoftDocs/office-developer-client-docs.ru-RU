---
title: IMessageOpenAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.OpenAttach
api_type:
- COM
ms.assetid: b680f5a7-0df3-4e7b-bf3b-f149eb42be8d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c702e4063bf5e5a06a9e476a02172a780c7e326a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809269"
---
# <a name="imessageopenattach"></a>IMessage::OpenAttach

  
  
**Относится к**: Outlook 
  
Открывает вложение. 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>Параметры

 _ulAttachmentNum_
  
> [in] Номер индекса вложения, чтобы открыть, сохраненный в свойстве **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения. Этот номер индекса вложения в сообщении уникально идентифицирует допустимо только в контексте сообщения.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), представляющий интерфейс, который будет использоваться для доступа к вложение. Передача значение NULL, приводит к стандартным интерфейсом вложения или **IAttach**, возвращаемых. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как открыть вложение. Можно задать следующие флажки: 
    
MAPI_BEST_ACCESS 
  
> Запрашивает открывать вложения с разрешениями максимальное сети, разрешенных для пользователя и приложения максимальное клиентского доступа. Например если клиент имеет разрешение на чтение и запись, вложение должен быть открыт с разрешением на чтение и запись; Если клиент имеет доступ только для чтения, следует открыть вложение с доступом только для чтения. 
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenAttach** для возврата успешно, возможно перед вложение доступными для клиента. Если вложение не поддерживается, последующие подключения к нему может вызвать ошибку. 
    
MAPI_MODIFY 
  
> Запросы на разрешение чтения и записи. По умолчанию открытия вложений с доступом только для чтения и клиенты не должны работать предполагается, что что назначено разрешение чтения и записи. 
    
 _lppAttach_
  
> [out] Указатель на указатель открыть вложение.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вложение был успешно открыт.
    
## <a name="remarks"></a>Замечания

Метод **IMessage::OpenAttach** открывает вложения сообщения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы открыть вложения, имеется доступ к номеру вложения или свойство **PR_ATTACH_NUM** . Вызов [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) для получения таблицы вложений сообщений и найдите строку, которая представляет вложение, чтобы открыть. Для получения дополнительных сведений в разделе [Открытие вложения](opening-an-attachment.md) . 
  
Не пытайтесь открыть одного вложения несколько раз. результаты, значение undefined и зависящие от поставщика хранилища сообщений.
  
Можно запросить открывать вложения в режиме чтения и записи, а не в режиме только для чтения по умолчанию. Тем не менее ли вложение фактически открывается в режиме чтения и записи зависит от поставщика хранилища сообщений. Можно либо попытка изменить вложение, Подготовка для обработки возможных сбоев или установите флажок для уровня доступа, которые были предоставлены извлекая свойство **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) вложений, если она доступна. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|Используется для AttachmentsDlg.cpp  <br/> |CAttachmentsDlg::OpenItemProp  <br/> |Mfcmapi (en) использует метод **IMessage::OpenAttach** для открытия вложения объектов  <br/> |
   
## <a name="see-also"></a>См. также



[IMessage: IMAPIProp](imessageimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

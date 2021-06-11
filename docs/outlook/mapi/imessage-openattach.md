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
ms.openlocfilehash: e0c3747b48526b715f976e7bf3c142097c85f29a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405900"
---
# <a name="imessageopenattach"></a>IMessage::OpenAttach

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает вложение. 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>Parameters

 _ulAttachmentNum_
  
> [in] Индексировать число открываемого вложения, как хранится в **свойстве PR_ATTACH_NUM** [(PidTagAttachNumber).](pidtagattachnumber-canonical-property.md) Этот номер индекса однозначно определяет вложение в сообщении и действителен только в контексте сообщения.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), представляющий интерфейс, используемый для доступа к вложениям. Передача NULL приводит к возвращению стандартного интерфейса вложения или **IAttach.** 
    
 _ulFlags_
  
> [in] Bitmask флагов, которые контролируют, как вложение открывается. Можно установить следующие флаги: 
    
MAPI_BEST_ACCESS 
  
> Запросы на открытие вложения с максимальным разрешением сети, разрешенным пользователю, и максимальным доступом к приложению клиента. Например, если у клиента есть разрешение на чтение и записи, вложение следует открыть с разрешения на чтение и записи; если клиент имеет доступ только для чтения, вложение должно открываться только для чтения. 
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenAttach** успешно возвращаться, возможно, до того, как вложение будет полностью доступно для вызываемого клиента. Если вложение не доступно, последующий вызов может привести к ошибке. 
    
MAPI_MODIFY 
  
> Запросы на чтение и написание разрешений. По умолчанию вложения открываются с доступом только для чтения, и клиенты не должны работать на предположении, что разрешение на чтение и записи было предоставлено. 
    
 _lppAttach_
  
> [вышел] Указатель на указатель на открытое вложение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вложение было успешно открыто.
    
## <a name="remarks"></a>Примечания

Метод **IMessage::OpenAttach** открывает вложение сообщения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы открыть вложение, необходимо иметь доступ к его номеру вложения **или PR_ATTACH_NUM** свойству. Позвоните [в IMessage::GetAttachmentTable,](imessage-getattachmenttable.md) чтобы получить таблицу вложений сообщения и найти строку, которая представляет вложение, которое необходимо открыть. Дополнительные [сведения см. в приложении Opening](opening-an-attachment.md) an Attachment. 
  
Не пытайтесь открыть одно вложение несколько раз; результаты неопределяются и зависят от поставщика магазина сообщений.
  
Вы можете запросить открытие вложения в режиме чтения и записи вместо режима только для чтения по умолчанию. Однако вопрос о том, будет ли вложение открыто в режиме чтения и записи, находится в итоге за поставщиком магазина сообщений. Можно либо попытаться изменить вложение, подготовиться к возможному сбою, либо проверить уровень доступа, предоставленный путем получения свойства[PR_ACCESS_LEVEL (PidTagAccessLevel),](pidtagaccesslevel-canonical-property.md)если оно доступно.  
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp Используется для  <br/> |CAttachmentsDlg::OpenItemProp  <br/> |MFCMAPI использует **метод IMessage::OpenAttach** для открытия объектов вложений,  <br/> |
   
## <a name="see-also"></a>См. также



[IMessage: IMAPIProp](imessageimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)


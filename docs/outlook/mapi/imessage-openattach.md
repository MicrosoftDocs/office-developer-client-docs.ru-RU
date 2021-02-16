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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Номер индекса открываемого вложения, который хранится в свойстве **PR_ATTACH_NUM** ([PidTagAttachNumber).](pidtagattachnumber-canonical-property.md) Этот номер индекса уникально идентифицирует вложение в сообщении и действителен только в контексте сообщения.
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса( IID), представляющий интерфейс, который будет использоваться для доступа к вложениям. Передача NULL приводит к возвращению стандартного интерфейса вложения или **IAttach.** 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет открытием вложения. Можно установить следующие флаги: 
    
MAPI_BEST_ACCESS 
  
> Запрашивает открытие вложения с максимальным разрешенным для пользователя сетевым разрешением и максимальным доступом клиентского приложения. Например, если у клиента есть разрешение на чтение и записи, вложение должно быть открыто с разрешением на чтение и записи; если клиент имеет доступ только для чтения, вложение должно быть открыто с доступом только для чтения. 
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **openAttach** успешно возвращаться, возможно, до того, как вложение будет полностью доступно вызываемому клиенту. Если вложение не доступно, последующий вызов может привести к ошибке. 
    
MAPI_MODIFY 
  
> Запрашивает разрешение на чтение и записи. По умолчанию вложения открываются с доступом только для чтения, и клиенты не должны работать при предположении, что разрешение на чтение и записи предоставлено. 
    
 _lppAttach_
  
> [out] Указатель на указатель на открытое вложение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вложение успешно открыто.
    
## <a name="remarks"></a>Примечания

Метод **IMessage::OpenAttach** открывает вложение сообщения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы открыть вложение, необходимо иметь доступ к его номеру вложения **или PR_ATTACH_NUM** свойству. Вызовите [IMessage::GetAttachmentTable,](imessage-getattachmenttable.md) чтобы получить таблицу вложений сообщения и найти строку, представляюную вложение, которое необходимо открыть. Дополнительные [сведения см.](opening-an-attachment.md) в открываемом вложении. 
  
Не пытайтесь открыть одно вложение несколько раз; результаты являются неопределенными и зависят от поставщика store сообщений.
  
Можно запросить открытие вложения в режиме чтения и записи, а не в режиме только для чтения по умолчанию. Однако, будет ли вложение открываться в режиме чтения и записи, может ли поставщик хранилище сообщений. Можно либо попытаться изменить вложение, подготовиться к обработке возможного сбоя, либо проверить уровень доступа, предоставленный путем получения свойства **PR_ACCESS_LEVEL** ([PidTagAccessLevel),](pidtagaccesslevel-canonical-property.md)если оно доступно. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp Used to  <br/> |CAttachmentsDlg::OpenItemProp  <br/> |MFCMAPI использует метод **IMessage::OpenAttach** для открытия объектов вложений,  <br/> |
   
## <a name="see-also"></a>См. также



[IMessage: IMAPIProp](imessageimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)


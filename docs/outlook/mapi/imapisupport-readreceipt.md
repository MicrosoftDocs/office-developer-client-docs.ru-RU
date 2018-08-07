---
title: IMAPISupportReadReceipt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ReadReceipt
api_type:
- COM
ms.assetid: ef31b61a-93b6-4ae8-bc71-f5ef5caf43f4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 5e56fd8c053ff32bdeb7b243701c0330b378cdc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809177"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**Относится к**: Outlook 
  
Создает доступ на чтение или nonread отчет для сообщения.
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] Битовая маска флаги, который управляет созданием доступ на чтение или nonread отчета. Можно задать следующий флаг:
    
MAPI_NON_READ 
  
> Создается nonread отчет. Если MAPI_NON_READ не установлен, создается чтения отчет.
    
 _lpReadMessage_
  
> [in] Указатель на сообщение о том, какие будет создан отчет.
    
 _lppEmptyMessage_
  
> [in, out] На входе _lppEmptyMessage_ указывает указатель на пустое сообщение. На выходе _lppEmptyMessage_ указывает указатель на сообщение отчета. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Отчет создан успешно.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::ReadReceipt** применяется только для объектов поддержки поставщика хранилища сообщений. Поставщики хранилища сообщений вызов **ReadReceipt** для указания MAPI для создания доступ на чтение или nonread отчетов для сообщений, на который указывает параметр _lpReadMessage_ . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вызовите **ReadReceipt** , когда свойству **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) и выполняется одно из следующих условий:
  
- О сообщениях.
    
- Сообщение перемещено.
    
- Сообщение скопирован.
    
- Был вызван метод [IMessage::SetReadFlag](imessage-setreadflag.md) сообщений. 
    
Не вызывайте **ReadReceipt** , когда сообщение удаляется. 
  
Доступ на чтение или nonread отчет следует отправить только один раз для сообщения. Отслеживать состояние чтения сообщения и не отправляет несколько отчетов для одного сообщения.
  
Если параметр _lppEmptyMessage_ указывает действительный отчет при возврате MAPI из **ReadReceipt**, вызовите метод [IMessage::SubmitMessage](imessage-submitmessage.md) , чтобы отправить сообщение и затем выпуска указателя мыши, вызвав его **IUnknown:s:Release **метод. 
  
В случае сбоя **ReadReceipt** необходимо освободить сообщение без отправки. Если сохранять состояние чтения сообщения можно попытка создать доступ на чтение или nonread отчета в дальнейшем. 
  
Можно скрыть или отобразить чтения и nonread отчеты, созданные с хранилищ в папках. Хранение отчетов чтения и nonread в скрытых папок позволяет реализовывать повышения безопасности.
  
## <a name="see-also"></a>См. также



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[Каноническое свойство PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


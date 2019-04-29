---
title: Имаписуппортреадрецеипт
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
ms.openlocfilehash: 1915004847fdfd27c97656223866aaab9d3e59c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425325"
---
# <a name="imapisupportreadreceipt"></a>IMAPISupport::ReadReceipt

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает отчет о прочтении или непрочтении для сообщения.
  
```cpp
HRESULT ReadReceipt(
ULONG ulFlags,
LPMESSAGE lpReadMessage,
LPMESSAGE FAR * lppEmptyMessage
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Битовая маска флагов, определяющих способ создания отчета о прочтении или непрочтении. Можно задать следующий флаг:
    
МАПИ_НОН_РЕАД 
  
> Создается отчет о непрочтенном. Если МАПИ_НОН_РЕАД не задано, создается отчет о прочтении.
    
 _Лпреадмессаже_
  
> возврата Указатель на сообщение, о котором должен быть создан отчет.
    
 _Лппемптимессаже_
  
> [вход, выход] Во входных данных _лппемптимессаже_ указывает на указатель на пустое сообщение. В выходных данных _лппемптимессаже_ указывает на указатель на сообщение отчета. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Отчет успешно создан.
    
## <a name="remarks"></a>Примечания

Метод **имаписуппорт:: ReadReceipt** реализован только для объектов поддержки поставщика хранилища сообщений. Поставщики хранилищ сообщений вызывают **ReadReceipt** , чтобы сообщить MAPI о создании отчета о прочтении или непрочтении для сообщения, на которое указывает параметр _лпреадмессаже_ . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

ВыЗовите **ReadReceipt** , если задано свойство **пр_реад_рецеипт_рекуестед** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)), и выполняется одно из следующих условий:
  
- Сообщение прочитано.
    
- Сообщение было перемещено.
    
- Сообщение скопировано.
    
- Был вызван метод сообщения [iMessage:: сетреадфлаг](imessage-setreadflag.md) . 
    
Не вызывайте **ReadReceipt** при удалении сообщения. 
  
Отчет о прочтении или непрочтении должен быть отправлен только один раз для сообщения. Следите за состоянием чтения сообщения и не отправляете несколько отчетов для одного сообщения.
  
Если параметр _лппемптимессаже_ указывает на допустимое сообщение отчета, когда MAPI возвращает значение из **ReadReceipt**, вызовите метод [iMessage:: субмитмессаже](imessage-submitmessage.md) , чтобы отправить сообщение, а затем отпустите указатель, вызвав его метод **IUnknown: s: Release **метод. 
  
Если **ReadReceipt** завершается с ошибкой, сообщение должно быть выпущено без отправки. Если вы сохраняете состояние чтения сообщения, вы можете попытаться создать отчет о прочтении или непрочтении позже. 
  
Можно либо скрыть, либо отобразить отчеты о прочтении и непрочтении, созданные хранилищами в папках. Хранение отчетов о прочтении и непрочтенных в скрытых папках позволяет реализовать более тесную защиту.
  
## <a name="see-also"></a>См. также



[IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
  
[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[Каноническое свойство PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


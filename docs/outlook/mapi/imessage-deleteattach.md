---
title: имессажеделетеаттач
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.DeleteAttach
api_type:
- COM
ms.assetid: 0a5cb49f-c4f3-4893-8616-80d6332efcfc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c14ccac0addbc1288e3507cf549344f75e69cc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430709"
---
# <a name="imessagedeleteattach"></a>IMessage::DeleteAttach

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Удаляет вложение.
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _улаттачментнум_
  
> возврата Номер индекса удаляемого вложения. Это значение для свойства **PR_ATTACH_NUM** вложения ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).
    
 _улуипарам_
  
> возврата Дескриптор родительского окна всех диалоговых окон или окон, которые отображает этот метод. Параметр _улуипарам_ игнорируется, если в параметре _ulFlags_ не задан флаг ATTACH_DIALOG. 
    
 _лппрогресс_
  
> возврата Указатель на объект Progress, который отображает индикатор хода выполнения. Если в _лппрогресс_передается значение null, то поставщик хранилища сообщений отображает индикатор хода выполнения с помощью реализации объекта Progress для MAPI. Параметр _лппрогресс_ игнорируется, если не установлен флаг ATTACH_DIALOG в _ulFlags_.
    
 _ulFlags_
  
> возврата Битовая маска флагов, которые управляют отображением пользовательского интерфейса. Можно задать следующий флаг:
    
ATTACH_DIALOG 
  
> Запрашивает отображение индикатора хода выполнения при выполнении операции.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вложение успешно удалено.
    
## <a name="remarks"></a>Примечания

Метод **iMessage::D елетеаттач** удаляет вложение из сообщения. 
  
Удаленное вложение не удаляется окончательно до тех пор, пока не будет вызван метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Перед вызовом **делетеаттач**вызовите метод **IUnknown:: Release** для вложения и всех его потоков. 
  
Так как удаление вложения может быть длительным процессом, **делетеаттач** предоставляет механизм, который отображает индикатор хода выполнения. Вы можете запросить отображение индикатора хода выполнения путем передачи указателя на [IMAPIProgress: реализация IUnknown](imapiprogressiunknown.md) или значение null, если у вас нет реализации. Кроме того, необходимо указать дескриптор окна в параметре _улуипарам_ и флаг ATTACH_DIALOG в параметре _ulFlags_ . 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Аттачментсдлг. cpp  <br/> |Каттачментсдлг:: Онделетеселектедитем  <br/> |MFCMAPI использует метод **iMessage::D елетеаттач** , чтобы удалить выбранное вложение.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)


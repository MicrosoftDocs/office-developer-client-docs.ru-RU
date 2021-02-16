---
title: IMessageDeleteAttach
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

 _ulAttachmentNum_
  
> [in] Номер индекса вложения, который необходимо удалить. Это значение свойства PR_ATTACH_NUM[(PidTagAttachNumber).](pidtagattachnumber-canonical-property.md) 
    
 _ulUIParam_
  
> [in] Обрабатывайте родительское окно любых диалогов или окон, которые отображает этот метод. Параметр _ulUIParam_ игнорируется, если ATTACH_DIALOG флага в параметре _ulFlags._ 
    
 _lpProgress_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения. Если в  _lpProgress_ передается NULL, поставщик хранилище сообщений отображает индикатор хода выполнения с помощью реализации объекта хода выполнения MAPI. Параметр _lpProgress_ игнорируется, если флаг ATTACH_DIALOG не установлен в _ulFlags._
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет отображением пользовательского интерфейса. Можно установить следующий флаг:
    
ATTACH_DIALOG 
  
> Запрашивает отображение индикатора хода выполнения по мере выполнения операции.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вложение успешно удалено.
    
## <a name="remarks"></a>Примечания

Метод **IMessage::D eleteAttach** удаляет вложение из сообщения. 
  
Удаленное вложение не удаляется окончательно, пока не будет вызван метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщения. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Перед **вызовом DeleteAttach** вызовите метод **IUnknown::Release** для вложения и каждого из его потоков. 
  
Поскольку удаление вложения может быть длительным процессом, **DeleteAttach** предоставляет механизм отображения индикатора хода выполнения. Вы можете запросить отображение индикатора хода выполнения, передав указатель на реализацию [IMAPIProgress : IUnknown](imapiprogressiunknown.md) или NULL, если у вас нет реализации. Также необходимо указать окне в параметре _ulUIParam_ и флаг ATTACH_DIALOG в _параметре ulFlags._ 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp  <br/> |CAttachmentsDlg::OnDeleteSelectedItem  <br/> |MFCMAPI использует **метод IMessage::D eleteAttach** для удаления выбранного вложения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)


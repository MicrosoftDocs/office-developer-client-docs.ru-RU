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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет вложение.
  
```cpp
HRESULT DeleteAttach(
ULONG ulAttachmentNum,
ULONG_PTR ulUIParam,
LPMAPIPROGRESS lpProgress,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulAttachmentNum_
  
> [in] Индекс номер вложения для удаления. Это значение для свойства PR_ATTACH_NUM  [(PidTagAttachNumber).](pidtagattachnumber-canonical-property.md)
    
 _ulUIParam_
  
> [in] Обрабатывайте родительское окно любых диалогов или окон, отображаемого этим методом. Параметр _ulUIParam_ игнорируется, если флаг ATTACH_DIALOG в параметре _ulFlags._ 
    
 _lpProgress_
  
> [in] Указатель на объект прогресса, отображает индикатор прогресса. Если NULL передается в  _lpProgress,_ поставщик магазина сообщений отображает индикатор прогресса с помощью реализации объекта progress MAPI. Параметр  _lpProgress_ игнорируется, если флаг ATTACH_DIALOG не задан в  _ulFlags_.
    
 _ulFlags_
  
> [in] Bitmask флагов, которые контролируют отображение пользовательского интерфейса. Можно установить следующий флаг:
    
ATTACH_DIALOG 
  
> Запрашивает отображение индикатора прогресса по мере выполнения операции.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вложение было успешно удалено.
    
## <a name="remarks"></a>Примечания

Метод **IMessage::D eleteAttach** удаляет вложение из сообщения. 
  
Удаленное вложение не удаляется окончательно до тех пор, пока не будет вызван метод [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Перед **вызовом DeleteAttach** позвоните по методу **IUnknown::Release** для вложения и каждого из его потоков. 
  
Так как удаление вложения может быть длительным процессом, **DeleteAttach** предоставляет механизм, отображающий индикатор прогресса. Вы можете запросить отображение индикатора прогресса, передав указатель на [реализацию IMAPIProgress: IUnknown](imapiprogressiunknown.md) или NULL, если у вас нет реализации. Также необходимо указать ручку окна в параметре _ulUIParam_ и флаг ATTACH_DIALOG в _параметре ulFlags._ 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp  <br/> |CAttachmentsDlg::OnDeleteSelectedItem  <br/> |MFCMAPI использует **метод IMessage::D eleteAttach** для удаления выбранного вложения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)


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
ms.openlocfilehash: 93f264cc91118e40f7a2869d29e7e53d404ae381
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809274"
---
# <a name="imessagedeleteattach"></a>IMessage::DeleteAttach

  
  
**Относится к**: Outlook 
  
Удаляет вложения.
  
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
  
> [in] Номер индекса для удаления вложения. Это значение для свойства **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения.
    
 _ulUIParam_
  
> [in] Дескриптор родительского окна все диалоговые окна и окна, этот метод отображает. Параметр _ulUIParam_ игнорируется, пока флаг ATTACH_DIALOG будет выполнен с помощью параметра _ulFlags_ . 
    
 _lpProgress_
  
> [in] Указатель на объект хода выполнения, который отображает индикатор хода выполнения. Если в _lpProgress_передается значение NULL, поставщик хранения сообщений отображает индикатор выполнения с помощью объекта реализации интерфейса MAPI хода выполнения. Параметр _lpProgress_ используется только флаг ATTACH_DIALOG установлен в _ulFlags_.
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющее отображение пользовательского интерфейса. Можно задать следующий флаг:
    
ATTACH_DIALOG 
  
> Запрос на отображение индикатор выполнения как операция продолжается.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вложение успешно удален.
    
## <a name="remarks"></a>Замечания

Метод **IMessage::DeleteAttach** удаляет вложения в сообщение. 
  
До вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) сообщение удаленного вложения не удаляется без возможности восстановления. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

До вызова метода **DeleteAttach**, вызовите метод **функции IUnknown::Release** для вложения и каждый из его потоков. 
  
Поскольку удаление вложений может быть много времени, **DeleteAttach** обеспечивает механизм, индикатор хода выполнения. Можно запросить отображение индикатор хода выполнения, передав указатель на [IMAPIProgress: IUnknown](imapiprogressiunknown.md) реализации или значение NULL, если у вас нет реализации. Необходимо также указать дескриптор окна в параметр _ulUIParam_ и флаг ATTACH_DIALOG с помощью параметра _ulFlags_ . 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp  <br/> |CAttachmentsDlg::OnDeleteSelectedItem  <br/> |Mfcmapi (en) метод **IMessage::DeleteAttach** используется для удаления выбранного вложения.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

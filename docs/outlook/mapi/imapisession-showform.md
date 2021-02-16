---
title: IMAPISessionShowForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.ShowForm
api_type:
- COM
ms.assetid: 233cf936-34db-42d4-b5e3-17a93acb2009
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8b90dee3958a20994f9a60d104ae714ad95307d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412529"
---
# <a name="imapisessionshowform"></a>IMAPISession::ShowForm

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Отображает форму.
  
```cpp
HRESULT ShowForm(
  ULONG_PTR ulUIParam,
  LPMDB lpMsgStore,
  LPMAPIFOLDER lpParentFolder,
  LPCIID lpInterface,
  ULONG ulMessageToken,
  LPMESSAGE lpMessageSent,
  ULONG ulFlags,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  ULONG ulAccess,
  LPSTR lpszMessageClass
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Handle to the parent window of the form.
    
 _lpMsgStore_
  
> [in] Указатель на хранилище сообщений, которое содержит папку, на которую указывает параметр _lpParentFolder._ 
    
 _lpParentFolder_
  
> [in] Указатель на папку, в которой было создано сообщение, связанное с параметром _ulMessageToken._ 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к сообщению, которое отображается в форме. Параметр  _lpInterface_ должен иметь NULL или IID_IMessage. Передача NULL приводит к использования [стандартного интерфейса IMessage.](imessageimapiprop.md) 
    
 _ulMessageToken_
  
> [in] Маркер, связанный с сообщением для отображения в форме. Параметр _ulMessageToken_ должен иметь содержимое параметра _lpulMessageToken_ из предыдущего вызова [IMAPISession::P repareForm.](imapisession-prepareform.md)
    
 _lpMessageSent_
  
> [in] Зарезервировано; должно быть NULL. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет тем, как и является ли сообщение сохраненным. Можно установить следующие флаги:
    
MAPI_NEW_MESSAGE 
  
> Сообщение никогда не было сохранено (то есть его метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) никогда не был вызван). 
    
MAPI_POST_MESSAGE 
  
> Сообщение должно быть сохранено в родительской папке. Сообщение не обрабатывается для отправки, а отправляется в папку. Если этот флаг не установлен, сообщение копируется в почтовый ящик и обрабатывается для отправки. 
    
 _ulMessageStatus_
  
> [in] Битоваяmas флагов, скопированная из свойства **PR_MSG_STATUS** ([PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)сообщения, связанного с маркером в параметре _ulMessageToken._ Флаги предоставляют сведения о состоянии сообщения. 
    
 _ulMessageFlags_
  
> [in] Битоваяmas флагов, скопированная из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)сообщения, связанного с маркером в параметре _ulMessageToken._ Эти флаги предоставляют дополнительные сведения о состоянии сообщения. 
    
 _ulAccess_
  
> [in] Флаг, который указывает уровень разрешений для сообщения, отображаемой в форме. Эти сведения копируются из свойства **PR_ACCESS** ([PidTagAccess)](pidtagaccess-canonical-property.md)сообщения, связанного с маркером в параметре _ulMessageToken._ 
    
 _lpszMessageClass_
  
> [in] Указатель на класс сообщения, отображаемого в форме, **скопирован** из свойства PR_MESSAGE_CLASS ([PidTagMessageClass)](pidtagmessageclass-canonical-property.md)сообщения, связанного с маркером в параметре _ulMessageToken._ 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Форма успешно отобрана.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::ShowForm** отображает форму сообщения, подготовленную методом **IMAPISession::P repareForm.** 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

В параметре _lpMessage_ метода **PrepareForm** должна быть только одна ссылка на сообщение. 
  
Следует помнить, что реализации форм могут возвращать значения ошибок, кроме значений, задокументированных в MAPI. Если эти значения ошибки можно использовать для более точного определения условия ошибки, сделайте это. В противном случае обработать эти ошибки так же, как и MAPI_E_CALL_FAILED. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI использует метод **IMAPISession::ShowForm** вместе с методом **PrepareForm** для отображения сообщения в модальной форме.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)


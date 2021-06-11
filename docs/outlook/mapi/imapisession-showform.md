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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительского окна формы.
    
 _lpMsgStore_
  
> [in] Указатель в хранилище сообщений, содержащий папку, указываемую параметром _lpParentFolder._ 
    
 _lpParentFolder_
  
> [in] Указатель на папку, в которой было создано сообщение, связанное с параметром _ulMessageToken._ 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, который будет использоваться для доступа к сообщению, отображаемом в форме. Параметр  _lpInterface должен_ быть NULL или IID_IMessage. Передача NULL приводит к стандартному интерфейсу [IMessage,](imessageimapiprop.md)который используется. 
    
 _ulMessageToken_
  
> [in] Маркер, связанный с сообщением, которое будет отображаться в форме. Параметр  _ulMessageToken_ должен быть задан для содержимого  _параметра lpulMessageToken_ из предыдущего вызова [в IMAPISession::P repareForm](imapisession-prepareform.md).
    
 _lpMessageSent_
  
> [in] Зарезервировано; должно быть NULL. 
    
 _ulFlags_
  
> [in] Битмаски флагов, которые контролируют, как и сохранено ли сообщение. Можно установить следующие флаги:
    
MAPI_NEW_MESSAGE 
  
> Сообщение никогда не было сохранено (то есть его [метод IMAPIProp::SaveChanges](imapiprop-savechanges.md) никогда не был вызван). 
    
MAPI_POST_MESSAGE 
  
> Сообщение должно быть сохранено в родительской папке. Сообщение не обрабатывается для отправки, а отправляется в папку. Если этот флаг не установлен, сообщение копируется в почтовый ящик и обрабатывается для отправки. 
    
 _ulMessageStatus_
  
> [in] Битмаска **флагов,** скопированная из свойства [PR_MSG_STATUS (PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)сообщения, связанного с маркером в параметре _ulMessageToken._ Флаги предоставляют сведения о состоянии сообщения. 
    
 _ulMessageFlags_
  
> [in] Битмаска **флагов,** скопированная из свойства [PR_MESSAGE_FLAGS (PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)сообщения, связанного с маркером в параметре _ulMessageToken._ Эти флаги предоставляют дополнительные сведения о состоянии сообщения. 
    
 _ulAccess_
  
> [in] Флаг, который указывает уровень разрешений для сообщения, отображаемой в форме. Эти сведения копируются из **свойства PR_ACCESS** [(PidTagAccess)](pidtagaccess-canonical-property.md)сообщения, связанного с маркером в параметре _ulMessageToken._ 
    
 _lpszMessageClass_
  
> [in] Указатель на класс сообщения, отображаемого в форме, **скопирован** с свойства [PR_MESSAGE_CLASS (PidTagMessageClass)](pidtagmessageclass-canonical-property.md)сообщения, связанного с маркером в параметре _ulMessageToken._ 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Форма успешно отображалась.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::ShowForm** отображает форму сообщения, подготовленную методом **IMAPISession::P repareForm.** 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Вы должны иметь только одну ссылку на сообщение, переданное в _параметре lpMessage_ метода **PrepareForm.** 
  
Следует помнить, что реализация форм может возвращать значения ошибок, помимо значений, задокументированных MAPI. Если вы можете использовать эти значения ошибок для более точного определения состояния ошибки, сделайте это. В противном случае справься с этими ошибками так, как MAPI_E_CALL_FAILED. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI использует **метод IMAPISession::ShowForm** вместе с методом **PrepareForm** для отображения сообщения в модальной форме.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)


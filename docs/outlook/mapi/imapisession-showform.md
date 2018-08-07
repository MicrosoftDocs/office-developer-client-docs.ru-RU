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
ms.openlocfilehash: d20c8e7432903ef9334f066df31694752384d034
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809087"
---
# <a name="imapisessionshowform"></a>IMAPISession::ShowForm

  
  
**Относится к**: Outlook 
  
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
  
> [in] Дескриптор родительского окна формы.
    
 _lpMsgStore_
  
> [in] Указатель на хранилище сообщений, содержащем папку, на который указывает параметр _lpParentFolder_ . 
    
 _lpParentFolder_
  
> [in] Указатель на папку, в котором был создан сообщения, связанного с параметром _ulMessageToken_ . 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к сообщение, которое отображается в форме. Параметр _lpInterface_ должен быть NULL или IID_IMessage. В стандартный интерфейс [IMessage](imessageimapiprop.md)используется результаты передаче значения NULL. 
    
 _ulMessageToken_
  
> [in] Маркер, который связан с сообщение, отображаемое в форме. Параметр _ulMessageToken_ должен иметь значение содержимого параметра _lpulMessageToken_ из предыдущего вызова [IMAPISession::PrepareForm](imapisession-prepareform.md).
    
 _lpMessageSent_
  
> [in] Зарезервировано; должен иметь значение NULL. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как и ли сообщение сохраняется. Можно задать следующие флажки:
    
MAPI_NEW_MESSAGE 
  
> Сообщения никогда не были сохранены (то есть, его [IMAPIProp::SaveChanges](imapiprop-savechanges.md) никогда не был вызван метод). 
    
MAPI_POST_MESSAGE 
  
> Сообщения должны сохраняться в родительской папки. Сообщение не обрабатывается для отправки, но вместо этого он был отправлен в папку. Если этот флаг не установлен, сообщение копируется в папке "Исходящие" и обрабатывается для отправки. 
    
 _ulMessageStatus_
  
> [in] Битовая маска флаги, скопированные из свойства **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) сообщения, связанный с маркером в параметре _ulMessageToken_ . Флаги предоставляют информацию о состоянии сообщения. 
    
 _ulMessageFlags_
  
> [in] Битовая маска флаги, скопированные из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщения, связанный с маркером в параметре _ulMessageToken_ . Эти флаги предоставляют информацию о состоянии сообщения. 
    
 _ulAccess_
  
> [in] Флаг, указывающий уровень разрешений для сообщения, которое отображается в форме. Эта информация копируется из свойства **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) сообщения, связанный с маркером в параметре _ulMessageToken_ . 
    
 _lpszMessageClass_
  
> [in] Указатель на класс сообщения сообщения, отображаемого в форме, скопированные из свойства **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) сообщения, связанный с маркером в параметре _ulMessageToken_ . 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Успешно отобразить форму.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Замечания

Метод **IMAPISession::ShowForm** отображает форму сообщение, которое было подготовлено с помощью метода **IMAPISession::PrepareForm** . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Должен иметь только один ссылку на сообщение, переданной в параметре _lpMessage_ метод **PrepareForm** . 
  
Обратите внимание, что реализации формы можно вернуть ошибочные значения не указаны, задокументированные с MAPI. Если значения этих ошибок можно использовать для более точные определения условия ошибки, сделайте это. В противном случае обрабатывает эти ошибки, как обрабатывается MAPI_E_CALL_FAILED. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |Mfcmapi (en) использует метод **IMAPISession::ShowForm** вместе с методом **PrepareForm** для отображения сообщения в модальную форму.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)


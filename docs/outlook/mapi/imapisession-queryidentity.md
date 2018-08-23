---
title: IMAPISessionQueryIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.QueryIdentity
api_type:
- COM
ms.assetid: a2cdda90-5457-49a7-b98c-7273ffe5cbbc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6b64653aa87ff7ac983409978a69f59148251d7d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583416"
---
# <a name="imapisessionqueryidentity"></a>IMAPISession::QueryIdentity

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Возвращает идентификатор записи объекта, который содержит основной идентификатор для этого сеанса.
  
```cpp
HRESULT QueryIdentity(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Параметры

 _lpcbEntryID_
  
> [out] Указатель на число байтов в идентификатор записи, на который указывает параметр _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Указатель на указатель на идентификатор записи объекта, который содержит основной идентификатор.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Основной идентификатор успешно возвращен.
    
MAPI_W_NO_SERVICE 
  
> Вызов завершился успешно, однако это не имеет не основного удостоверения для сеанса. При возвращении этого предупреждения вызова необходимо обрабатывать об успешном завершении. Чтобы проверить это предупреждение, используйте **HR_FAILED** макрос. Дополнительные сведения можно [С помощью макросов для обработки ошибок](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Замечания

Метод **IMAPISession::QueryIdentity** получает основной идентификатор для текущего сеанса и возвращает значение, используя параметр _lppEntryID_ . Основной идентификатор является объектом, обычно обмена сообщениями пользователя, представляющий пользователя сеанса.  _lppEntryID_ возвращает первичный идентификатор объекта [IMailUser](imailuserimapiprop.md) , которые также хранятся как свойство [PidTagEntryID](pidtagentryid-canonical-property.md) . Значение, возвращаемое в _lppEntryID_ можно использовать для открытия объекта **IMailUser** с помощью [IMAPISession::OpenEntry](imapisession-openentry.md).
  
Несмотря на то, что многие поставщики услуг в нескольких служб сообщения можно обеспечить основной идентификатор сеанса, MAPI назначает отдельный поставщик услуг. Поставщик услуг, который предоставляет основной идентификатор задает следующие элементы:
  
- Флаг STATUS_PRIMARY_IDENTITY в свойстве **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
    
- Свойство **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)).
    
- Свойство **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)).
    
- Свойство **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)).
    
Если поставщик услуг, который предоставляет основной идентификатор принадлежит службы сообщений, других поставщиков услуг службы сообщений также необходимо задать свойства PR_IDENTITY. Эти свойства публикуются в таблице состояния сеанса. 
  
Если это возможно **QueryIdentity** возвращает значение для свойства **PR_IDENTITY_ENTRYID** из строки состояния, с STATUS_PRIMARY_IDENTITY. Если свойство **PR_IDENTITY_ENTRYID** отсутствует в строке основного удостоверения, **QueryIdentity** возвращает идентификатора единичных записей, созданных с помощью прочие сведения из этой строки. 
  
В случае отсутствия из всех **PR_RESOURCE_FLAG** столбцов в таблице состояния флага STATUS_PRIMARY_IDENTITY **QueryIdentity** возвращает первый идентификатор записи, которая будет обнаружен. Если идентификатор не соответствующие записи для возврата, **QueryIdentity** успешно с предупреждением MAPI_W_NO_SERVICE и _lppEntryID_ , указывает идентификатор жестко записи. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Можно вызвать метод [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md) для назначения задач предоставления основной идентификатор сеанса службы сообщений. 
  
Другой способ получить основной идентификатор — поиск по ключевым словам в таблице состояния для строки со столбцами **PR_RESOURCE_FLAGS** , задайте значение STATUS_PRIMARY_IDENTITY. Дополнительные сведения об этой альтернативный способ получения сведений об удостоверениях см в [таблице состояния и состояния объектов](status-table-and-status-objects.md).
  
По окончании с помощью идентификатора записи для основного удостоверения, возвращаемые **QueryIdentity**освободите память путем вызова функции [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Дополнительные сведения сведения об удостоверениях, как правило, можно [Основного удостоверения MAPI](mapi-primary-identity.md). 
  
Дополнительные сведения о получении идентификатор сеанса MAPI разделе [Извлечение основной и поставщика удостоверений](retrieving-primary-and-provider-identity.md). 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnQueryIdentity  <br/> |Mfcmapi (en) использует метод **IMAPISession::QueryIdentity** для открытия записи адресной книги для основной идентификатор сеанса.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISession::OpenEntry](imapisession-openentry.md)
  
[IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Основной идентификатор MAPI](mapi-primary-identity.md)
  
[Получение удостоверения поставщика и основного удостоверения](retrieving-primary-and-provider-identity.md)
  
[Обработка ошибок с помощью макросов](using-macros-for-error-handling.md)
  
[Таблица и объекты состояний](status-table-and-status-objects.md)


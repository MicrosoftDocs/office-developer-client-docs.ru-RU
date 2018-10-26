---
title: IMAPIFormMgrLoadForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.LoadForm
api_type:
- COM
ms.assetid: 5ca500c3-c737-45a5-b0fc-473b75c1d68d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3e758acfa1cf0c11be666dd730d9bf589d2e9d77
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586216"
---
# <a name="imapiformmgrloadform"></a>IMAPIFormMgr::LoadForm

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Запускает существующее сообщение при открытии формы.
  
```cpp
HRESULT LoadForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pmsg,
  LPMAPIVIEWCONTEXT pViewContext,
  REFIID riid,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Дескриптор родительского окна индикатор хода выполнения, отображаемое при открытии формы. Параметр _ulUIParam_ игнорируется, пока флаг MAPI_DIALOG будет выполнен с помощью параметра _ulFlags_ . 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как форма будет открыта. Можно задать следующие флажки:
    
MAPI_DIALOG 
  
> Отображает пользовательский интерфейс для предоставления состояния или запрашивать у пользователя для получения дополнительных сведений. Если этот флаг не установлен, пользовательский интерфейс не отображается.
    
MAPIFORM_EXACTMATCH 
  
> Следует разрешить только класс строки сообщения, которые являются точное совпадение.
    
 _lpszMessageClass_
  
> [in] Указатель на строку с именем класса сообщений для сообщений для загрузки. Если значение NULL передается в параметре _lpszMessageClass_ , класс сообщения определяет, какие из сообщения, на который указывает параметр _pmsg_ . 
    
 _ulMessageStatus_
  
> [in] Битовая маска флагов клиента или поставщика, скопированные из свойства **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) сообщения, предоставляющий информацию о состоянии сообщения. Необходимо задать параметр _ulMessageStatus_ , если _lpszMessageClass_ отлично от NULL; в противном случае _ulMessageStatus_ игнорируется. 
    
 _ulMessageFlags_
  
> [in] Указатель на битовой маски флагов, скопированные из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) сообщения, которое указывает, текущее состояние сообщения. Необходимо задать параметр _ulMessageFlags_ , если _lpszMessageClass_ отлично от NULL; в противном случае _ulMessageFlags_ игнорируется. 
    
 _pFolderFocus_
  
> [in] Указатель на папку, содержащую сообщение напрямую. Параметр _pFolderFocus_ может быть NULL, если такая папка не существует (например, если сообщение встроена в другое сообщение). 
    
 _pMessageSite_
  
> [in] Указатель на сайте сообщение сообщения.
    
 _pmsg_
  
> [in] Указатель на сообщение.
    
 _pViewContext_
  
> [in] Указатель на контекст представления для сообщения. Параметр _pViewContext_ может быть NULL. 
    
 _riid_
  
> [in] Идентификатор (ИД интерфейса) интерфейса, которое будет использоваться для объекта возвращенные формы. Параметр _riid_ не должна быть NULL. 
    
 _ppvObj_
  
> [out] Указатель на указатель на возвращенный интерфейс.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_INTERFACE 
  
> Форма не поддерживает запрошенный интерфейс.
    
MAPI_E_NOT_FOUND 
  
> Класс сообщения, переданные в _lpszMessageClass_ не соответствует класс сообщения для формы в библиотеке форм. 
    
## <a name="remarks"></a>Замечания

Средства просмотра форм вызовите метод **IMAPIFormMgr::LoadForm** для открытия формы для существующего сообщения. **LoadForm** открывает объекта формы, загружает сообщения в объект формы, задает контекст соответствующее представление при необходимости и возвращает запрошенный интерфейс для объекта формы. 
  
Параметр _pFolderFocus_ указывает на папку, содержащую сообщение. Если сообщение внедрен в другое сообщение, _pFolderFocus_ должен иметь значение NULL. 
  
## <a name="notes-to-implementers"></a>Примечания для реализующих

Если NULL передается в _lpszMessageClass_, реализация получает класс сообщения, состояние и флаги сообщения от **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** и **PR_MESSAGE_FLAGS сообщения **свойства. Если этот параметр указан в строке класс сообщения в _lpszMessageClass_реализации необходимо использовать значения в _ulMessageStatus_ и _ulMessageFlags_.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |Mfcmapi (en) использует метод **IMAPIFormMgr::LoadForm** для загрузки формы перед их отображением.  <br/> |
   
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagMessageClass](pidtagmessageclass-canonical-property.md)
  
[Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)


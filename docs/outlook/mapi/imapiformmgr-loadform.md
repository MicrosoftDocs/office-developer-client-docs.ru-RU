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
ms.openlocfilehash: 7e445646477ad1fc56b41141b541358d9b9f9616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418787"
---
# <a name="imapiformmgrloadform"></a>IMAPIFormMgr::LoadForm

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Запускает форму для открытия существующего сообщения.
  
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
  
> [in] Handle to the parent window of the progress indicator that is displayed while the form is opened. Параметр _ulUIParam_ игнорируется, если MAPI_DIALOG флага в параметре _ulFlags._ 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет открытием формы. Можно установить следующие флаги:
    
MAPI_DIALOG 
  
> Отображает пользовательский интерфейс для предоставления состояния или запроса дополнительных сведений. Если этот флаг не установлен, пользовательский интерфейс не отображается.
    
MAPIFORM_EXACTMATCH 
  
> Должны быть разрешены только строки класса сообщений, точно совпадают.
    
 _lpszMessageClass_
  
> [in] Указатель на строку, которая именует класс сообщения для загрузки. Если в параметре _lpszMessageClass_ передается NULL, класс сообщения определяется из сообщения, на которое указывает параметр _pmsg._ 
    
 _ulMessageStatus_
  
> [in] Битовая почта клиентских или определяемых поставщиком флагов, скопированная из свойства **PR_MSG_STATUS** ([PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)сообщения, которое предоставляет сведения о состоянии сообщения. Параметр  _ulMessageStatus должен_ быть задан, если  _lpszMessageClass_ не имеет NULL; в противном  _случае ulMessageStatus_ игнорируется. 
    
 _ulMessageFlags_
  
> [in] Указатель на битовуюmask флагов, скопированную из свойства **PR_MESSAGE_FLAGS** ([PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)сообщения, которое указывает текущее состояние сообщения. Параметр  _ulMessageFlags необходимо_ установить, если  _lpszMessageClass_ не имеет NULL; в противном  _случае ulMessageFlags_ игнорируется. 
    
 _pFolderFocus_
  
> [in] Указатель на папку, которая непосредственно содержит сообщение. Параметр  _pFolderFocus_ может иметь NULL, если такая папка не существует (например, если сообщение внедрено в другое сообщение). 
    
 _pMessageSite_
  
> [in] Указатель на сайт сообщения сообщения.
    
 _pmsg_
  
> [in] Указатель на сообщение.
    
 _pViewContext_
  
> [in] Указатель на контекст представления сообщения. Параметр  _pViewContext может_ иметь NULL. 
    
 _riid_
  
> [in] Идентификатор интерфейса, используемый для возвращаемого объекта формы. Параметр  _riid_ не должен иметь NULL. 
    
 _ppvObj_
  
> [out] Указатель на указатель на возвращенный интерфейс.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_INTERFACE 
  
> Форма не поддерживает запрашиваемую интерфейс.
    
MAPI_E_NOT_FOUND 
  
> Класс сообщения, переданный  _в lpszMessageClass,_ не соответствует классу сообщения для любой формы в библиотеке форм. 
    
## <a name="remarks"></a>Примечания

Посетители форм **звонят методу IMAPIFormMgr::LoadForm,** чтобы открыть форму для существующего сообщения. **LoadForm** открывает объект формы, загружает сообщение в объект формы, при необходимости настраивает соответствующий контекст представления и возвращает нужный интерфейс для объекта формы. 
  
Параметр  _pFolderFocus_ указывает на папку, в которую входит сообщение. Если сообщение внедрено в другое сообщение,  _pFolderFocus_ должен иметь NULL. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если в  _lpszMessageClass_ передается NULL, реализация получает класс, состояние и флаги сообщения из свойств **PR_MESSAGE_CLASS** [(PidTagMessageClass),](pidtagmessageclass-canonical-property.md) **PR_MSG_STATUS** **и PR_MESSAGE_FLAGS** сообщения. Если строка класса сообщения предоставляется в  _lpszMessageClass,_ реализация должна использовать значения  _в ulMessageStatus_ и  _ulMessageFlags_.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI использует метод **IMAPIFormMgr::LoadForm** для загрузки формы перед ее отображением.  <br/> |
   
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagMessageClass](pidtagmessageclass-canonical-property.md)
  
[Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)


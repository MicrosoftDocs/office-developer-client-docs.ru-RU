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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
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

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительского окна индикатора прогресса, отображаемого во время открытия формы. Параметр _ulUIParam_ игнорируется, если флаг MAPI_DIALOG в параметре _ulFlags._ 
    
 _ulFlags_
  
> [in] Битмаски флагов, которые контролируют, как форма открывается. Можно установить следующие флаги:
    
MAPI_DIALOG 
  
> Отображает пользовательский интерфейс для предоставления статуса или запроса дополнительных сведений. Если этот флаг не установлен, пользовательский интерфейс не отображается.
    
MAPIFORM_EXACTMATCH 
  
> Разрешены только строки класса сообщений, которые соответствуют точному типу.
    
 _lpszMessageClass_
  
> [in] Указатель на строку, которая называет класс сообщений загружаемого сообщения. Если NULL передается в _параметре lpszMessageClass,_ класс сообщения определяется из сообщения, на которое указывает параметр _pmsg._ 
    
 _ulMessageStatus_
  
> [in] Битмаска флагов, определенных клиентом или **поставщика,** скопированная из свойства [PR_MSG_STATUS (PidTagMessageStatus)](pidtagmessagestatus-canonical-property.md)сообщения, которое содержит сведения о состоянии сообщения. Параметр  _ulMessageStatus_ должен быть задан, если  _lpszMessageClass_ не является NULL; в противном  _случае ulMessageStatus_ игнорируется. 
    
 _ulMessageFlags_
  
> [in] Указатель на битмаску **флагов, скопированные** из свойства [PR_MESSAGE_FLAGS (PidTagMessageFlags)](pidtagmessageflags-canonical-property.md)сообщения, которое указывает текущее состояние сообщения. Параметр  _ulMessageFlags должен_ быть задан, если  _lpszMessageClass_ не является NULL; в противном  _случае ulMessageFlags_ игнорируется. 
    
 _pFolderFocus_
  
> [in] Указатель на папку, которая непосредственно содержит сообщение. Параметр  _pFolderFocus_ может быть NULL, если такой папки нет (например, если сообщение встроено в другое сообщение). 
    
 _pMessageSite_
  
> [in] Указатель на сайт сообщения сообщения.
    
 _pmsg_
  
> [in] Указатель на сообщение.
    
 _pViewContext_
  
> [in] Указатель на контекст представления для сообщения. Параметр  _pViewContext может_ быть NULL. 
    
 _riid_
  
> [in] Идентификатор интерфейса (IID) интерфейса, который будет использоваться для возвращаемого объекта формы. Параметр  _riid_ не должен быть NULL. 
    
 _ppvObj_
  
> [вышел] Указатель на указатель на возвращенный интерфейс.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_INTERFACE 
  
> Форма не поддерживает запрашиваемую интерфейсную форму.
    
MAPI_E_NOT_FOUND 
  
> Класс сообщений, переданный  _в lpszMessageClass,_ не соответствует классу сообщений для любой формы в библиотеке форм. 
    
## <a name="remarks"></a>Примечания

Зрители формы звонят по методу **IMAPIFormMgr::LoadForm,** чтобы открыть форму для существующего сообщения. **LoadForm** открывает объект формы, загружает сообщение в объект формы, при необходимости задает соответствующий контекст представления и возвращает запрашиваемую интерфейсную форму объекта. 
  
Параметр  _pFolderFocus_ указывает на папку, содержаную сообщение. Если сообщение встроено в другое сообщение,  _pFolderFocus_ должен быть NULL. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если NULL передается в _lpszMessageClass,_ реализация получает класс сообщения, состояние и флаги из свойств **PR_MESSAGE_CLASS** сообщения [(PidTagMessageClass),](pidtagmessageclass-canonical-property.md)PR_MSG_STATUS **и PR_MESSAGE_FLAGS.**  Если строка класса сообщения представлена  _в lpszMessageClass,_ реализация должна использовать значения  _в ulMessageStatus_ и  _ulMessageFlags_.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI использует **метод IMAPIFormMgr::LoadForm** для загрузки формы перед ее отображением.  <br/> |
   
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagMessageClass](pidtagmessageclass-canonical-property.md)
  
[Каноническое свойство PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Каноническое свойство PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)


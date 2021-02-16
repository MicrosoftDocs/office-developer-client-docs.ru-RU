---
title: IMAPIFormMgrCreateForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CreateForm
api_type:
- COM
ms.assetid: 7d4d50f8-3904-4e93-a535-ac7decceb1a3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c6e18ee9f8ea1d7dc6592d576c5a1163db526639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419851"
---
# <a name="imapiformmgrcreateform"></a>IMAPIFormMgr::CreateForm

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает форму для создания нового сообщения на основе класса сообщения формы.
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Handle to the parent window for the progress indicator that is displayed while the form is opened. Параметр _ulUIParam_ игнорируется, если MAPI_DIALOG флага в параметре _ulFlags._ 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет открытием формы. Можно установить следующий флаг:
    
MAPI_DIALOG 
  
> Отображает пользовательский интерфейс для предоставления состояния или запроса дополнительных сведений. Если этот флаг не установлен, пользовательский интерфейс не отображается.
    
 _pfrminfoToActivate_
  
> [in] Указатель на информационный объект формы, используемый для открытия формы.
    
 _refiidToAsk_
  
> [in] Указатель на идентификатор интерфейса для интерфейса, возвращаемой для созданного объекта формы. Параметр  _refiidToAsk_ не должен иметь NULL. 
    
 _ppvObj_
  
> [out] Указатель на указатель на возвращенный интерфейс.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_INTERFACE 
  
> Запрашиваемая интерфейс не поддерживается объектом формы.
    
## <a name="remarks"></a>Примечания

Посетители форм звонят **методу IMAPIFormMgr::CreateForm,** чтобы открыть форму для создания нового сообщения на основе класса сообщения формы. **CreateForm** открывает форму, создавая экземпляр сервера форм для этой формы, как описано в данном объекте сведений формы. При необходимости **CreateForm** вызывает метод [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) для загрузки кода сервера формы на диск пользователя. 
  
Параметр  _pfrminfoToActivate должен_ указать на объект сведений о форме, который был правильно разрешен. 
  
После открытия формы вызываемая форма должна настроить сообщение с помощью интерфейса [IPersistMessage](ipersistmessageiunknown.md) и при желании настроить контекст представления для формы. Дополнительные сведения см. [в теме "Запуск сервера форм".](launching-a-form-server.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI использует метод **IMAPIFormMgr::CreateForm** для создания формы перед ее отображением.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Запуск сервера форм](launching-a-form-server.md)


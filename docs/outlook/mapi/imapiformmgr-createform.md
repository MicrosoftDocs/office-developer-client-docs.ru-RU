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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает форму для создания нового сообщения на основе класса сообщений формы.
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Ручка родительского окна для индикатора прогресса, отображаемого во время открытия формы. Параметр _ulUIParam_ игнорируется, если флаг MAPI_DIALOG в параметре _ulFlags._ 
    
 _ulFlags_
  
> [in] Битмаски флагов, которые контролируют, как форма открывается. Можно установить следующий флаг:
    
MAPI_DIALOG 
  
> Отображает пользовательский интерфейс для предоставления статуса или запроса дополнительных сведений. Если этот флаг не установлен, пользовательский интерфейс не отображается.
    
 _pfrminfoToActivate_
  
> [in] Указатель на информационный объект формы, используемый для открытия формы.
    
 _refiidToAsk_
  
> [in] Указатель на идентификатор интерфейса (IID) для возврата интерфейса для созданного объекта формы. Параметр  _refiidToAsk_ не должен быть NULL. 
    
 _ppvObj_
  
> [вышел] Указатель на указатель на возвращенный интерфейс.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_INTERFACE 
  
> Запрашиваемая интерфейсная форма не поддерживается объектом формы.
    
## <a name="remarks"></a>Примечания

Зрители формы звонят по методу **IMAPIFormMgr::CreateForm,** чтобы открыть форму для создания нового сообщения на основе класса сообщений формы. **CreateForm** открывает форму, создавая экземпляр сервера формы для этой формы, как описано в данном информационном объекте формы. При необходимости **CreateForm** вызывает [метод IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) для загрузки кода сервера форм на диск пользователя. 
  
Параметр  _pfrminfoToActivate должен_ указать на объект информационной формы, который был правильно разрешен. 
  
После открытия формы зритель формы вызова должен настроить сообщение с помощью интерфейса [IPersistMessage](ipersistmessageiunknown.md) и может дополнительно настроить контекст представления для формы. Дополнительные сведения см. в [дополнительных сведениях о запуске сервера форм.](launching-a-form-server.md) 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |MFCMAPI использует **метод IMAPIFormMgr::CreateForm** для создания формы перед ее отображением.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Запуск сервера форм](launching-a-form-server.md)


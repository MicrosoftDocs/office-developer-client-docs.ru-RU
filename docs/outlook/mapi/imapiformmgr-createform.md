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
ms.openlocfilehash: e86c3d9678739c09024c0655cbbbb702749a53f0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586167"
---
# <a name="imapiformmgrcreateform"></a>IMAPIFormMgr::CreateForm

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Дескриптор родительского окна для индикатора, отображаемое при открытии формы. Параметр _ulUIParam_ игнорируется, пока флаг MAPI_DIALOG будет выполнен с помощью параметра _ulFlags_ . 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который определяет, как форма будет открыта. Можно задать следующий флаг:
    
MAPI_DIALOG 
  
> Отображает пользовательский интерфейс для предоставления состояния или запрашивать у пользователя для получения дополнительных сведений. Если этот флаг не установлен, пользовательский интерфейс не отображается.
    
 _pfrminfoToActivate_
  
> [in] Указатель на объект данные формы, который используется для открытия формы.
    
 _refiidToAsk_
  
> [in] Указатель интерфейса должно быть возвращено для объекта формы, которая была создана с идентификатором интерфейса (ИД интерфейса). Параметр _refiidToAsk_ не должна быть NULL. 
    
 _ppvObj_
  
> [out] Указатель на указатель на возвращенный интерфейс.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
MAPI_E_NO_INTERFACE 
  
> Запрошенный интерфейс не поддерживается объектом формы.
    
## <a name="remarks"></a>Замечания

Средства просмотра форм вызовите метод **IMAPIFormMgr::CreateForm** для открытия формы для создания нового сообщения на основе класса сообщения формы. **CreateForm** открывает форму путем создания экземпляра сервера форм для этой формы, как описано в объекте данные указанной формы. При необходимости **CreateForm** вызывает метод [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) , чтобы загрузить серверного кода формы диск компьютера пользователя. 
  
Параметр _pfrminfoToActivate_ должен указывать на объект данные формы, правильно разрешены. 
  
После открытия формы, вызывающий средство просмотра формы необходимо настроить сообщение с помощью интерфейса [IPersistMessage](ipersistmessageiunknown.md) и при необходимости можно настроить контекст представления для формы. Для получения дополнительных сведений см [запуска сервера формы](launching-a-form-server.md). 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |Mfcmapi (en) использует метод **IMAPIFormMgr::CreateForm** для создания формы перед их отображением.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)
  
[Запуск сервера форм](launching-a-form-server.md)


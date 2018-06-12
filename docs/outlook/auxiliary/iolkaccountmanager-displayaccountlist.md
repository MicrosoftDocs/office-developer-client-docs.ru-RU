---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Отображает диалоговое окно Параметры учетной записи или добавление новой учетной записи.
ms.openlocfilehash: 3c7c433eb4d8f316d32b6cd12bbbbb0e1a1cee43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807852"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

Отображает диалоговое окно **Настройки учетной записи** и **Добавление новой учетной записи** . 
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::DisplayAccountList ( 
    HWND hwnd,
    DWORD dwFlags,
    LPCWSTR wszTitle,
    DWORD cCategories,
    const CLSID * rgclsidCategories,
    const CLSID * pclsidType
);

```

## <a name="parameters"></a>Parameters

_HWND_
  
> [in] Дескриптор окна модальное диалоговое окно отображаемой. Может быть равно нулю.
    
_dwFlags_
  
> [in] Флаги для изменения режима отображения. 
    
   - **ACCTUI_NO_WARNING**— не выводить предупреждения о том, что изменения не вступят в силу только после перезапуска Outlook. Применяется только в том случае, если приложение является выполняется в процессе с Outlook.exe.
    
   - **ACCTUI_SHOW_DATA_TAB**— Показать диалоговое окно **Параметры учетной записи** с вкладкой **данных** . Допустимо только в том случае, если не указано **ACCTUI_SHOW_ACCTWIZARD** . 
    
   - **ACCTUI_SHOW_ACCTWIZARD**— Отображение диалогового окна **Добавление новой учетной записи** . 
    
_wszTitle_
  
> [in] Этот параметр не используется и не должен иметь значение NULL.
    
_cCategories_
  
> [in] Этот параметр не используется и должен иметь значение NULL. 
    
_rgclsidCategories_
  
> [in] Этот параметр не используется и должен иметь значение NULL.
    
_pclsidType_
  
> [in] Этот параметр не используется и должен иметь значение NULL.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |Вызов выполнен успешно.  <br/> |
|E_ACCT_UI_BUSY  <br/> |Не удалось создать диалоговое окно.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Диалоговое окно " **Добавление новой учетной записи** " возвратил ошибку.  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |Параметр _cCategories_, _rgclsidCategories_или _pclsidType_ не равно NULL.  <br/> |
|MAPI_E_USER_CANCEL  <br/> |Диалоговое окно " **Настройка учетных записей** " возвратил ошибку.  <br/> |
   
## <a name="remarks"></a>Замечания

Параметры _cCategories_, _rgclsidCategories_и _pclsidType_ не используется в данный момент и должен иметь значение NULL.  _wszTitle_ не используется, а также должен иметь значение NULL. 
  


---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Отображает диалоговое окно "Параметры учетной записи" или "Добавление новой учетной записи".
ms.openlocfilehash: ecf5242fa4f224516e12e667ab66fd0adfe4a25d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415035"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

Отображает диалоговое окно **"Параметры учетной записи"** или **"Добавление новой** учетной записи". 
  
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

## <a name="parameters"></a>Параметры

_hwnd_
  
> [in] Handle to the window to which the displayed dialog box is modal. Может быть нулем.
    
_dwFlags_
  
> [in] Флаги для изменения поведения дисплея. 
    
   - **ACCTUI_NO_WARNING**— не отображайте предупреждение о том, что изменения не будут действовать до перезапуска Outlook. Применяется, только если приложение работает в процессе с Outlook.exe.
    
   - **ACCTUI_SHOW_DATA_TAB**— отображите диалоговое окно **"Параметры** учетной записи" с **выбранной** вкладками "Данные". Допустимо, **только ACCTUI_SHOW_ACCTWIZARD** не за установлено. 
    
   - **ACCTUI_SHOW_ACCTWIZARD**— отобразить диалоговое окно "Добавление **новой** учетной записи". 
    
_wszTitle_
  
> [in] Этот параметр не используется и должен иметь NULL.
    
_cCategories_
  
> [in] Этот параметр не используется и должен иметь NULL. 
    
_rgclsidCategories_
  
> [in] Этот параметр не используется и должен иметь NULL.
    
_pclsidType_
  
> [in] Этот параметр не используется и должен иметь NULL.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Вызов был успешным.  <br/> |
|E_ACCT_UI_BUSY  <br/> |Не удалось создать диалоговое окно.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |В **диалоговом окне** "Добавление новой учетной записи" возвращена ошибка.  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |Параметр  _cCategories,_  _rgclsidCategories_ или  _pclsidType_ не имеет NULL.  <br/> |
|MAPI_E_USER_CANCEL  <br/> |В **диалоговом окне** "Параметры учетной записи" возвращена ошибка.  <br/> |
   
## <a name="remarks"></a>Примечания

Параметры  _cCategories,_  _rgclsidCategories_ и  _pclsidType_ в настоящее время не используются и должны иметь NULL.  _wszTitle_ не используется и также должен иметь NULL. 
  


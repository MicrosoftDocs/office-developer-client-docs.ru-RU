---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Отображает диалоговое окно Параметры учетной записи или диалоговое окно "Добавить новую учетную запись".
ms.openlocfilehash: ecf5242fa4f224516e12e667ab66fd0adfe4a25d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415035"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

Отображает диалоговое **окно Параметры** учетной записи или диалоговое окно **"Новая** учетная запись". 
  
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

_hwnd_
  
> [in] Ручка к окну, в которое отображается диалоговое окно, является модальной. Может быть ноль.
    
_dwFlags_
  
> [in] Флаги для изменения поведения дисплея. 
    
   - **ACCTUI_NO_WARNING**— не отображайте предупреждение о том, что изменения не будут действовать до Outlook перезапуска. Применяется только в том случае, если приложение работает в процессе с Outlook.exe.
    
   - **ACCTUI_SHOW_DATA_TAB**— покажите диалоговое **окно Параметры** учетной записи с выбранной вкладке **Data.** Допустимо **только ACCTUI_SHOW_ACCTWIZARD** не установлено. 
    
   - **ACCTUI_SHOW_ACCTWIZARD**— отображение **диалогового окна Добавить новую** учетную запись. 
    
_wszTitle_
  
> [in] Этот параметр не используется и должен быть NULL.
    
_cCategories_
  
> [in] Этот параметр не используется и должен быть NULL. 
    
_rgclsidCategories_
  
> [in] Этот параметр не используется и должен быть NULL.
    
_pclsidType_
  
> [in] Этот параметр не используется и должен быть NULL.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Вызов был успешным.  <br/> |
|E_ACCT_UI_BUSY  <br/> |Диалоговое окно не удалось создать.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |В **диалоговом окне Добавить** новую учетную запись была возвращена ошибка.  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |Параметр  _cCategories,_  _rgclsidCategories_ или  _pclsidType_ не является NULL.  <br/> |
|MAPI_E_USER_CANCEL  <br/> |Диалоговое **окно Параметры** учетной записи возвращает ошибку.  <br/> |
   
## <a name="remarks"></a>Примечания

Параметры  _cCategories,_  _rgclsidCategories_ и  _pclsidType_ в настоящее время не используются и должны быть NULL.  _wszTitle_ не используется и также должен быть NULL. 
  


---
title: иолкаккаунтманажердисплайаккаунтлист
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

Отображает диалоговое окно " **Параметры учетной записи** " или " **Добавление новой учетной записи** ". 
  
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
  
> возврата Дескриптор окна, в котором отображается модальное диалоговое окно. Может равняться нулю.
    
_dwFlags_
  
> возврата Флаги для изменения поведения отображения. 
    
   - **ACCTUI_NO_WARNING**не отображать предупреждение о том, что изменения вступят в силу только после перезапуска Outlook. Применяется только в том случае, если приложение выполняется в процессе работы с Outlook. exe.
    
   - **ACCTUI_SHOW_DATA_TAB**— отображение диалогового окна " **Параметры учетной записи** " с выбранной вкладкой " **данные** ". Допустимо, только если не задано значение **ACCTUI_SHOW_ACCTWIZARD** . 
    
   - **ACCTUI_SHOW_ACCTWIZARD**— отображение диалогового окна " **Добавление новой учетной записи** ". 
    
_всзтитле_
  
> возврата Этот параметр не используется и должен иметь значение NULL.
    
_ккатегориес_
  
> возврата Этот параметр не используется и должен иметь значение NULL. 
    
_ргклсидкатегориес_
  
> возврата Этот параметр не используется и должен иметь значение NULL.
    
_пклсидтипе_
  
> возврата Этот параметр не используется и должен иметь значение NULL.
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Вызов выполнен успешно.  <br/> |
|E_ACCT_UI_BUSY  <br/> |Не удается создать диалоговое окно.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Диалоговое окно " **Добавление новой учетной записи** " вернуло ошибку.  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |Параметр _ккатегориес_, _ргклсидкатегориес_или _пклсидтипе_ имеет значение, отличное от NULL.  <br/> |
|MAPI_E_USER_CANCEL  <br/> |Диалоговое окно " **Параметры учетной записи** " возвратило ошибку.  <br/> |
   
## <a name="remarks"></a>Примечания

Параметры _ккатегориес_, _ргклсидкатегориес_и _пклсидтипе_ не используются в данный момент и должны иметь значение null.  _всзтитле_ не используется, и он также должен иметь значение null. 
  


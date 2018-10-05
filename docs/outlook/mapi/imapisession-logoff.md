---
title: IMAPISessionLogoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Logoff
api_type:
- COM
ms.assetid: 93e38f6c-4b67-4f2d-bc94-631efec86852
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 317c3702415ddf30038ccd0d40cdf0f19abc61f8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399650"
---
# <a name="imapisessionlogoff"></a>IMAPISession::Logoff

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Завершение сеанса MAPI.
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Дескриптор родительского окна все диалоговые окна или окна для отображения. Этот параметр игнорируется, если флаг MAPI_LOGOFF_UI не установлен.
    
 _ulFlags_
  
> [in] Битовая маска флаги, определяющие операции выхода из системы. Можно задать следующие флажки:
    
MAPI_LOGOFF_SHARED 
  
> Если этот сеанс является общей, все клиенты, войти в систему с помощью общего сеанса уведомляться об выхода из системы в процессе выполнения. Клиенты должны выйти из системы. Каждый клиент, который использует совместный сеанс можно задать этот флаг. MAPI_LOGOFF_SHARED игнорируется, если не общий текущего сеанса.
    
MAPI_LOGOFF_UI 
  
> **Выход из системы** может отображать диалоговое окно во время операции, возможно запросом на подтверждение. 
    
 _ulReserved_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Выход из системы операция выполнена успешно.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISession::Logoff** завершает сеанс MAPI. При возврате **выхода из системы** , ни один из методов, за исключением [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) может быть вызван. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При возврате **выхода из системы** , release путем вызова метода **функции IUnknown::Release** объект сеанса. 
  
Дополнительные сведения о завершении сеанса можно [Завершение сеанса MAPI](ending-a-mapi-session.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::Logoff  <br/> |Mfcmapi (en) использует метод **IMAPISession::Logoff** для сеанса перед выпуском его.  <br/> |
   
> [!NOTE]
> Из-за быстрого завершения работы, введенные в пакет обновления 2 для Microsoft Office Outlook 2007, Microsoft Outlook 2010 и Microsoft Outlook 2013 клиенты никогда не следует передавать параметр **MAPI_LOGOFF_SHARED** в [IMAPISession::Logoff](imapisession-logoff.md). Передача **MAPI_LOGOFF_SHARED** вызывает все клиенты MAPI приступить к завершению работы и будет привести к возникновению проблем. 
  
## <a name="see-also"></a>См. также



[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Завершение сеанса MAPI](ending-a-mapi-session.md)


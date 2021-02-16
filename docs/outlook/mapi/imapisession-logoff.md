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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338110"
---
# <a name="imapisessionlogoff"></a>IMAPISession::Logoff

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Завершает сеанс MAPI.
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a>Параметры

 _ulUIParam_
  
> [in] Handle to the parent window of any dialog boxes or windows to be displayed. Этот параметр игнорируется, если MAPI_LOGOFF_UI флага не задан.
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которые контролируют операцию выйдите из системы. Можно установить следующие флаги:
    
MAPI_LOGOFF_SHARED 
  
> Если этот сеанс является общим, все клиенты, которые вошли в систему с помощью общего сеанса, должны быть уведомлены о том, что происходит вход. Клиенты должны выйти. Любой клиент, использующий общий сеанс, может установить этот флаг. MAPI_LOGOFF_SHARED игнорируется, если текущий сеанс не является общим.
    
MAPI_LOGOFF_UI 
  
> **Во время** операции можно отобразить диалоговое окно с запросом подтверждения. 
    
 _ulReserved_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Операция logoff прошла успешно.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::Logoff** завершает сеанс MAPI. Когда **logoff** возвращается, ни один из методов, кроме [IUnknown::Release,](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) не может быть вызван. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Когда **logoff** возвращается, отпустите объект сеанса, вызывая его **метод IUnknown::Release.** 
  
Дополнительные сведения о завершении сеанса см. в под [вопросе "Завершение сеанса MAPI".](ending-a-mapi-session.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::Logoff  <br/> |MFCMAPI использует метод **IMAPISession::Logoff** для выхода из сеанса перед его освобождением.  <br/> |
   
> [!NOTE]
> Из-за быстрого завершения работы, введенного в Microsoft Office Outlook 2007 Пакет обновления 2, Microsoft Outlook 2010, русская версия и Microsoft Outlook 2013, клиенты никогда не должны передавать параметр **MAPI_LOGOFF_SHARED** [iMAPISession::Logoff](imapisession-logoff.md). Передача **MAPI_LOGOFF_SHARED** приведет к тому, что все клиенты MAPI начнут работу и произойдет непредвиденное поведение. 
  
## <a name="see-also"></a>См. также



[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Завершение сеанса MAPI](ending-a-mapi-session.md)


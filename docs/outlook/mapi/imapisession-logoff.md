---
title: Имаписессионлогофф
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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Завершает сеанс MAPI.
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a>Параметры

 _Улуипарам_
  
> возврата Дескриптор родительского окна всех диалоговых окон и окон, которые должны отображаться. Этот параметр игнорируется, если не установлен флаг МАПИ_ЛОГОФФ_УИ.
    
 _ulFlags_
  
> возврата Битовая маска флагов, которые контролируют операцию выхода. Можно задать следующие флаги:
    
МАПИ_ЛОГОФФ_ШАРЕД 
  
> Если этот сеанс является общим, все клиенты, выполнившие вход с использованием общего сеанса, должны получать уведомления о выходе из системы. Клиенты должны выйти из системы. Этот флаг может устанавливать любой клиент, использующий общий сеанс. МАПИ_ЛОГОФФ_ШАРЕД игнорируется, если текущий сеанс не является общим.
    
МАПИ_ЛОГОФФ_УИ 
  
> При **выходе из системы** во время операции выводится диалоговое окно, которое может запрашивать подтверждение у пользователя. 
    
 _Улресервед_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Операция выхода выполнена успешно.
    
## <a name="remarks"></a>Комментарии

Метод **IMAPISession:: logoff** ЗАВЕРШАЕТ сеанс MAPI. При возвращении после **выхода** ни один из методов, кроме [IUnknown::](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) , не может быть вызван. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

При **выходе из системы** выпустите объект Session, вызвав его метод **IUnknown:: Release** . 
  
Для получения дополнительных сведений о завершении сеанса обратитесь [к разделу завершение сеанса MAPI](ending-a-mapi-session.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мапиобжектс. cpp  <br/> |Кмапиобжектс:: выход  <br/> |MFCMAPI использует метод **IMAPISession:: logoff** для выхода из сеанса перед его освобождением.  <br/> |
   
> [!NOTE]
> Из-за возможности быстрого завершения работы, появившегося в Microsoft Office Outlook 2007 с пакетом обновления 2, Microsoft Outlook 2010 и Microsoft Outlook 2013, клиенты никогда не должны передавать параметр **мапи_логофф_шаред** в [IMAPISession:: LOGOFF](imapisession-logoff.md). Передача **мапи_логофф_шаред** приведет к тому, что все клиенты MAPI начнут завершать работу и произойдет неожиданное поведение. 
  
## <a name="see-also"></a>См. также



[IMAPISession: IUnknown](imapisessioniunknown.md)


[MFCMAPI как пример кода](mfcmapi-as-a-code-sample.md)
  
[Завершение сеанса MAPI](ending-a-mapi-session.md)


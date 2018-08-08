---
title: IMAPIFormSetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.SetViewContext
api_type:
- COM
ms.assetid: a7b10007-42d8-4755-8362-f8ad9a8dad68
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c1ba49ba1b4deacb684da1411d86ebd4dd19e63f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808890"
---
# <a name="imapiformsetviewcontext"></a>IMAPIForm::SetViewContext

  
  
**Относится к**: Outlook 
  
Устанавливает контекст представления для формы. 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a>Параметры

 _pViewContext_
  
> [in] Указатель на новый контекст представления для формы.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Контекст представления был успешно установлен.
    
## <a name="remarks"></a>Замечания

Средства просмотра формы вызовите метод **IMAPIForm::SetViewContext** , чтобы установить контекст представления определенной формы как текущий. Форма может иметь только один контекст представления за раз. 
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Большинство серверов формы реализации **SetViewContext** , используя следующий алгоритм: 
  
- Если контекст представления для формы уже существует, Отмена регистрации формы путем вызова метода [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) с **значение null,** с помощью параметра _pmnvs_ , а затем вызвать контекст представления [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) метод, чтобы уменьшить его счетчик ссылок. 
    
- Если новый контекст представления, не равно **null**, вызов **IMAPIViewContext::SetAdviseSink** с помощью параметра _pViewContext_ для настройки нового представления уведомить приемника. 
    
- Если новый контекст представления, не равно **null**, вызовите метод [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) , чтобы определить, какие флаги состояния были установлены. 
    
- Если новый контекст представления, не равно **null**, сохраните ее и вызвать метод [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) увеличить счетчик ссылок на него. 
    
- Обновите все элементы пользовательского интерфейса, которые зависят от контекста представления. 
    
В зависимости от состояния флаги, возвращенный из **IMAPIViewContext::GetViewStatus** **SetViewContext** можно также выполнить другие действия. Например если возвращаются флаги VCSTATUS_NEXT и VCSTATUS_PREV, **SetViewContext** можно включить кнопки **Далее** и **Назад** для нового контекста представления. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CreateAndDisplayNewMailInFolder  <br/> |Mfcmapi (en) использует метод **IMAPIForm::SetViewContext** для установки контекст представления mfcmapi (en) на форме перед отображением формы.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

